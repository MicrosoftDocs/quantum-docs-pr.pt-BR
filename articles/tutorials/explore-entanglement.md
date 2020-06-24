---
title: Explorar o entrelaçamento com Q#
description: Saiba como escrever um programa quântico em Q#. Desenvolver um aplicativo de Estado de Bell usando o QDK (Quantum development kit)
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 05/29/2020
ms.topic: tutorial
uid: microsoft.quantum.write-program
ms.openlocfilehash: 294366b884da93f11c60cfdbdce9b40cf5202b0d
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274226"
---
# <a name="tutorial-explore-entanglement-with-q"></a>Tutorial: Explorar o emaranhamento com o Q\#

Neste tutorial, mostraremos como escrever um programa Q# que processa e mede qubits e demonstra os efeitos da superposição e do emaranhamento.
Isso orientará você na instalação do QDK, na criação e na execução do programa em um simulador quântico.  

Você escreverá um aplicativo chamado Bell para demonstrar o entrelaçamento quântico.
O nome Bell foi criado em referência aos estados Bell, que são estados quânticos específicos de dois qubits usados para representar os exemplos mais simples de sobreposição e entrelaçamento quântico.

## <a name="prerequisites"></a>Pré-requisitos

Se estiver pronto para começar a codificação, siga estas etapas antes de continuar: 

* Instale o Quantum development kit para o [Python](xref:microsoft.quantum.install.python) ou o [.NET](xref:microsoft.quantum.install.cs).
* Caso já tenha o QDK instalado, verifique se você o [atualizou](xref:microsoft.quantum.update) para a última versão

Você também pode acompanhar a narrativa sem instalar o QDK, examinar as visões gerais da linguagem de programação Q# e os primeiros conceitos da computação quântica.

## <a name="demonstrating-qubit-behavior-with-q"></a>Demonstrar o comportamento do qubit com Q#

Lembre-se de nossa [definição simples de um qubit](xref:microsoft.quantum.overview.understanding).  Onde os bits clássicos contêm apenas um valor binário, como 0 ou 1, o estado de um [qubit](xref:microsoft.quantum.glossary#qubit) pode estar em uma **sobreposição** de 0 e 1.  Conceitualmente, um qubit pode ser pensado como uma direção no espaço (também conhecido como um vetor).  Um qubit pode estar em qualquer uma das possíveis direções. Os dois **estados clássicos** são as duas direções, que representam 100% de chance de medir 0 e 100% de chance de medir 1.  Essa representação também é visualizada mais formalmente pela [esfera Bloch](/quantum/concepts/the-qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere).

O ato de medição produz um resultado binário e altera um estado do qubit. A medida produz um valor binário, 0 ou 1.  O qubit passa de estar em sobreposição (qualquer direção) para um dos estados clássicos.  Depois disso, repetir a mesma medição sem nenhuma operação intermediária produz o mesmo resultado binário.  

Vários qubits podem ser [**entrelaçados**](xref:microsoft.quantum.glossary#entanglement). Quando fazemos uma medição de um qubit entrelaçado, nosso conhecimento do estado dos outros é atualizado também.

Agora, estamos prontos para demonstrar como o Q# expressa esse comportamento.  Você começará com o programa mais simples possível e o desenvolverá para demonstrar a sobreposição quântica e o entrelaçamento quântico.

## <a name="setup"></a>Instalação

Este tutorial usa um programa host e consiste em duas partes:

1. Uma série de algoritmos quânticos, implementados usando a linguagem de programação quântica Q#.
1. Um programa host, implementado em Python ou em C#, que serve como o principal ponto de entrada e invoca operações Q# para executar os algoritmos quânticos.

#### <a name="python"></a>[Python](#tab/tabid-python)

1. Escolha uma localização para seu aplicativo

1. Crie um arquivo chamado `Bell.qs`. Esse arquivo conterá o código Q#.

1. Crie um arquivo chamado `host.py`. Esse arquivo conterá o código de host do Python.

#### <a name="c-command-line"></a>[Linha de comando do C#](#tab/tabid-csharp)

1. Crie um projeto Q#:

    ```
    dotnet new console -lang Q# --output Bell
    cd Bell
    ```

    Você deverá ver um arquivo `.csproj`, um arquivo Q# chamado `Operations.qs` e um arquivo de programa host chamado `Driver.cs`

1. Renomear o arquivo Q#

    ```
    mv Operation.qs Bell.qs
    ```

#### <a name="visual-studio"></a>[Visual Studio](#tab/tabid-vs2019)

1. Criar um novo projeto

   * Abra o Visual Studio
   * Acesse o menu **Arquivo** e selecione **Novo** -> **Projeto...**
   * No gerenciador de modelos de projeto, digite `Q#` no campo de pesquisa e selecione o modelo `Q# Application`
   * Dê ao projeto o nome `Bell`

1. Renomear o arquivo Q#

   * Navegue até o **Gerenciador de Soluções**
   * Clique com o botão direito do mouse no arquivo `Operations.qs`
   * Renomeie-o como `Bell.qs`

* * *

## <a name="write-a-q-operation"></a>Escrever uma operação Q#

Nossa meta é preparar dois qubits em um estado quântico específico, demonstrando como operar em qubits com Q# para alterar seu estado e demonstrar os efeitos da sobreposição e entrelaçamento. Criaremos isso em partes para demonstrar os estados, as operações e a medida do qubit.

**Visão geral:**  no primeiro código abaixo, mostramos como trabalhar com qubits no Q#.  Apresentaremos duas operações, `M` e `X`, que transformam o estado de um qubit. 

Neste snippet de código, uma operação `Set` é definida que usa como parâmetro um qubit e outro parâmetro, `desired`, que representa o estado no qual gostaríamos que o qubit estivesse.  A operação `Set` executa uma medida no qubit usando a operação `M`.  Em Q#, uma medição de qubit sempre retorna `Zero` ou `One`.  Se a medição retornar um valor não igual a um valor desejado, Set “inverterá” o qubit; ou seja, executará uma operação `X`, que altera o estado do qubit para um novo estado no qual as probabilidades de uma medição retornar `Zero` e `One` são invertidas.  Para demonstrar o efeito da operação `Set`, uma operação `TestBellState` é adicionada.  Essa operação aceita como entrada um `Zero` ou `One` e chama a operação `Set` algum número de vezes com essa entrada, além de contar o número de vezes que `Zero` foi retornado da medição do qubit e do número de vezes que `One` foi retornado. É claro que, nesta primeira simulação da operação `TestBellState`, esperamos que a saída mostre que todas as medições do conjunto de qubits com `Zero` como a entrada do parâmetro retornarão `Zero` e todas as medições de um conjunto de qubits com `One` como a entrada do parâmetro retornarão `One`.  Mais adiante, adicionaremos código a `TestBellState` para demonstrar a sobreposição e o entrelaçamento.


### <a name="q-operation-code"></a>Código de operação Q#

1. Substitua o conteúdo do arquivo Bell.qs pelo seguinte código:

    ```qsharp
    namespace Quantum.Bell {
        open Microsoft.Quantum.Intrinsic;
        open Microsoft.Quantum.Canon;

        operation Set(desired : Result, q1 : Qubit) : Unit {
            if (desired != M(q1)) {
                X(q1);
            }
        }
    }
    ```

    Esta operação agora pode ser chamada para definir um qubit como um estado clássico, retornando `Zero` 100% do tempo ou retornando `One` 100% do tempo.  `Zero` e `One` são constantes que representam os únicos dois possíveis resultados de uma medição de um qubit.

    A operação `Set` mede o qubit.
    Se o qubit estiver no estado que desejamos, `Set` o deixará sozinho; caso contrário, executando a operação `X`, alteraremos o estado do qubit para o desejado.

### <a name="about-q-operations"></a>Sobre as operações Q#

Uma operação Q# é uma sub-rotina quântica. Ou seja, é uma rotina que pode ser chamada que contém operações quânticas.

Os argumentos de uma operação são especificados como uma tupla, entre parênteses.

O tipo de retorno da operação é especificado após dois-pontos. Nesse caso, a operação `Set` não tem retorno, sendo, portanto, marcada como retornando `Unit`. Em Q#, esse é o equivalente de `unit` em F#, que é aproximadamente análogo a `void` em C# e uma tupla vazia (`Tuple[()]`) no Python.

Você usou duas operações quânticas em sua primeira operação Q#:

* A operação [M](xref:microsoft.quantum.intrinsic.m), que mede o estado do qubit
* A operação [X](xref:microsoft.quantum.intrinsic.x), que inverte o estado de um qubit

Uma operação quântica transforma o estado de um qubit. Algumas vezes, as pessoas falam sobre portões quânticos em vez de operações, em analogia a portões lógicos clássicos. Isso está enraizado nos primórdios da computação quântica, quando os algoritmos eram meramente um constructo teórico e eram visualizados como diagramas de forma semelhante à dos diagramas de circuito na computação clássica.

### <a name="add-q-test-code"></a>Adicionar um código de teste Q#

1. Adicione a seguinte operação ao arquivo `Bell.qs`, dentro do namespace, após o final da operação `Set`:

    ```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using (qubit = Qubit()) {

            for (test in 1..count) {
                Set(initial, qubit);
                let res = M(qubit);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            Set(Zero, qubit);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes);
    }
    ```

    Essa operação (`TestBellState`) executará um loop para iterações `count`, definirá um valor `initial` especificado em um qubit e, em seguida, medirá (`M`) o resultado. Ela coletará estatísticas sobre quantos zeros e aqueles medidos e os retornará ao chamador. Ela executa outra operação necessária. Ela redefine o qubit para um estado conhecido (`Zero`) antes de retorná-lo, permitindo que outras pessoas aloquem esse qubit em um estado conhecido. Isso é exigido pela instrução `using`.

### <a name="about-variables-in-q"></a>Sobre as variáveis em Q#

Por padrão, as variáveis em Q# são imutáveis; o valor delas não pode ser alterado depois que elas são associadas. A palavra-chave `let` é usada para indicar a associação de uma variável imutável. Os argumentos da operação são sempre imutáveis.

Caso precise de uma variável cujo valor possa ser alterado, como `numOnes` no exemplo, você poderá declarar a variável com a palavra-chave `mutable`. O valor de uma variável mutável pode ser alterado usando uma instrução `set`.

Em ambos os casos, o tipo de uma variável é inferido pelo compilador. O Q# não exige nenhuma anotação de tipo para variáveis.

### <a name="about-using-statements-in-q"></a>Sobre as instruções `using` em Q#

A instrução `using` também é especial para o Q#. Ela é usada para alocar qubits para uso em um bloco de código. Em Q#, todos os qubits são alocados e liberados dinamicamente, em vez de serem recursos fixos que existem pelo tempo de vida inteiro de um algoritmo complexo. Uma instrução `using` aloca um conjunto de qubits no início e libera esses qubits no final do bloco.

## <a name="create-the-host-application-code"></a>Criar o código do aplicativo host

#### <a name="python"></a>[Python](#tab/tabid-python)

1. Abra o arquivo `host.py`e adicione o seguinte código:

    ```python
    import qsharp

    from qsharp import Result
    from Quantum.Bell import TestBellState

    initials = (Result.Zero, Result.One)

    for i in initials:
      res = TestBellState.simulate(count=1000, initial=i)
      (num_zeros, num_ones) = res
      print(f'Init:{i: <4} 0s={num_zeros: <4} 1s={num_ones: <4}')
    ```

#### <a name="c"></a>[C#](#tab/tabid-csharp)

1. Substitua o conteúdo do arquivo `Driver.cs` pelo seguinte código:

    ```csharp
    using System;

    using Microsoft.Quantum.Simulation.Core;
    using Microsoft.Quantum.Simulation.Simulators;

    namespace Quantum.Bell
    {
        class Driver
        {
            static void Main(string[] args)
            {
                using (var qsim = new QuantumSimulator())
                {
                    // Try initial values
                    Result[] initials = new Result[] { Result.Zero, Result.One };
                    foreach (Result initial in initials)
                    {
                        var res = TestBellState.Run(qsim, 1000, initial).Result;
                        var (numZeros, numOnes) = res;
                        System.Console.WriteLine(
                            $"Init:{initial,-4} 0s={numZeros,-4} 1s={numOnes,-4}");
                    }
                }

                System.Console.WriteLine("Press any key to continue...");
                Console.ReadKey();
            }
        }
    }
    ```

#### [](#tab/tabid-vs2019)

* * *

### <a name="about-the-host-application-code"></a>Sobre o código do aplicativo host

#### <a name="python"></a>[Python](#tab/tabid-python)

O aplicativo host do Python tem três partes:

* Calcula os argumentos necessários para o algoritmo quântico. No exemplo, `count` é corrigido em um 1.000 e `initial` é o valor inicial do qubit.
* Executa o algoritmo quântico chamando o método `simulate()` da operação Q# importada.
* Processa o resultado da operação. No exemplo, `res` recebe o resultado da operação. Aqui, o resultado é uma tupla do número de zeros (`num_zeros`) e do número de uns (`num_ones`) medidos pelo simulador. Desconstruiremos a tupla para obter os dois campos e imprimiremos os resultados.

#### <a name="c"></a>[C#](#tab/tabid-csharp)

O aplicativo host C# tem quatro partes:

* Constrói um simulador quântico. No exemplo, `qsim` é o simulador.
* Calcula os argumentos necessários para o algoritmo quântico. No exemplo, `count` é corrigido em um 1.000 e `initial` é o valor inicial do qubit.
* Executa o algoritmo quântico. Cada operação Q# gera uma classe C# com o mesmo nome. Essa classe tem um método `Run` que executa a operação de **maneira assíncrona**. A execução é assíncrona, porque a execução no hardware real será assíncrona. Como o método `Run` é assíncrono, efetuamos fetch da propriedade `Result`; isso bloqueia a execução até que a tarefa seja concluída e retorna o resultado de maneira síncrona.
* Processa o resultado da operação. No exemplo, `res` recebe o resultado da operação. Aqui, o resultado é uma tupla do número de zeros (`numZeros`) e do número de uns (`numOnes`) medidos pelo simulador. Isso é retornado como uma ValueTuple em C#. Desconstruiremos a tupla para obter os dois campos, imprimiremos os resultados e aguardaremos um pressionamento de tecla.

#### [](#tab/tabid-vs2019)

* * *

## <a name="build-and-run"></a>Criar e executar

#### <a name="python"></a>[Python](#tab/tabid-python)

1. Execute o seguinte comando no terminal:

    ```
    python host.py
    ```

    Esse comando executa o aplicativo host, que simula a operação Q#.

Os resultados devem ser:

```Output
Init:0    0s=1000 1s=0   
Init:1    0s=0    1s=1000
```

#### <a name="command-line--visual-studio-code"></a>[Linha de comando/Visual Studio Code](#tab/tabid-csharp)

1. Execute o seguinte no terminal:

    ```dotnetcli
    dotnet run
    ```

    Esse comando baixará automaticamente todos os pacotes necessários, compilará o aplicativo e, em seguida, o executará na linha de comando.

1. Como alternativa, pressione **F1** para abrir a paleta de comandos e selecione **Depurar: Iniciar sem Depuração.**
Talvez você precise criar um arquivo ``launch.json`` descrevendo como iniciar o programa.
O ``launch.json`` padrão deve funcionar bem para a maioria dos aplicativos.

Os resultados devem ser:

```Output
Init:Zero 0s=1000 1s=0
Init:One  0s=0    1s=1000
Press any key to continue...
```

#### <a name="visual-studio"></a>[Visual Studio](#tab/tabid-vs2019)

1. Basta clicar em `F5` e o programa deverá ser compilado e executado.

Os resultados devem ser:

```Output
Init:Zero 0s=1000 1s=0
Init:One  0s=0    1s=1000
Press any key to continue...
```

O programa será encerrado depois que você pressionar uma tecla.

* * *

## <a name="prepare-superposition"></a>Preparar a superposição

**Visão geral** Agora vamos examinar como o Q# expressa maneiras de colocar qubits em sobreposição.  Lembre-se de que o estado de um qubit pode estar em uma sobreposição de 0 e 1.  Usaremos a operação `Hadamard` para fazer isso. Se o qubit estiver em qualquer um dos estados clássicos (em que uma medição retorna `Zero` sempre ou `One` sempre), a operação `Hadamard` ou `H` colocará o qubit em um estado em que uma medição do qubit retornará `Zero` 50% do tempo e retornará `One` 50% do tempo.  Conceitualmente, o qubit pode ser pensado como a metade entre o `Zero` e o `One`.  Agora, quando simularmos a operação `TestBellState`, veremos que os resultados retornarão aproximadamente um número igual de `Zero` e `One` após a medição.  

Primeiro, tentaremos inverter o qubit (se o qubit estiver no `Zero`, o estado será invertido para `One` e vice-versa). Isso é feito com a execução de uma operação `X` antes de medi-lo em `TestBellState`:

```qsharp
X(qubit);
let res = M(qubit);
```

Agora os resultados (depois de pressionar `F5`) são invertidos:

```Output
Init:Zero 0s=0    1s=1000
Init:One  0s=1000 1s=0
```

No entanto, tudo o que vimos até agora é clássico. Vamos obter um resultado quântico. Basta substituir a operação `X` na execução anterior por uma operação `H` ou Hadamard. Em vez de inverteremos o qubit até o final de 0 a 1, só o inverteremos até a metade. As linhas substituídas em `TestBellState` agora têm a seguinte aparência:

```qsharp
H(qubit);
let res = M(qubit);
```

Agora os resultados ficam mais interessantes:

```Output
Init:Zero 0s=484  1s=516
Init:One  0s=522  1s=478
```

Sempre que medimos, pedimos um valor clássico, mas como o qubit está na metade entre 0 e 1, obtemos (estatisticamente) 0 na metade do tempo e 1 na metade do tempo. Isso é conhecido como __superposição__ e nos dá nossa primeira visão real de um estado quântico.

## <a name="prepare-entanglement"></a>Preparar o entrelaçamento

**Visão geral:**  Agora vamos examinar como o Q# expressa maneiras de entrelaçar qubits.  Primeiro, definimos o primeiro qubit como o estado inicial e usamos a operação `H` para colocá-lo em sobreposição.  Em seguida, antes de medirmos o primeiro qubit, usamos uma nova operação (`CNOT`), que significa Não-Controlada.  O resultado da execução dessa operação em dois qubits será inverter o segundo qubit se o primeiro qubit for `One`.  Agora, os dois qubits estão entrelaçados.  Nossas estatísticas para o primeiro qubit não mudaram (possibilidade de 50-50 de `Zero` ou `One` após a medição), mas agora, quando medimos o segundo qubit, ele é __sempre__ igual ao que medimos para o primeiro qubit. Nosso `CNOT` entrelaçou os dois qubits, de modo que o que acontecer com um deles acontecerá com o outro. Se você inverter as medidas (fizer o segundo qubit antes do primeiro), a mesma coisa acontecerá. A primeira medida será aleatória e a segunda estará na etapa de bloqueio com tudo o que foi descoberto para o primeiro.

A primeira coisa que precisaremos fazer é alocar dois qubits em vez de um em `TestBellState`:

```qsharp
using ((q0, q1) = (Qubit(), Qubit())) {
```

Isso nos permitirá adicionar uma nova operação (`CNOT`) antes de medir (`M`) em `TestBellState`:

```qsharp
Set(initial, q0);
Set(Zero, q1);

H(q0);
CNOT(q0, q1);
let res = M(q0);
```

Adicionamos outra operação `Set` para inicializar o primeiro qubit, a fim de garantir que ele esteja sempre no estado `Zero` quando começarmos.

Também precisamos redefinir o segundo qubit antes de liberá-lo.

```qsharp
Set(Zero, q0);
Set(Zero, q1);
```

A rotina completa agora tem esta aparência:

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                Set (initial, q0);
                Set (Zero, q1);

                H(q0);
                CNOT(q0,q1);
                let res = M(q0);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            
            Set(Zero, q0);
            Set(Zero, q1);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes);
    }
```

Se executarmos isso, obteremos exatamente o mesmo resultado 50-50 que obtivemos antes. No entanto, estamos interessados mesmo em como o segundo qubit reage ao primeiro que está sendo medido. Adicionaremos essa estatística com uma nova versão da operação `TestBellState`:

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int, Int) {
        mutable numOnes = 0;
        mutable agree = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                Set(initial, q0);
                Set(Zero, q1);

                H(q0);
                CNOT(q0, q1);
                let res = M(q0);

                if (M(q1) == res) {
                    set agree += 1;
                }

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            
            Set(Zero, q0);
            Set(Zero, q1);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes, agree);
    }
```

O novo valor retornado (`agree`) faz o acompanhamento toda vez que a medida do primeiro qubit corresponde à medida do segundo qubit. Também precisamos atualizar o aplicativo host de acordo:

#### <a name="python"></a>[Python](#tab/tabid-python)

```python
import qsharp

from qsharp import Result
from Quantum.Bell import TestBellState

initials = {Result.Zero, Result.One} 

for i in initials:
    res = TestBellState.simulate(count=1000, initial=i)
    (num_zeros, num_ones, agree) = res
    print(f'Init:{i: <4} 0s={num_zeros: <4} 1s={num_ones: <4} agree={agree: <4}')
```

#### <a name="c"></a>[C#](#tab/tabid-csharp)

```csharp
            using (var qsim = new QuantumSimulator())
            {
                // Try initial values
                Result[] initials = new Result[] { Result.Zero, Result.One };
                foreach (Result initial in initials)
                {
                    var res = TestBellState.Run(qsim, 1000, initial).Result;
                    var (numZeros, numOnes, agree) = res;
                    System.Console.WriteLine(
                        $"Init:{initial,-4} 0s={numZeros,-4} 1s={numOnes,-4} agree={agree,-4}");
                }
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
```

#### [](#tab/tabid-vs2019)

* * *

Agora, na execução, obtemos algo incrível:

```Output
Init:Zero 0s=499  1s=501  agree=1000
Init:One  0s=490  1s=510  agree=1000
```

Conforme indicado na visão geral, nossas estatísticas para o primeiro qubit não foram alteradas (possibilidade de 50-50 de 0 ou 1), mas agora, quando medimos o segundo qubit, ele é __sempre__ igual ao que medimos para o primeiro qubit, porque eles estão entrelaçados!

Parabéns, você escreveu seu primeiro programa quântico!

## <a name="next-steps"></a>Próximas etapas

O tutorial [Pesquisa de Grover](xref:microsoft.quantum.quickstarts.search) mostrará como criar e executar a pesquisa de Grover, um dos algoritmos mais populares da computação quântica, além de apresentar um bom exemplo de programa Q# que pode ser usado para resolver problemas reais com a computação quântica.  

A [Introdução ao Quantum Development Kit](xref:microsoft.quantum.welcome) recomenda mais maneiras de aprender o Q# e a programação quântica.
