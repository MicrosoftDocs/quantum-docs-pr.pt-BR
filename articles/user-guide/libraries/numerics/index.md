---
title: Introdução à Biblioteca de Numéricos do Quantum | Microsoft Docs
description: Introdução à Biblioteca de Numéricos do Quantum
author: thomashaener
ms.author: thhaner
ms.date: 5/14/2019
ms.topic: article
uid: microsoft.quantum.numerics.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: dc6407d9775ad8a401036912abd0b70033796144
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868773"
---
# <a name="introduction-to-the-quantum-numerics-library"></a>Introdução à Biblioteca de Numéricos do Quantum

Muitos algoritmos quantum dependem de [oracles](xref:microsoft.quantum.concepts.oracles) que avaliam as funções matemáticas em uma superposição de entradas.
O principal componente do algoritmo de Shor, por exemplo, avalia $f(x) = a^x\operatorname{mod} N$ para um $a$ fixo, o número para fatorar $N$ e um inteiro de $x$ a $2n$ qubits em uma superposição uniforme em todas as cadeias de caracteres de $2n$ bits.

Para executar o algoritmo de Shor em um computador quantum real, essa função precisa ser escrita em termos das operações nativas do computador de destino.
Usando a representação binária de $x$ com $x_i$ denotando a contagem de bits $i$-ésimos do bit menos significativo, $f(x)$ pode ser escrito como $f(x) = a^{\sum_{i=0}^{2n-1} x_i 2^i} \operatorname{mod} N$.
Por sua vez, isso pode ser escrito como um produto (mod N) de termos $a^{2^i x_i}=(a^{2^i})^{x_i}$. A função $f(x)$ pode, portanto, ser implementada usando uma sequência de multiplicações $2n$ (modulares) por $a^{2^i}$ condicional em $x_i$ sendo diferente de zero. As constantes $a^{2^i}$ podem ser pré-calculadas e de módulo N reduzido antes da execução do algoritmo.

Essa sequência de multiplicações modulares controladas pode ser simplificada ainda mais: Cada multiplicação pode ser efetuada usando uma sequência de $n$ adições modulares controladas; e cada adição modular pode ser criada com base em uma adição regular e um comparador.


Considerando que muitas etapas são necessárias para se chegar a uma implementação real, seria extremamente útil ter essa funcionalidade disponível desde o início.
É por isso que o Quantum Development Kit oferece suporte para uma ampla variedade de funcionalidades numéricas.


## <a name="functionality"></a>Funcionalidade

Além da aritmética de inteiros mencionada até agora, a biblioteca de numéricos fornece

- Funcionalidade de inteiro com (sem) sinal (multiplicação, quadrado, divisão com resto, inversão...) com um ou dois números inteiros quantum como entrada
- Funcionalidade de ponto fixo (adição/subtração, multiplicação, quadrado, 1/x, avaliação polinomial) com um ou dois números de ponto fixo quantum como entrada

## <a name="getting-started"></a>Introdução

> [!div class="nextstepaction"]
> [Saiba como usar a biblioteca de numéricos](xref:microsoft.quantum.numerics.usage)
