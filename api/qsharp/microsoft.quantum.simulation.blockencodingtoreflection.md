---
uid: Microsoft.Quantum.Simulation.BlockEncodingToReflection
title: Função BlockEncodingToReflection
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingToReflection
qsharp.summary: >-
  Converts a `BlockEncoding` into an equivalent `BLockEncodingReflection`.

  That is, given a `BlockEncoding` unitary $U$ that encodes some operator $H$ of interest, converts it into a `BlockEncodingReflection` $U'$ that encodes the same operator, but also satisfies $U'^\dagger = U'$. This increases the size of the auxiliary register of $U$ by one qubit.
ms.openlocfilehash: 742d4f5623c7c26810998f6c96e2c7b05cc452d3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225339"
---
# <a name="blockencodingtoreflection-function"></a>Função BlockEncodingToReflection

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Converte um `BlockEncoding` em um equivalente `BLockEncodingReflection` .

Ou seja, dado um `BlockEncoding` unitário $U $ que codifica algum operador $H $ de interesse, converte-o em um `BlockEncodingReflection` $U ' $ que codifica o mesmo operador, mas também satisfaz $U ' ^ \Dagger = U ' $.
Isso aumenta o tamanho do registro auxiliar de $U $ por um qubit.

```qsharp
function BlockEncodingToReflection (blockEncoding : Microsoft.Quantum.Simulation.BlockEncoding) : Microsoft.Quantum.Simulation.BlockEncodingReflection
```


## <a name="input"></a>Entrada

### <a name="blockencoding--blockencoding"></a>blockEncoding: [blockEncoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)

Um `BlockEncoding` unitário $U $ a ser convertido em uma reflexão.



## <a name="output--blockencodingreflection"></a>Saída: [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)

Um unitário $U ' $ agindo em conjunto em registros `a` e `s` que os codificadores de bloco $H $ e satisfaz $U ' ^ \Dagger = U ' $.

## <a name="remarks"></a>Comentários

Isso aumenta o tamanho do registro auxiliar de $U $ por um qubit.

## <a name="references"></a>Referências

- Simulação de Hamiltonian por Qubitization Guang Hao Low, Julio L. Chuang https://arxiv.org/abs/1610.06546

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Simulation. BlockEncoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [Microsoft. Quantum. Simulation. BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)