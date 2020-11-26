---
uid: Microsoft.Quantum.Arithmetic.AddFxP
title: Operação AddFxP
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddFxP
qsharp.summary: Adds two fixed-point numbers stored in quantum registers.
ms.openlocfilehash: 36a5d585a493f0e6f33f74b1686aaa01cca7ac0b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191033"
---
# <a name="addfxp-operation"></a>Operação AddFxP

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Adiciona dois números de ponto fixo armazenados em registros de Quantum.

```qsharp
operation AddFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="description"></a>Descrição

Considerando dois registros de ponto fixo, respectivamente nos Estados $ \ket{f_1} $ e $ \ket{f_2} $, o executa a operação $ \ket{f_1} \ket{f_2} \mapsto \ket{f_1} \ket{f_1 + f_2} $.

## <a name="input"></a>Entrada

### <a name="fp1--fixedpoint"></a>FP1: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Primeiro número de ponto fixo


### <a name="fp2--fixedpoint"></a>FP2: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Segundo número de ponto fixo, será atualizado para conter a soma das duas entradas.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

A implementação atual requer que os dois números de ponto fixo tenham a mesma posição de ponto de contagem do bit menos significativo, ou seja, $n _i $ e $p _i $ devem ser iguais.