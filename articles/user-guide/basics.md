---
title: 'Noções básicas do Q #'
description: 'Conceitos básicos de p #'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 02/28/2020
ms.topic: article
uid: microsoft.quantum.guide.basics
ms.openlocfilehash: 45e6f2f33dafc2aec177091d3cfa94aca14fbf0a
ms.sourcegitcommit: af10179284967bd7a72a52ae7e1c4da65c7d128d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "85415347"
---
# <a name="q-basics"></a>Noções básicas do Q #

Este artigo apresenta uma breve introdução aos blocos de construção básicos de Q #.

Para obter uma visão geral do Q # e onde ele se encaixa como um componente fundamental do kit de desenvolvimento Quantum, consulte [o que é Q #?](xref:microsoft.quantum.overview.q-sharp). 

## <a name="what-is-a-quantum-program"></a>O que é um programa Quantum?

Do ponto de vista técnico, um programa Quantum é um conjunto específico de sub-rotinas clássicas que, quando chamados, executam determinadas operações em um sistema Quantum.
Uma consequência importante dessa exibição é que um programa Q # não modele diretamente o qubits, mas, em vez disso, descreve como um computador com controle clássico interage com esses qubits.
Por design, Q # não define os Estados Quantum ou outras propriedades da mecânica quantum diretamente.
Por exemplo, considere o estado $ \ket{+} = \left (\ket {0} + \ket {1} \right)/\sqrt {2} $ discutido no guia de [conceitos da computação Quantum](xref:microsoft.quantum.concepts.intro) .
Para preparar esse estado em Q #, comece com os fatos que os qubits são inicializados no estado $ \ket {0} $ e que $ \ket{+} = H\ket {0} $, em que $H $ é a [transformação Hadamard](xref:microsoft.quantum.glossary#hadamard), implementada pela [ `H` operação](xref:microsoft.quantum.intrinsic.h). O código Basic Q # para inicializar e transformar um qubit, assim, tem a seguinte aparência:

```qsharp
using (qubit = Qubit()) {
    // At this point, the qubit is in the state |0⟩.
    H(qubit);
    // H is now applied, such that the qubit is in H|0⟩ = |+⟩, as desired.
}
```
Para obter mais informações sobre como inicializar, ou *alocar*, qubits, consulte [trabalhando com qubits](xref:microsoft.quantum.guide.qubits).

## <a name="quantum-states-in-q"></a>Estados da Quantum em Q #

O mais importante é que o programa anterior não se refere explicitamente ao estado em Q #, mas descreveu como nosso programa *transformou* o estado.
Com essa abordagem, você pode ser totalmente independente do que um estado Quantum ainda *está* em cada computador de destino, que pode ter interpretações diferentes dependendo do computador. 

Um programa Q # não pode introspecção no estado de um qubit.
Em vez disso, um programa pode chamar operações como [`Measure`](xref:microsoft.quantum.intrinsic.measure) para aprender informações de um qubit e chamar operações como [`X`](xref:microsoft.quantum.intrinsic.x) e [`H`](xref:microsoft.quantum.intrinsic.h) para agir no estado de um qubit.
O que essas operações realmente *fazem* é apenas concreto pelo computador de destino usado para executar o programa Q # específico.
Por exemplo, se estiver executando o programa em nosso [simulador de estado completo](xref:microsoft.quantum.machines.full-state-simulator), o simulador executará as operações matemáticas correspondentes para o sistema Quantum simulado.
Mas olhando para o futuro, quando o computador de destino é um computador Quantum real, chamar tais operações em Q # direciona o computador Quantum para executar as operações *reais* correspondentes no sistema Quantum *real* , por exemplo, pulsos de laser com precisamente tempo.

Um programa Q # recombina essas operações conforme definido por um computador de destino para criar operações novas e de nível mais alto para a computação da Quantum Express.
Dessa forma, Q # torna fácil expressar os algoritmos Quantum subjacente e Quantum híbrido-clássico, além de ser geral em relação à estrutura de um computador de destino ou simulador.

## <a name="q-operations-and-functions"></a>Operações e funções do Q #

Concretamente, um programa Q # compreende *operações*, *funções*e qualquer tipo definido pelo usuário. 

As operações são usadas para descrever as transformações de sistemas Quantum e são o bloco de construção mais fundamental de programas do Q #. Cada operação definida em Q # pode então chamar qualquer número de outras operações.

Em contraste com as operações, as funções são usadas para descrever o comportamento clássico puramente *determinístico* e não têm efeitos além da computação de valores clássicos. Por exemplo, suponha que você queira medir o qubits no final de um programa e adicionar os resultados de medida a uma matriz.
Nesse caso, `Measure` é uma *operação* que instrui o computador de destino a executar uma medida no qubits (real ou simulado). Ao mesmo tempo, o *Functions* lida com o processo clássico de adicionar os resultados retornados a uma matriz.

Juntas, operações e funções são conhecidas como *callables*. A estrutura subjacente e o comportamento são introduzidos e detalhados em [operações e funções em Q #](xref:microsoft.quantum.guide.operationsfunctions).


## <a name="q-syntax-overview"></a>Visão geral da sintaxe de Q #

A sintaxe de uma linguagem descreve as diferentes combinações de símbolos que formam um programa sintaticamente correto.
Em Q #, os elementos de sintaxe são classificados em três grupos diferentes: tipos, expressões e instruções.

### <a name="types"></a>Tipos
Q # é uma linguagem fortemente tipada, de modo que o uso cuidadoso dos tipos pode ajudar o compilador a fornecer fortes garantias sobre programas do Q # no momento da compilação.
Além dos tipos primitivos internos padrão e específicos do Quantum, por exemplo,,, `Int` `Bool` `Qubit` e `Result` , Q # fornece suporte para tipos definidos pelo usuário.

Para obter descrições de todos os tipos primitivos, detalhes para tipos de matriz e tupla e etapas para definir novos tipos em um arquivo Q #, consulte [tipos em Q #](xref:microsoft.quantum.guide.types).

### <a name="expressions"></a>Expressões
Uma expressão em uma linguagem de programação é uma combinação de uma ou mais constantes, variáveis, operadores e funções que a linguagem de programação interpreta e avalia como um valor específico.
Mais simples, para cada tipo em um idioma, as expressões desse tipo podem ser *literais* ou símbolos associados a um valor desse tipo.
Por exemplo, `5` é um `Int` literal (portanto, também uma expressão do tipo `Int` ) e, se o símbolo `count` estiver associado ao valor inteiro `5` , `count` também será uma expressão de número inteiro.

Além disso, uma expressão pode consistir em outras expressões combinadas por determinados operadores.
Por exemplo, outra `Int` expressão que é avaliada como `5` é `2+3` .

Para obter mais informações sobre expressões e operadores compatíveis em Q #, consulte [expressões de tipo em q #](xref:microsoft.quantum.guide.expressions). 

### <a name="statements"></a>Instruções 
Uma instrução é uma unidade sintática de uma linguagem de programação imperativa que expressa algumas ações a serem executadas. As instruções contrastam com expressões nessas instruções não retornam resultados e são executadas exclusivamente para seus efeitos colaterais. No entanto, as expressões sempre retornam um resultado e, muitas vezes, não têm efeitos colaterais. Em suma, as instruções Q # são executadas, enquanto as expressões são avaliadas.

Um exemplo simples de uma instrução em Q # é atribuir um símbolo a uma expressão:
```qsharp
let count = 5;
```

Um exemplo mais interessante é a `for` instrução que dá suporte à iteração e inclui um *bloco de instruções*.
Suponha que `qubits` o símbolo seja associado a um registro de qubits (tecnicamente do tipo `Qubit[]` , ou uma matriz de `Qubit` tipos). Então
```qsharp
for (qubit in qubits) {
    H(qubit);
}
```
é uma instrução que itera em cada qubit no registro, executando a `H` operação em cada uma delas. Observe que `H(qubit);` também é uma instrução em si.

Você pode usar qualquer expressão de chamada do tipo `Unit` (um `Unit` tipo não retorna nenhuma informação) como uma instrução.
Esse tipo de expressão é útil ao chamar operações em qubits que retornam `Unit` porque a finalidade da instrução é modificar o estado de Quantum implícito.
As instruções de avaliação de expressão exigem um ponto e vírgula de terminação.

Você usa instruções para criar quase todos os aspectos de um programa Q #, e nenhuma página única pode abranger todas as informações relacionadas a eles.
Para obter mais informações sobre sua estrutura lexical e formatação, consulte a [estrutura de arquivos de Q #](xref:microsoft.quantum.guide.filestructure); para atribuição e escopo de associação de símbolo, consulte [variáveis em Q #](xref:microsoft.quantum.guide.variables); e para loops de fluxo de controle, como `for` , consulte [fluxo de controle em Q #](xref:microsoft.quantum.guide.controlflow).

## <a name="next-steps"></a>Próximas etapas

Comece a aprender sobre os [tipos em Q #](xref:microsoft.quantum.guide.types).

Para obter mais informações sobre as bases e a motivação por trás de Q #, consulte [por que precisamos de q #?](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/).
