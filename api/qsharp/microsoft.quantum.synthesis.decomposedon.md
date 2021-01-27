---
uid: Microsoft.Quantum.Synthesis.DecomposedOn
title: Função decompostay
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecomposedOn
qsharp.summary: Decomposes a permutation on a variable
ms.openlocfilehash: fb7aa5af8f3eb07399e0d2dd2d50723f4e6b169a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855523"
---
# <a name="decomposedon-function"></a>Função decompostay

Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Redação de uma permutação em uma variável

```qsharp
function DecomposedOn (perm : Int[], index : Int) : ((Int[], Int[]), Int[])
```


## <a name="description"></a>Descrição

Dada uma permutação $ \pi $ ( `perm` ) e um índice $i $ ( `index` ), esse método retorna três permutas $ ((\ pi_l, \ pi_r), \pi ') $ de forma que as imagens de $ \ pi_l $ e $ \ pi_r $ não alterem bits em seus elementos em índices diferentes de $i $ e imagens de $ \pi ' $ não altere o bit $i $ em seus elementos.

## <a name="input"></a>Entrada

### <a name="perm--int"></a>Perm: [int](xref:microsoft.quantum.lang-ref.int)[]




### <a name="index--int"></a>índice: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--intintint"></a>Saída: (([int](xref:microsoft.quantum.lang-ref.int)[],[int](xref:microsoft.quantum.lang-ref.int)[]),[int](xref:microsoft.quantum.lang-ref.int)[])



## <a name="example"></a>Exemplo

Suponha que a entrada seja Perm = [0, 2, 3, 5, 7, 1, 4, 6] e índice = 0. em seguida, essa função computa três permutações com base na tabela a seguir, que lista a permutação `perm` em notação binária com elementos no grupo A e imagens no grupo D.  As colunas listam os índices de bits.

|   A |   B |   C |   D |
| 2 1 0 | 2 1 0 | 2 1 0 | 2 1 0 |
|-------|-------|-------|-------|
| 0 0 0 |       |       | 0 0 0 | 0
| 0 0 1 |       |       | 0 1 0 | 2
| 0 1 0 |       |       | 0 1 1 | 3
| 0 1 1 |       |       | 1 0 1 | 5
| 1 0 0 |       |       | 1 1 1 | 7
| 1 0 1 |       |       | 0 0 1 | 1
| 1 1 0 |       |       | 1 0 0 | 4
| 1 1 1 |       |       | 1 1 0 | 6

Todos os valores de índices diferentes de 0 (= índice) são copiados de a para B e de D para C.

|   A |   B |   C |   D |
| 2 1 0 | 2 1 0 | 2 1 0 | 2 1 0 |
|-------|-------|-------|-------|
| 0 0 0 | 0 0   | 0 0   | 0 0 0 |
| 0 0 1 | 0 0   | 0 1   | 0 1 0 |
| 0 1 0 | 0 1   | 0 1   | 0 1 1 |
| 0 1 1 | 0 1   | 1 0   | 1 0 1 |
| 1 0 0 | 1 0   | 1 1   | 1 1 1 |
| 1 0 1 | 1 0   | 0 0   | 0 0 1 |
| 1 1 0 | 1 1   | 1 0   | 1 0 0 |
| 1 1 1 | 1 1   | 1 1   | 1 1 0 |

Em seguida, 0 é colocado para o primeiro elemento com um índice vazio na coluna 0 no bloco B e, em seguida, um 1 é colocado em B, onde o prefixo corresponde (no primeiro caso, a outra linha com os índices 0 0).
Depois, um 1 é adicionado na mesma linha no bloco C e, em seguida, um 0 para o prefixo correspondente no bloco C.  Esse processo é repetido, até que todos os índices tenham sido colocados na coluna 0 nos blocos B e C.

|   A |   B |   C |   D |
| 2 1 0 | 2 1 0 | 2 1 0 | 2 1 0 |
|-------|-------|-------|-------|
| 0 0 0 | 0 0 0 | 0 0 0 | 0 0 0 |
| 0 0 1 | 0 0 1 | 0 1 1 | 0 1 0 |
| 0 1 0 | 0 1 0 | 0 1 0 | 0 1 1 |
| 0 1 1 | 0 1 1 | 1 0 1 | 1 0 1 |
| 1 0 0 | 1 0 0 | 1 1 0 | 1 1 1 |
| 1 0 1 | 1 0 1 | 0 0 1 | 0 0 1 |
| 1 1 0 | 1 1 0 | 1 0 0 | 1 0 0 |
| 1 1 1 | 1 1 1 | 1 1 1 | 1 1 0 |

Podemos ler três novas permutações da tabela:

- $ \ pi_l $ com elementos em A, imagens em B (esquerda)
- $ \ pi_r $ com elementos em D, imagens em C (direita)
- $ \pi ' $ com elementos em B, imagens em C (restante)

Observe que os valores de bit de design não mudam em $ \ pi_l $ e $ \ pi_r $ para os índices 1 e 2, e os valores de bits não são alterados em $ \ pi_ ' $ para o índice 0.  Observe também que $ \ pi_l $ e $ \ pi_r $ devem ser inversos.

As permutações derivadas e retornadas são: esquerda = [0, 1, 2, 3, 4, 5, 6, 7] Right = [0, 1, 3, 2, 4, 5, 7, 6] resto = [0, 3, 2, 5, 6, 1, 4, 7]