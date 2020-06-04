---
title: 'Noções básicas do Q #'
description: 'Conceitos básicos de p #'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 02/28/2020
ms.topic: article
uid: microsoft.quantum.guide.basics
ms.openlocfilehash: e77b52d1a6eb7e2f62ab12dedd75d00ac8fec4be
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327315"
---
# <a name="q-basics"></a>Noções básicas do Q #

Nesta seção, apresentamos uma breve introdução aos blocos de construção básicos de Q #.

Para obter uma visão geral rápida do que é o Q # e onde ele se encaixa como um componente fundamental do kit de desenvolvimento Quantum, você pode conferir [o que é Q #?](xref:microsoft.quantum.overview.q-sharp). 

## <a name="what-is-a-quantum-program"></a>O que é um programa Quantum?

Do ponto de vista técnico, um programa Quantum pode ser visto como um conjunto específico de sub-rotinas clássicas que, quando chamados, executam determinadas operações em um sistema Quantum.
Uma consequência importante dessa exibição é que um programa escrito em Q # não modele diretamente o qubits em si, mas descreve como um computador de controle clássico interage com esses qubits.
Por design, p #, portanto, não define os Estados Quantum ou outras propriedades da mecânica quantum diretamente.
Por exemplo, considere o estado $ \ket{+} = \left (\ket {0} + \ket {1} \right)/\sqrt {2} $ discutido no guia de [conceitos da computação Quantum](xref:microsoft.quantum.concepts.intro) .
Para preparar esse estado em Q #, usamos os fatos que os qubits são inicializados no estado $ \ket {0} $ e que $ \ket{+} = H\ket {0} $, em que $H $ é a transformação Hadamard, implementada pelo [ `H` Operation] (] (xref: Microsoft. Quantum. intrínseca. H):

```qsharp
using (qubit = Qubit()) {
    // At this point, qubit is in the state |0⟩.
    H(qubit);
    // We've now applied H, such that our qubit is in H|0⟩ = |+⟩, as we wanted.
}
```

## <a name="quantum-states-in-q"></a>Estados da Quantum em Q #

O mais importante é que, ao escrever o programa acima, não nos referimos explicitamente ao estado em Q #, mas, em vez disso, descrevemos como o estado foi *transformado* por nosso programa.
Isso nos permite ser totalmente independente do que um estado Quantum ainda *está* em cada computador de destino, que pode ter interpretações diferentes dependendo do computador. 

Um programa Q # não tem a capacidade de introspecção no estado de um qubit.
Em vez disso, um programa pode chamar operações como [`Measure`](xref:microsoft.quantum.intrinsic.measure) para aprender informações de um qubit e chamar operações como [`X`](xref:microsoft.quantum.intrinsic.x) e [`H`](xref:microsoft.quantum.intrinsic.h) para agir no estado de um qubit.
O que essas operações realmente *fazem* é apenas concreto pelo computador de destino que usamos para executar o programa Q # específico.
Por exemplo, se você estiver executando o programa em nosso [simulador de estado completo](xref:microsoft.quantum.machines.full-state-simulator), o simulador executará as operações matemáticas correspondentes para o sistema Quantum simulado.
Mas olhando para o futuro, quando o computador de destino for um computador Quantum real, chamar tais operações em Q # direcionará o computador Quantum para executar as operações *reais* correspondentes no sistema Quantum *real* (por exemplo, os pulsos de laser com precisão de tempo).

Um programa Q # recombina essas operações conforme definido por um computador de destino para criar operações novas e de nível mais alto para a computação da Quantum Express.
Dessa forma, Q # torna fácil expressar os algoritmos Quantum subjacente e Quantum híbrido-clássico, além de ser geral em relação à estrutura de um computador de destino ou simulador.

## <a name="q-operations-and-functions"></a>Operações e funções do Q #

Concretamente, um programa Q # é composto de *operações*, *funções*e qualquer tipo definido pelo usuário. 

As operações são usadas para descrever as transformações de sistemas Quantum e são o bloco de construção mais básico de programas do Q #. Cada operação definida em Q # pode então chamar qualquer número de outras operações.

Em contraste com as operações, as funções são usadas para descrever o comportamento clássico puramente *determinístico* e não têm efeitos além da computação de valores clássicos. Por exemplo, suponha que gostaríamos de medir nosso qubits no final de um programa e adicionar os resultados da medida a uma matriz.
Nesse caso `Measure` , é uma *operação* que instrui o computador de destino a executar uma medida no qubits (real ou simulado) e o processo clássico de adicionar os resultados retornados a uma matriz será manipulado por *funções*.

Juntos, as operações e funções são chamadas de *callables*, e sua estrutura subjacente e comportamento é introduzido nas [operações e funções na página de Q #](xref:microsoft.quantum.guide.operationsfunctions) .


## <a name="q-syntax-overview"></a>Visão geral da sintaxe de Q #

A sintaxe de uma linguagem descreve as diferentes combinações de símbolos que formam um programa sintaticamente correto.
Em Q #, podemos classificar os elementos de sua sintaxe em três grupos diferentes: tipos, expressões e instruções.

### <a name="types"></a>Tipos
Q # é uma linguagem fortemente tipada, de modo que o uso cuidadoso dos tipos pode ajudar o compilador a fornecer fortes garantias sobre programas do Q # no momento da compilação.
Além dos tipos primitivos internos padrão e específicos do Quantum (por exemplo,, `Int` , `Bool` `Qubit` e `Result` ), o Q # fornece suporte para tipos definidos pelo usuário.
Todos os vários tipos primitivos de Q # são descritos nos [tipos na página Q #](xref:microsoft.quantum.guide.types) , juntamente com detalhes sobre tipos de matriz e tupla, além de como definir novos tipos dentro de um arquivo Q #.

### <a name="expressions"></a>Expressões
Uma expressão em uma linguagem de programação é uma combinação de uma ou mais constantes, variáveis, operadores e funções que a linguagem de programação interpreta e avalia como um valor específico.
Mais simples, para cada tipo em um idioma, as expressões desse tipo podem ser *literais* ou símbolos associados a um valor desse tipo.
Por exemplo, `5` é um `Int` literal (portanto, também uma expressão do tipo `Int` ) e, se o símbolo `count` estiver associado ao valor inteiro `5` , `count` também será uma expressão de número inteiro.

Além disso, uma expressão pode consistir em outras expressões combinadas com determinados operadores.
Portanto, outro exemplo de uma `Int` expressão que é avaliada como `5` é `2+3` .

As possíveis expressões de tipos em Q #, bem como os operadores compatíveis que podem ser usados para formá-los, são detalhadas nas [expressões de tipo na página de Q #](xref:microsoft.quantum.guide.expressions) . 

### <a name="statements"></a>Instruções 
Uma instrução é uma unidade sintática de uma linguagem de programação imperativa que expressa alguma ação a ser executada. As instruções contrastam com expressões nessas instruções não retornam resultados e são executadas exclusivamente para seus efeitos colaterais, enquanto as expressões sempre retornam um resultado e, muitas vezes, não têm efeitos colaterais.
Essa distinção é frequentemente observada no texto: uma expressão é avaliada, enquanto uma instrução é executada.

Um exemplo muito básico de uma instrução em Q # é atribuir um símbolo a uma expressão:
```qsharp
let count = 5;
```

Um exemplo um pouco mais interessante é a `for` instrução que dá suporte à iteração e inclui um *bloco de instruções*.
Suponha que `qubits` o símbolo seja associado a um registro de qubits (tecnicamente do tipo `Qubit[]` , ou seja, uma matriz de `Qubit` tipos). Então
```qsharp
for (qubit in qubits) {
    H(qubit);
}
```
é uma instrução que itera em cada qubit no registro, executando a `H` operação em cada um. Observe que `H(qubit);` também é uma instrução em si.

Na verdade, qualquer expressão de chamada do tipo `Unit` (aqueles que não retornam nenhuma informação) pode ser usada como uma instrução.
Isso é basicamente usado ao chamar operações em qubits que retornam `Unit` porque a finalidade da instrução é modificar o estado de Quantum implícito.
As instruções de avaliação de expressão exigem um ponto e vírgula de terminação.

Quase todos os aspectos de um programa Q # são criados usando instruções, portanto, nenhuma única página pode abranger todas as informações relacionadas a elas.
No entanto, sua estrutura lexical e formatação são descritas na página [estrutura de arquivo Q #](xref:microsoft.quantum.guide.filestructure) , atribuição de associação de símbolo e escopo em [variáveis em q #](xref:microsoft.quantum.guide.variables)e loops de fluxo de controle, como `for` no [fluxo de controle em Q #](xref:microsoft.quantum.guide.controlflow).

## <a name="next-steps"></a>Próximas etapas
No restante deste guia, mostraremos como usar o Q # para construir programas Quantum complexos por meio dos blocos de construção básicos de operações, funções e tipos.

Para começar, você pode começar a aprender sobre os [tipos em Q #](xref:microsoft.quantum.guide.types).

Se você estiver interessado em aprender mais sobre as bases e a motivação por trás de Q #, confira [por que precisamos de q #?](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/).
