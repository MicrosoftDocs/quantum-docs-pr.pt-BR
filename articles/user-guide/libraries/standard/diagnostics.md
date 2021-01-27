---
title: Diagnóstico nas Q# bibliotecas padrão
description: Saiba mais sobre as funções de diagnóstico e as operações nas Q# bibliotecas padrão usadas para capturar erros ou erros em programas Quantum.
author: cgranade
uid: microsoft.quantum.libraries.diagnostics
ms.author: chgranad
ms.topic: conceptual
no-loc:
- Q#
- $$v
ms.openlocfilehash: d13122187a24893d297cfdbb3ad4db03eb22ded0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858692"
---
# <a name="diagnostics"></a>Diagnósticos #

Assim como no desenvolvimento clássico, é importante poder diagnosticar erros e erros em programas Quantum.
As Q# bibliotecas padrão fornecem várias maneiras diferentes de garantir a exatidão dos programas Quantum, conforme detalhado em <xref:microsoft.quantum.guide.testingdebugging> .
Em grande parte, esse suporte é fornecido na forma de funções e operações que instruem o computador de destino a fornecer informações adicionais de diagnóstico para o programa ou desenvolvedor do host, ou impõem a exatidão das condições e invariáveis expressas pela função ou pela chamada de operação.

## <a name="machine-diagnostics"></a>Diagnóstico de máquina ##

O diagnóstico sobre valores clássicos pode ser obtido usando a <xref:Microsoft.Quantum.Intrinsic.Message> função para registrar uma mensagem de forma dependente do computador.
Por padrão, isso grava a cadeia de caracteres no console.
Usado junto com cadeias de caracteres interpoladas, <xref:Microsoft.Quantum.Intrinsic.Message> facilita o relatório de informações de diagnóstico sobre valores clássicos:

```qsharp
let angle = Microsoft.Quantum.Math.PI() * 2.0 / 3.0;
Message($"About to rotate by an angle of {angle}...");
```

> [!NOTE]
> `Message` tem assinatura `(String -> Unit)` , representando novamente que a emissão de uma mensagem de log de depuração não pode ser observada de dentro do Q# .

O <xref:Microsoft.Quantum.Diagnostics.DumpMachine> e o <xref:Microsoft.Quantum.Diagnostics.DumpRegister> callables instruem os computadores de destino a fornecer informações de diagnóstico sobre todos os qubits atualmente alocados ou sobre um registro específico do qubits, respectivamente.
Cada computador de destino varia de acordo com as informações de diagnóstico fornecidas em resposta a uma instrução de despejo.
A máquina de destino do [simulador de estado completo](xref:microsoft.quantum.machines.full-state-simulator) , por exemplo, fornece o programa de host com o vetor de estado que ele usa internamente para representar um registro de qubits.
Por comparação, a máquina de destino do [Toffoli Simulator](xref:microsoft.quantum.machines.toffoli-simulator) fornece um único bit clássico para cada qubit.

 Para saber mais sobre a saída [do simulador de estado completo](xref:microsoft.quantum.machines.full-state-simulator) `DumpMachine` , dê uma olhada na seção de funções de despejo do nosso [artigo de teste e depuração](xref:microsoft.quantum.guide.testingdebugging#dump-functions).


## <a name="facts-and-assertions"></a>Fatos e asserções ##

Conforme discutido em [teste e depuração](xref:microsoft.quantum.guide.testingdebugging), uma função ou operação com assinatura `Unit -> Unit` ou `Unit => Unit` , respectivamente, pode ser marcada como um *teste de unidade*.
Cada teste de unidade geralmente consiste em um pequeno programa Quantum, juntamente com uma ou mais condições que verificam a exatidão desse programa.
Essas condições podem vir na forma de _fatos_, que verificam os valores de suas entradas ou _asserções_, que verificam os Estados de um ou mais qubits passados como entrada.

Por exemplo, `EqualityFactI(1 + 1, 2, "1 + 1 != 2")` representa o fato matemático que $1 + 1 = $2, enquanto `AssertQubit(One, qubit)` representa a condição que a medição `qubit` retornará um `One` com certeza.
No primeiro caso, podemos verificar a exatidão da condição, dado apenas seus valores, enquanto, no último, devemos saber algo sobre o estado do qubit para avaliar a asserção.

As Q# bibliotecas padrão fornecem várias funções diferentes para representar fatos, incluindo:

- <xref:Microsoft.Quantum.Diagnostics.Fact>
- <xref:Microsoft.Quantum.Diagnostics.EqualityWithinToleranceFact>
- <xref:Microsoft.Quantum.Diagnostics.NearEqualityFactC>
- <xref:Microsoft.Quantum.Diagnostics.EqualityFactI>


### <a name="testing-qubit-states"></a>Testando Estados de qubit ###

Na prática, as asserções dependem do fato de que as simulações clássicas da mecânica quantum não precisam obedecer à [teorema no-Cloning](https://arxiv.org/abs/quant-ph/9607018), de modo que podemos fazer medidas e asserções não físicas ao usar um simulador para o nosso computador de destino.
Portanto, podemos testar operações individuais em um simulador clássico antes de implantar em hardware.
Em computadores de destino que não permitem a avaliação de asserções, as chamadas para <xref:Microsoft.Quantum.Diagnostics.AssertMeasurement> podem ser ignoradas com segurança.

Em geral, a <xref:Microsoft.Quantum.Diagnostics.AssertMeasurement> operação declara que medir o qubits fornecido na base Pauli especificada sempre terá o resultado especificado.
Se a asserção falhar, a execução terminará chamando `fail` com a mensagem fornecida.
Por padrão, essa operação não é implementada; os simuladores que podem oferecer suporte a ele devem fornecer uma implementação que executa a verificação de tempo de execução.
`AssertMeasurement` tem assinatura `((Pauli[], Qubit[], Result, String) -> ())` .
Como `AssertMeasurement` é uma função com uma tupla vazia como seu tipo de saída, nenhum efeito de tendo chamado `AssertMeasurement` é observável em um Q# programa.

A <xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> função de operação Asserts que medindo o determinado qubits na base de Pauli especificada terá o resultado fornecido com a probabilidade determinada, dentro de certa tolerância.
A tolerância é aditiva (por exemplo, `abs(expected-actual) < tol` ).
Se a asserção falhar, a execução terminará chamando `fail` com a mensagem fornecida.
Por padrão, essa operação não é implementada; os simuladores que podem oferecer suporte a ele devem fornecer uma implementação que executa a verificação de tempo de execução.
`AssertMeasurementProbability` tem assinatura `((Pauli[], Qubit[], Result, Double, String, Double) -> Unit)` . O primeiro dos `Double` parâmetros fornece a probabilidade desejada do resultado e o segundo a tolerância.

Podemos fazer mais do que declarar uma única medida, usando que as informações clássicas usadas por um simulador para representar o estado interno de um qubit é receptivos para copiar, de modo que não precisamos realmente executar uma medida para testar nossa declaração.
Em particular, isso nos permite motivos sobre medidas *incompatíveis* que seriam impossíveis em hardware real.

Suponha que `P : Qubit => Unit` seja uma operação destinada a preparar o estado $ \ket{\psi} $ quando sua entrada estiver no estado $ \ket {0} $.
Deixe que $ \ket{\psi '} $ seja o estado real preparado pelo `P` .
Em seguida, $ \ket{\psi} = \ket{\psi '} $ If e only se medindo $ \ket{\psi '} $ no eixo descrito por $ \ket{\psi} $ sempre retorna `Zero` .
Ou seja, \begin{align} \ket{\psi} = \ket{\psi '} \Text{If e only if} \braket{\psi | \psi '} = 1.
\end{align} usando as operações primitivas definidas no prelúdio, podemos executar diretamente uma medida que retorna `Zero` se $ \ket{\psi} $ for um eigenstate de um dos operadores Pauli.


A operação <xref:Microsoft.Quantum.Diagnostics.AssertQubit> fornece uma abreviação particularmente útil para fazer isso no caso em que desejarmos testar a asserção $ \ket{\psi} = \ket {0} $.
Isso é comum, por exemplo, quando não computamos para retornar ancilla qubits a $ \ket {0} $ antes de liberá-los.
A declaração em relação a $ \ket {0} $ também é útil quando desejamos declarar que as operações de preparação de dois Estados preparam `P` `Q` o mesmo estado e quando o `Q` dá suporte ao `Adjoint` .
Em particular,

```qsharp
using (register = Qubit()) {
    P(register);
    Adjoint Q(register);

    AssertQubit(Zero, register);
}
```

No entanto, em geral, talvez não tenhamos acesso a asserções sobre Estados que não coincidem com eigenstates de operadores Pauli.
Por exemplo, $ \ket{\psi} = (\ket {0} + e ^ {i \pi/8} \ket {1} )/\sqrt {2} $ não é um eigenstate de nenhum operador Pauli, de modo que não podemos usar <xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> para determinar exclusivamente que um estado $ \ket{\psi '} $ é igual a $ \ket{\psi} $.
Em vez disso, devemos decompor a asserção $ \ket{\psi '} = \ket{\psi} $ em suposições que podem ser diretamente testadas usando os primitivos suportados pelo nosso simulador.
Para fazer isso, deixe $ \ket{\psi} = \alpha \ket {0} + \beta \ket {1} $ para números complexos $ \alpha = \_ r + a \_ i $ e $ \beta $.
Observe que essa expressão requer quatro números reais \{ de $ a \_ r, a \_ i, b \_ r, b \_ i \} $ para especificar, pois cada número complexo pode ser expresso como a soma de uma parte real e imaginário.
No entanto, devido à fase global, podemos escolher $a \_ i = $0, de modo que precisamos apenas de três números reais para especificar exclusivamente um estado de qubit único.

Portanto, precisamos especificar três asserções que são independentes umas das outras para declarar o estado esperado.
Fazemos isso encontrando a probabilidade de observar `Zero` cada medição de Pauli, considerando $ \alpha $ e $ \beta $, e declarando cada uma independentemente.
Deixe $x $, $y $ e $z $ sejam `Result` valores para Pauli $X $, $Y $ e $Z $ medições, respectivamente.
Em seguida, usando a função probabilidade para medições Quantum, \begin{align} \Pr (x = \texttt{Zero} | \alpha, \beta) & = \frac12 + a \_ r b \_ r + a \_ i b \_ i \\ \\ \Pr (y = \texttt{Zero} | \alpha, \beta) & = \frac12 + a \_ r b \_ i-a \_ i b \_ r \\ \\ \Pr (z = \texttt{zero} | \alpha, \beta) & = \frac12\left (1 + a \_ r ^ 2 + a \_ i ^ 2 + b \_ r ^ 2 + b \_ i ^ 2 \right).
\end{align}

A <xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance> operação implementa essas asserções dadas as representações de $ \alpha $ e $ \beta $ como valores do tipo <xref:Microsoft.Quantum.Math.Complex> .
Isso é útil quando o estado esperado pode ser calculado matematicamente.

### <a name="asserting-equality-of-quantum-operations"></a>Declarando a igualdade de operações Quantum ###

Até agora, estamos preocupados com as operações de teste que destinam-se a preparar Estados específicos.
No entanto, muitas vezes estamos interessados em como uma operação atua para entradas arbitrárias em vez de uma única entrada fixa.
Por exemplo, suponha que implementamos uma operação `U : ((Double, Qubit[]) => () : Adjoint)` correspondente a uma família de operadores unitários $U (t) $ e fornecemos um `adjoint` bloco explícito em vez de usar `adjoint auto` .
Talvez esteja interessado em afirmar que $U ^ \dagger (t) = U (-t) $, conforme esperado se $t $ representa um tempo de evolução.

Em geral, há duas estratégias diferentes que podemos seguir para fazer a asserção de que duas operações `U` e agir de forma `V` idêntica.
Primeiro, podemos verificar se `U(target); (Adjoint V)(target);` preserva cada Estado em uma determinada base.
Em segundo lugar, podemos verificar que `U(target); (Adjoint V)(target);` agir na metade de um estado confusas preserva esse Entanglement.
Essas estratégias são implementadas pelas operações de Canon <xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlace> e <xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced> , respectivamente.

> [!NOTE]
> A declaração referenciada mencionada acima funciona com base no [Choi – Jamiłkowski isomorphism](https://en.wikipedia.org/wiki/Channel-state_duality), uma estrutura matemática que relaciona as operações em $n $ qubits a confusas Estados em $2n $ qubits.
> Em particular, a operação de identidade em $n $ qubits é representada por $n as cópias do estado confusas $ \ket{\ beta_ {00} } \mathrel{: =} (\ket {00} + \ket {11} )/\sqrt {2} $.
> A operação <xref:Microsoft.Quantum.Preparation.PrepareChoiState> implementa esse isomorphism, preparando um estado que representa uma determinada operação.

Aproximadamente, essas estratégias são diferenciadas por uma compensação de espaço em tempo.
A iteração em cada Estado de entrada leva mais tempo, ao passo que o uso de Entanglement como referência requer o armazenamento de qubits adicionais.
Nos casos em que uma operação implementa uma operação clássica reversível, de modo que estamos interessados apenas em seu comportamento nos Estados de base computacional, <xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlaceCompBasis> testa a igualdade nesse conjunto restrito de entradas.

> [!TIP]
> A iteração sobre Estados de entrada é tratada pelas operações de enumeração <xref:Microsoft.Quantum.Canon.IterateThroughCartesianProduct> e <xref:Microsoft.Quantum.Canon.IterateThroughCartesianPower> .
> Essas operações são úteis mais geralmente para aplicar uma operação a cada elemento do produto cartesiano entre dois ou mais conjuntos.

Mais importante, no entanto, as duas abordagens testam diferentes propriedades das operações em exame.
Como a declaração in-loco chama cada operação várias vezes, uma vez para cada Estado de entrada, quaisquer escolhas aleatórias e resultados de medidas podem ser alterados entre as chamadas.
Por outro lado, a declaração referenciada chama cada operação exatamente uma vez, de modo que ela verifica se as operações são iguais *em uma única captura*.
Esses dois testes são úteis para garantir a exatidão dos programas Quantum.


## <a name="further-reading"></a>Leitura Adicional ##

- <xref:microsoft.quantum.guide.testingdebugging>
- <xref:Microsoft.Quantum.Diagnostics>
