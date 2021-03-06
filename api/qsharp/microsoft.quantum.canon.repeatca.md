---
uid: Microsoft.Quantum.Canon.RepeatCA
title: Operação RepeatCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatCA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: af93220562d6be27b2f41e770bd953e5e808fcbf
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852203"
---
# <a name="repeatca-operation"></a>Operação RepeatCA

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Repete uma operação um determinado número de vezes.

```qsharp
operation RepeatCA<'TInput> (op : ('TInput => Unit is Adj + Ctl), nTimes : Int, input : 'TInput) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="op--tinput--unit--is-adj--ctl"></a>op: a [unidade](xref:microsoft.quantum.lang-ref.unit)  ' TInput => é adj + CTL

A operação a ser chamada repetidamente.


### <a name="ntimes--int"></a>nTimes: [int](xref:microsoft.quantum.lang-ref.int)

O número de vezes para chamar `op` .


### <a name="input--tinput"></a>entrada: ' TInput

A entrada a ser passada para `op` .



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="tinput"></a>'TInput



## <a name="example"></a>Exemplo

Os itens a seguir são equivalentes:

```qsharp
RepeatCA(U, 17, target);
(BoundCA(ConstantArray(17, U)))(target);
```

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. arrays. DrawMany](xref:Microsoft.Quantum.Arrays.DrawMany)
- [Microsoft. Quantum. Canon. Repeat](xref:Microsoft.Quantum.Canon.Repeat)
- [Microsoft. Quantum. Canon. REPEATA](xref:Microsoft.Quantum.Canon.RepeatA)
- [Microsoft. Quantum. Canon. RepeatC](xref:Microsoft.Quantum.Canon.RepeatC)