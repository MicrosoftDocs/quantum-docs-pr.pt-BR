---
title: 'Usando a biblioteca de numéricos do Microsoft Q #'
description: Saiba mais sobre os tipos e as operações disponíveis na biblioteca de numéricos do Microsoft Quantum.
author: thomashaener
ms.author: thhaner
ms.date: 5/14/2019
ms.topic: article
uid: microsoft.quantum.numerics.usage
ms.openlocfilehash: 10d5675e0ef182211a38db4d09347b05afe109c3
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274330"
---
# <a name="using-the-numerics-library"></a>Usando a biblioteca de numéricos

## <a name="overview"></a>Visão geral

A biblioteca de numéricos consiste em três componentes

1. **Aritmética de inteiro básica** com somas e comparadores de inteiros
1. **Funcionalidade de inteiro de alto nível** criada com base na funcionalidade básica; inclui multiplicação, divisão, inversão, etc.  para inteiros assinados e não assinados.
1. **Funcionalidade aritmética de ponto fixo** com inicialização de ponto fixo, adição, multiplicação, recíproca, avaliação polinomial e medição.

Todos esses componentes podem ser acessados usando uma única `open` instrução:
```qsharp
open Microsoft.Quantum.Arithmetic;
```

## <a name="types"></a>Tipos

A biblioteca de numéricos dá suporte aos seguintes tipos

1. **`LittleEndian`**: Uma matriz qubit `qArr : Qubit[]` que representa um inteiro onde `qArr[0]` denota o bit menos significativo.
1. **`SignedLittleEndian`**: Igual a `LittleEndian` , exceto que representa um inteiro assinado armazenado no complemento de dois.
1. **`FixedPoint`**: Representa um número real que consiste em uma matriz qubit `qArr2 : Qubit[]` e uma posição de ponto binário `pos` , que conta o número de dígitos binários à esquerda do ponto binário. `qArr2`é armazenado da mesma maneira que o `SignedLittleEndian` .

## <a name="operations"></a>Operations

Para cada um dos três tipos acima, uma variedade de operações está disponível:

1. **`LittleEndian`**
    - Adição
    - Comparação
    - Multiplicação
    - Elevar
    - Divisão (com restante)

1. **`SignedLittleEndian`**
    - Adição
    - Comparação
    - Complemento do módulo 2 da inversão
    - Multiplicação
    - Elevar

1. **`FixedPoint`**
    - Preparação/inicialização para um valor clássico
    - Adição (constante clássica ou outro ponto fixo da Quantum)
    - Comparação
    - Multiplicação
    - Elevar
    - Avaliação polinomial com especialização para funções pares e ímpares
    - Recíproco (1/x)
    - Medida (duplo clássico)

Para obter mais informações e documentação detalhada para cada uma dessas operações, consulte os documentos de referência da biblioteca do Q # em [docs.Microsoft.com](https://docs.microsoft.com/quantum)

## <a name="sample-integer-addition"></a>Exemplo: adição de inteiro

Como um exemplo básico, considere a operação $ $ \ket x\ket y\mapsto \ket x\ket {x + y} $ $ ou seja, uma operação que usa um inteiro n-qubit $x $ e um n-ou (n + 1)-qubit registrar $y $ como entrada, o último que ele mapeia para a soma $ (x + y) $. Observe que a soma é o módulo computado $2 ^ n $ se $y $ é armazenado em um registro de $n de bits.

Usando o kit de desenvolvimento Quantum, essa operação pode ser aplicada da seguinte maneira:
```qsharp
operation TestMyAddition(xValue : Int, yValue : Int, n : Int) : Unit {
    using ((xQubits, yQubits) = (Qubit[n], Qubit[n]))
    {
        let x = LittleEndian(xQubits); // define bit order
        let y = LittleEndian(yQubits);
        
        ApplyXorInPlace(xValue, x); // initialize values
        ApplyXorInPlace(yValue, y);
        
        AddI(x, y); // perform addition x+y into y
        
        // ... (use the result)
    }
}
```

## <a name="sample-evaluating-smooth-functions"></a>Exemplo: avaliando funções suaves

Para avaliar funções suaves, como $ \sin (x) $ em um computador Quantum, em que $x $ é um `FixedPoint` número Quantum, a biblioteca de numéricos do Quantum Development Kit fornece as operações `EvaluatePolynomialFxP` e `Evaluate[Even/Odd]PolynomialFxP` .

O primeiro, `EvaluatePolynomialFxP` , permite avaliar um polinomial da forma $ $ P (x) = a_0 + a_1x + a_2x ^ 2 + \cdots + a_dx ^ d, $ $, em que $d $ denota o *grau*. Para fazer isso, tudo o que é necessário são os coeficientes polinomiais `[a_0,..., a_d]` (do tipo `Double[]` ), a entrada `x : FixedPoint` e a saída `y : FixedPoint` (inicialmente zero):
```qsharp
EvaluatePolynomialFxP([1.0, 2.0], x, y);
```
O resultado, $P (x) = 1 + 2x $, será armazenado em `yFxP` .

A segunda, `EvaluateEvenPolynomialFxP` e a terceira, `EvaluateOddPolynomialFxP` são especializações para os casos de funções pares e ímpares, respectivamente. Ou seja, para uma função par/ímpar $f (x) $ e $ $ P_ {mesmo} (x) = a_0 + a_1 x ^ 2 + a_2 x ^ 4 + \cdots + a_d x ^ {2D}, $ $ $f (x) $ é aproximado bem pelo $P _ {mesmo} (x) $ ou $P _ {Odd} (x): = x\cdot P_ {mesmo} (x) $, respectivamente.
Em Q #, esses dois casos podem ser tratados da seguinte maneira:
```qsharp
EvaluateEvenPolynomialFxP([1.0, 2.0], x, y);
```
que avalia $P _ {mesmo} (x) = 1 + 2x ^ 2 $ e
```qsharp
EvaluateOddPolynomialFxP([1.0, 2.0], x, y);
```
que avalia $P _ {Odd} (x) = x + 2x ^ 3 $.

## <a name="more-samples"></a>Mais exemplos

Você pode encontrar mais exemplos no [repositório principal de exemplos](https://github.com/Microsoft/Quantum).

Para começar, clone o repositório e abra a `Numerics` subpasta:

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/Numerics
```

Em seguida, `cd` em uma das pastas de exemplo e executar o exemplo via

```bash
dotnet run
```