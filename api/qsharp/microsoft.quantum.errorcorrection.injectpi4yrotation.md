---
uid: Microsoft.Quantum.ErrorCorrection.InjectPi4YRotation
title: Operação InjectPi4YRotation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: InjectPi4YRotation
qsharp.summary: Rotates a single qubit by π/4 about the Y-axis.
ms.openlocfilehash: 4ff0abe67a6d18204e417a45f8d8f1d092d02b88
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200791"
---
# <a name="injectpi4yrotation-operation"></a>Operação InjectPi4YRotation

Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gira um único qubit por π/4 sobre o eixo Y.

```qsharp
operation InjectPi4YRotation (data : Qubit, magic : Qubit) : Unit is Adj
```


## <a name="description"></a>Descrição

Executa uma rotação de π/4 sobre `Y` .

A rotação é executada consumindo um estado mágico; ou seja, uma cópia do estado $ $ \begin{align} \cos\frac{\pi} {8} \ket {0} + \sin \frac{\pi} {8} \ket {1} .
\end{align} $ $

## <a name="input"></a>Entrada

### <a name="data--qubit"></a>dados: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Um qubit a ser girado sobre $Y $ por $ \pi/$4.


### <a name="magic--qubit"></a>mágica: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Um qubit inicialmente no estado mágico. O aplicativo a seguir dessa operação `magic` é retornado para o estado $ \ket {0} $.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Os itens a seguir são equivalentes:

```qsharp
Ry(PI() / 4.0, data);
```

e

```qsharp
using (magic = Qubit()) {
    Ry(PI() / 4.0, magic);
    InjectPi4YRotation(data, magic);
    Reset(magic);
}
```

Esta operação dá suporte ao `Adjoint` functor, caso em que o mesmo estado mágico é consumido, mas o efeito no qubit de dados é uma rotação de $-\ pi/4 $ $Y $.