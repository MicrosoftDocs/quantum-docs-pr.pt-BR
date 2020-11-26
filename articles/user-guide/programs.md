---
title: 'Q # introdution'
description: 'Introdução rápida aos programas Quantum em p #'
author: beheim
ms.author: beheim
ms.date: 11/08/2020
ms.topic: article
uid: microsoft.quantum.guide.programs
ms.openlocfilehash: 975bcda5e0042406b465a83f17f1d2d3f5a1ec4f
ms.sourcegitcommit: b930bb59a1ba8f41d2edc9ed98197109aa8c7f1b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96233113"
---
# <a name="q-quantum-programming-language"></a>Linguagem de programação da Quantum Q #

Tudo o que você precisa saber sobre a linguagem de programação Q # é detalhado no [Guia de linguagem do q #](xref:microsoft.quantum.qsharp.index). Como qualquer outra coisa, nosso [processo de design de linguagem](https://github.com/microsoft/qsharp-language#q-language-and-core-libraries-design) é software livre e as contribuições são bem-vindas.
Para obter mais informações sobre as bases e a motivação por trás de Q #, consulte [por que precisamos de q #?](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/).  
O Q # é fornecido como parte do kit de desenvolvimento Quantum (QDK) para uma visão geral rápida, confira [o que é o QDK?](xref:microsoft.quantum.overview.q-sharp). 

## <a name="what-is-a-quantum-program"></a>O que é um programa Quantum?

Um programa Quantum pode ser visto como um conjunto específico de sub-rotinas clássicas que, quando chamado, executam uma computação interagindo com um sistema Quantum; um programa escrito em Q # não modele diretamente o estado Quantum, mas descreve como um computador de controle clássico interage com o qubits.
Isso nos permite ser totalmente independente do que um estado Quantum ainda *está* em cada computador de destino, que pode ter interpretações diferentes dependendo do computador. 

Uma consequência importante disso é que Q # não tem a capacidade de introspecção no estado de um qubit ou outras propriedades da mecânica quantum diretamente, o que garante que um programa Q # possa ser fisicamente executado em um computador Quantum.
Em vez disso, um programa pode chamar operações como [`Measure`](xref:Microsoft.Quantum.Intrinsic.Measure) para extrair informações clássicas de um qubit.

Uma vez alocados, um qubit pode ser passado para operações e funções, também conhecido como *callables*. De certa forma, isso é tudo o que um programa Q # pode fazer com um qubit; Todas as ações diretas no estado de um qubit são definidas por chamadores *intrínsecos* , como [`X`](xref:Microsoft.Quantum.Intrinsic.X) and [`H`](xref:Microsoft.Quantum.Intrinsic.H) -ex. callables, cujas implementações não são definidas em Q #, mas, em vez disso, são definidas pelo computador de destino. O que essas operações realmente *fazem* é apenas concreto pelo computador de destino que usamos para executar o programa Q # específico.

Por exemplo, se estiver executando o programa em nosso [simulador de estado completo](xref:microsoft.quantum.machines.full-state-simulator), o simulador executará as operações matemáticas correspondentes para o sistema Quantum simulado.
Mas olhando para o futuro, quando o computador de destino for um computador Quantum real, chamar tais operações em Q # direcionará o computador Quantum para executar as operações *reais* correspondentes no sistema Quantum *real* (por exemplo, os pulsos de laser com precisão de tempo).

Um programa Q # recombina essas operações conforme definido por um computador de destino para criar operações novas e de nível mais alto para a computação da Quantum Express.
Dessa forma, Q # torna fácil expressar os algoritmos Quantum subjacente e Quantum híbrido-clássico, além de ser geral em relação à estrutura de um computador de destino ou simulador.

Um exemplo simples é o seguinte programa, que aloca um qubit no estado $ \ket {0} $, depois aplica uma operação Hadamard `H` a ele e mede o resultado na `PauliZ` base.

```qsharp
@EntryPoint()
operation MeasureOneQubit() : Result {
    // The following using block creates a fresh qubit and initializes it
    // in the |0〉 state.
    using (qubit = Qubit()) {
        // We apply a Hadamard operation H to the state, thereby preparing the
        // state 1 / sqrt(2) (|0〉 + |1〉).
        H(qubit);
        // Now we measure the qubit in Z-basis.
        let result = M(qubit);
        // As the qubit is now in an eigenstate of the measurement operator,
        // we reset the qubit before releasing it.
        if (result == One) { X(qubit); }
        // Finally, we return the result of the measurement.
        return result;
    }
}
```

Nosso [katas Quantum](https://github.com/microsoft/QuantumKatas#introduction) fornece uma boa introdução sobre [conceitos de computação Quantum](https://github.com/microsoft/QuantumKatas#quantum-computing-concepts-qubits-and-gates) , como operações de Quantum comuns e como manipular o qubits. Mais exemplos também podem ser encontrados em [operações intrínsecas e funções](xref:microsoft.quantum.libraries.standard.prelude).



