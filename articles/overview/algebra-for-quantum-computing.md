---
title: Álgebra linear para computação quântica
description: Saiba quais conceitos básicos de álgebra linear são necessários para entender a computação quântica
author: bradben
ms.author: v-benbra
ms.date: 5/5/2020
ms.topic: overview
uid: microsoft.quantum.overview.algebra
no-loc:
- Q#
- $$v
ms.openlocfilehash: 3e6700acc09adf9e2e771f6289c73ad51aa2cb90
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92692260"
---
# <a name="linear-algebra-for-quantum-computing"></a>Álgebra linear para computação quântica

A álgebra linear é a linguagem da computação quântica. Embora você não precise conhecê-la para implementar ou escrever programas quânticos, ela é amplamente usada para descrever os estados de qubits e as operações quânticas, além de prever o que um computador quântico fará em resposta a uma sequência de instruções.

Assim como a familiaridade com os conceitos básicos de [física quântica](xref:microsoft.quantum.overview.understanding) pode ajudar você a entender a computação quântica, um conhecimento básico de álgebra linear pode ajudar você a entender como funcionam os algoritmos quânticos. No mínimo, o ideal é estar familiarizado com os **vetores** e a **multiplicação de matrizes** . Caso você precise relembrar esses conceitos de álgebra, estes são alguns tutoriais que abordam os princípios básicos:

- [Tutorial do Jupyter Notebook sobre álgebra linear](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/LinearAlgebra)
- [Tutorial do Jupyter Notebook sobre aritmética complexa](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/ComplexArithmetic)
- [Álgebra linear para computação quântica](https://cds.cern.ch/record/1522001/files/978-1-4614-6336-8_BookBackMatter.pdf)
- [Conceitos básicos de álgebra linear](https://www.math.ubc.ca/~carrell/NB.pdf)
- [Primer de computação quântica](https://www.codeproject.com/Articles/5155638/Quantum-Computation-Primer-Part-1#exploring-quantum-superposition)

## <a name="vectors-and-matrices-in-quantum-computing"></a>Vetores e matrizes na computação quântica

No tópico [Noções básicas sobre computação quântica](xref:microsoft.quantum.overview.understanding), você viu que um qubit pode estar em um estado igual a 1 ou 0, uma superposição ou ambos. Usando a álgebra linear, o estado de um qubit é descrito como um vetor e é representado por uma só coluna **matriz** $ \begin{bmatrix} a \\\\ b \end{bmatrix} $. Ele também é conhecido como um **vetor de estado quântico** e precisa atender ao requisito de $|a|^2 + |b|^2 = 1$.  

Os elementos da matriz representam a probabilidade de o qubit entrar em colapso para uma forma ou outra, com $|a|^2$ sendo a probabilidade de um colapso para zero e $|b|^2$, a probabilidade de um colapso para um. Todas as seguintes matrizes representam vetores de estado quântico válidos:

$$\begin{bmatrix} 1 \\\\ 0 \end{bmatrix}, \begin{bmatrix} 0 \\\\ 1 \end{bmatrix}, \begin{bmatrix} \frac{1}{\sqrt{2}} \\\\ \frac{1}{\sqrt{2}} \end{bmatrix}, \begin{bmatrix} \frac{1}{\sqrt{2}} \\\\ \frac{-1}{\sqrt{2}} \end{bmatrix}, \text{ and }\begin{bmatrix} \frac{1}{\sqrt{2}} \\\\ \frac{i}{\sqrt{2}} \end{bmatrix}.$$

Em [Computadores e simuladores quânticos](xref:microsoft.quantum.overview.simulators), você também viu que as operações quânticas são usadas para modificar o estado de um qubit.  As operações quânticas também podem ser representadas por uma matriz. Quando uma operação quântica é aplicada a um qubit, as duas matrizes que os representam são multiplicadas e a resposta resultante representa o novo estado do qubit após a operação.  

Veja a seguir duas operações quânticas comuns representadas com a multiplicação de matrizes.


A [operação `X`](xref:Microsoft.Quantum.Intrinsic.X) é representada pela matriz de Pauli $X$,

$$X = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix},$$
    
e é usada para inverter o estado de um qubit de 0 para 1 (ou vice-versa), por exemplo

$$\begin{bmatrix}0 &1\\\\ 1 &0\end{bmatrix}\begin{bmatrix} 1 \\\\ 0 \end{bmatrix} = \begin{bmatrix} 0 \\\\ 1 \end{bmatrix}.$$

A [operação 'H'](xref:Microsoft.Quantum.Intrinsic.H) é representada pela transformação de Hadamard $H$,

$$H = \dfrac{1}{\sqrt{2}}\begin{bmatrix}1 &1\\\\ 1 &-1\end{bmatrix},$$

 e coloca um qubit em um estado de superposição no qual ele tem uma probabilidade igual de colapso para uma das formas, conforme mostrado aqui

$$\frac{1}{\sqrt{2}}\begin{bmatrix}1 &1\\\\ 1 &-1\end{bmatrix}\begin{bmatrix} 1 \\\\ 0 \end{bmatrix}=\frac{1}{\sqrt{2}}\begin{bmatrix} 1 \\\\ 1 \end{bmatrix}=\left(\frac{1}{\sqrt{2}}\right)^2=\frac{1}{2}.$$

Uma matriz que representa uma operação quântica tem um requisito: ela precisa ser uma matriz **unitária** . Uma matriz será unitária se o **inverso** da matriz for igual ao **conjugado transposto** da matriz.

## <a name="representing-two-qubit-states"></a>Como representar os estados de dois qubits

Nos exemplos acima, o estado de um qubit foi descrito usando uma matriz de coluna única $\begin{bmatrix} a \\\\ b \end{bmatrix}$ e a aplicação de uma operação a ela foi descrita multiplicando as duas matrizes. No entanto, os computadores quânticos usam mais de um qubit, portanto, como você descreve o estado combinado de dois qubits? 

Lembre-se de que cada qubit é um espaço vetorial, portanto, eles não podem apenas ser multiplicados. Em vez disso, você usa um **produto tensorial** , uma operação relacionada que cria um espaço vetorial com base em espaços vetoriais individuais e é representado pelo símbolo $\otimes$. Por exemplo, o produto tensorial de dois estados de qubits $\begin{bmatrix} a \\\\ b \end{bmatrix}$ e $\begin{bmatrix} c \\\\ d \end{bmatrix}$ é calculado

$$ \begin{bmatrix} a \\\\ b \end{bmatrix} \otimes \begin{bmatrix} c \\\\ d \end{bmatrix} =\begin{bmatrix} a \begin{bmatrix} c \\\\ d \end{bmatrix} \\\\ b \begin{bmatrix}c \\\\ d \end{bmatrix} \end{bmatrix} = \begin{bmatrix} ac \\\\ ad \\\\ bc \\\\ bd \end{bmatrix}. $$

O resultado é uma matriz de quatro dimensões, com cada elemento representando uma probabilidade. Por exemplo, $ac$ é a probabilidade de que os dois qubits sofram um colapso para 0 e 0, $ad$ é a probabilidade de 0 e 1 etc. 

Assim como apenas um estado de qubit $\begin{bmatrix} a \\\\  b \end{bmatrix}$ deve atender ao requisito $|a|^2 + |b|^2 = 1$ para representar um estado quântico, um estado de dois qubits $\begin{bmatrix} ac \\\\  ad \\\\  bc \\\\  bd \end{bmatrix}$ deve atender ao requisito $|ac|^2 + |ad|^2 + |bc|^2+ |bd|^2 = 1$.

## <a name="summary"></a>Resumo

A álgebra linear é a linguagem padrão para descrever a computação e a física quântica. Embora as [bibliotecas](xref:microsoft.quantum.libraries) incluídas no Microsoft Quantum Development Kit ajudem você a executar algoritmos quânticos avançados sem se aprofundar na matemática subjacente, entender as noções básicas ajudará você a começar a usá-los rapidamente e a fornecerá uma base sólida para o desenvolvimento.

## <a name="next-steps"></a>Próximas etapas

[Instalar o QDK](xref:microsoft.quantum.install)
