---
title: Simuladores e aplicativos host quânticos | Microsoft Docs
description: Descreve como impulsionar simuladores de quantum com uma linguagem .NET de computação clássica, normalmente, C# ou Q#.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines
ms.openlocfilehash: 14aed75ed0ed192f88699b1c7dbacfae23f74642
ms.sourcegitcommit: 9d1c045cf1a2c3e19030cb38dbc7496dbd24ab58
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2020
ms.locfileid: "73442219"
---
# <a name="quantum-simulators-and-host-applications"></a>Simuladores e aplicativos host quânticos

## <a name="what-youll-learn"></a>O que você vai aprender

> [!div class="checklist"]
> * Como os algoritmos quânticos são executados
> * Quais simuladores de quantum estão incluídos nesta versão
> * Como escrever um driver C# para o algoritmo quântico

## <a name="the-quantum-development-kit-execution-model"></a>O modelo de execução do Quantum development kit

Em [Como escrever um programa quântico](xref:microsoft.quantum.write-program), executamos nosso algoritmo quântico passando um objeto `QuantumSimulator` para o método `Run` da classe do algoritmo.
A classe `QuantumSimulator` executa o algoritmo quântico simulando totalmente o vetor de estado quântico, que é perfeito para executar e testar `Teleport`.
Confira o [Guia de conceitos](xref:microsoft.quantum.concepts.intro) para saber mais sobre os vetores de estado quântico.

Outros computadores de destino podem ser usados para executar um algoritmo quântico.
O computador é responsável por fornecer implementações de primitivos quânticos para o algoritmo.
Isso inclui operações primitivas, como H, CNOT e Measure, bem como gerenciamento e acompanhamento de qubits.
Diferentes classes de computadores quânticos representam modelos de execução diferentes para o mesmo algoritmo quântico.

Cada tipo de computador quântico pode fornecer diferentes implementações desses primitivos.
Por exemplo, o simulador de rastreamento do computador quântico incluído no kit de desenvolvimento não faz nenhuma simulação.
Em vez disso, ele rastreia o uso de portões, qubits e outros recursos para o algoritmo.

### <a name="quantum-machines"></a>Computadores quânticos

No futuro, definiremos classes adicionais de computadores quânticos para dar suporte a outros tipos de simulação e à execução em computadores quânticos topológicos.
Permitir que o algoritmo permaneça constante enquanto varia a implementação de computador subjacente facilita o teste e a depuração de um algoritmo em simulação e, em seguida, executa-o em um hardware real com a confiança de que o algoritmo não foi alterado.

### <a name="whats-included-in-this-release"></a>O que está incluído nesta versão

Esta versão do Kit do Desenvolvedor do Quantum inclui várias classes de computadores quânticos.
Todas elas são definidas no namespace `Microsoft.Quantum.Simulation.Simulators`.

* Um [simulador de vetor de estado completo](xref:microsoft.quantum.machines.full-state-simulator), a classe `QuantumSimulator`.
* Um [estimador de recursos simples](xref:microsoft.quantum.machines.resources-estimator), a classe `ResourcesEstimator`, permite uma análise de nível superior dos recursos necessários para executar um algoritmo quântico.
* Um [estimador de recursos baseado em rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro), a classe `QCTraceSimulator`, permite a análise avançada de consumos de recursos para o grafo de chamadas inteiro do algoritmo.
* Um [simulador Toffoli](xref:microsoft.quantum.machines.toffoli-simulator), a classe `ToffoliSimulator`.

## <a name="writing-a-host-application"></a>Como escrever um aplicativo host

Em [Como escrever um programa quântico](xref:microsoft.quantum.write-program), escrevemos um driver C# simples para nosso algoritmo de teletransporte. Um driver C# tem quatro objetivos principais:

* Construir o computador de destino
* Calcular os argumentos necessários para o algoritmo quântico
* Executar o algoritmo quântico usando o simulador
* Processar o resultado da operação

Aqui, discutiremos cada etapa mais detalhadamente.

### <a name="constructing-the-target-machine"></a>Construir o computador de destino

Os computadores quânticos são instâncias de classes .NET normais e, portanto, são criadas invocando o construtor delas, assim como qualquer classe .NET.
Alguns simuladores, incluindo o `QuantumSimulator`, implementam a interface <xref:System.IDisposable?displayProperty=nameWithType> .NET e, portanto, devem ser encapsulados em uma instrução `using` C#.

### <a name="computing-arguments-for-the-algorithm"></a>Como calcular argumentos para o algoritmo

Em nosso exemplo de `Teleport`, calculamos alguns argumentos relativamente artificiais para passarmos ao nosso algoritmo quântico.
No entanto, de modo mais geral, há dados significativos exigidos pelo algoritmo quântico e é mais fácil fornecê-los por meio do driver clássico.

Por exemplo, ao fazer simulações químicas, o algoritmo quântico exige uma tabela grande de integrais de interação orbital molecular.
Geralmente, eles são lidos de um arquivo que é fornecido durante a execução do algoritmo.
Como o Q# não tem um mecanismo para acessar o sistema de arquivos, esse tipo de dados é melhor coletado pelo driver clássico e, em seguida, passado para o método `Run` do algoritmo quântico.

Outro caso em que o driver clássico desempenha um papel fundamental é em métodos de variação.
Nessa classe de algoritmos, um estado quântico é preparado com base em alguns parâmetros clássicos e esse estado é usado para calcular algum valor de interesse.
Os parâmetros são ajustados com base em um tipo de algoritmo de aprendizado de máquina ou de escalada e o algoritmo quântico é executado novamente.
Para esses algoritmos, o próprio algoritmo de escalada é mais bem implementado como uma função puramente clássica que é chamada pelo driver clássico; os resultados da escalada são então passados para a próxima execução do algoritmo quântico.

### <a name="running-the-quantum-algorithm"></a>Como executar o algoritmo quântico

Essa parte é geralmente muito simples.
Cada operação Q# é compilada em uma classe que fornece um método `Run` estático.
Os argumentos para esse método são fornecidos pela tupla de argumento combinada da própria operação, mais um primeiro argumento adicional que é o simulador a ser usado na execução. Para uma operação que espera a tupla nomeada do tipo `(a: String, (b: Double, c: Double))`, a contraparte combinada dela é do tipo `(String a, Double b, Double c)`.


Há algumas sutilezas ao passar argumentos para um método `Run`:

* As matrizes precisam ser encapsuladas em um objeto `Microsoft.Quantum.Simulation.Core.QArray<T>`.
    Uma classe `QArray` tem um construtor que pode usar qualquer coleção ordenada (`IEnumerable<T>`) de objetos apropriados.
* A tupla vazia, `()` em Q#, é representada por `QVoid.Instance` em C#.
* As tuplas não vazias são representadas como instâncias `ValueTuple` do .NET.
* Os tipos definidos pelo usuário Q# são passados como o tipo base.
* Para passar uma operação ou uma função para um método `Run`, você precisa obter uma instância da classe da operação ou da função, usando o método `Get<>` do simulador.

### <a name="processing-the-results"></a>Como processar os resultados

Os resultados do algoritmo quântico são retornados do método `Run`.
O método `Run` é executado de maneira assíncrona e, portanto, retorna uma instância de <xref:System.Threading.Tasks.Task`1>.
Há várias maneiras de obter os resultados da operação real. A mais simples é usar a [propriedade `Result`](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task-1.result) de `Task`:

```csharp
    var res = BellTest.Run(sim, 1000, initial).Result;
```
mas outras técnicas, como usar o [método `Wait`](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task.wait) ou a [palavra-chave `await`](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/await) do C# também funcionarão.

Como acontece com argumentos, as tuplas Q# são representadas como instâncias de `ValueTuple` e as matrizes Q# são representadas como instâncias de `QArray`.
Os tipos definidos pelo usuário são retornados como os tipos base.
A tupla vazia, `()`, é retornada como uma instância da classe `QVoid`.

Muitos algoritmos quânticos exigem pós-processamento substancial para obter respostas úteis.
Por exemplo, a parte quântica do algoritmo de Shor é apenas o início de uma computação que localiza os fatores de um número.

Na maioria dos casos, é mais simples e mais fácil fazer esse tipo de pós-processamento no driver clássico.
Somente o driver clássico pode relatar resultados para o usuário ou gravá-los em disco.
O driver clássico terá acesso a bibliotecas analíticas e a outras funções matemáticas que não são expostas no Q#.


## <a name="failures"></a>Falhas

Quando a instrução `fail` Q# é atingida durante a execução de uma operação, uma `ExecutionFailException` é gerada.

Devido ao uso de `System.Task` no método `Run`, a exceção gerada como resultado de uma instrução `fail` será encapsulada em uma `System.AggregateException`.
Para encontrar o motivo real da falha, você precisará iterar no `AggregateException` 
`InnerExceptions`, por exemplo:

```csharp

            try
            {
                using(var sim = new QuantumSimulator())
                {
                    /// call your operations here...
                }
            }
            catch (AggregateException e)
            {
                // Unwrap AggregateException to get the message from Q# fail statement.
                // Go through all inner exceptions.
                foreach (Exception inner in e.InnerExceptions)
                {
                    // If the exception of type ExecutionFailException
                    if (inner is ExecutionFailException failException)
                    {
                        // Print the message it contains
                        Console.WriteLine($" {failException.Message}");
                    }
                }
            }
```

## <a name="other-classical-languages"></a>Outras linguagens clássicas

Embora as amostras que fornecemos estejam em C#, F# e Python, o Quantum development kit também dá suporte à composição de programas host clássicos em outras linguagens.
Por exemplo, se você quiser escrever um programa host no Visual Basic, [ele deverá funcionar corretamente](https://github.com/tcNickolas/MiscQSharp/blob/master/Quantum_VBNet/README.md#using-q-with-visual-basic-net).
