---
uid: Microsoft.Quantum.Canon.ApplyToTail
title: Operação ApplyToTail
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTail
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 077e6dedee68b0bd05a668387b22f8bec87a4041
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850447"
---
# <a name="applytotail-operation"></a>Operação ApplyToTail

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma operação ao último elemento de uma matriz.

```qsharp
operation ApplyToTail<'T> (op : ('T => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a>Descrição

Dada uma operação `op` e uma matriz de destinos `targets` , aplica-se `op(Tail(targets))` .

## <a name="input"></a>Entrada

### <a name="op--t--unit"></a>op: ' T' = [unidade](xref:microsoft.quantum.lang-ref.unit) de> 

Uma operação a ser aplicada.


### <a name="targets--t"></a>destinos: ' t []

Uma matriz de destinos, da qual a última será aplicada `op` .



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'

O tipo de entrada da operação a ser aplicada.

## <a name="example"></a>Exemplo

Os seguintes trechos de código Q # são equivalentes:

```qsharp
ApplyToTail(H, register);
H(Tail(register));
```

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyToTailA](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [Microsoft. Quantum. Canon. ApplyToTailC](xref:Microsoft.Quantum.Canon.ApplyToTailC)
- [Microsoft. Quantum. Canon. ApplyToTailCA](xref:Microsoft.Quantum.Canon.ApplyToTailCA)