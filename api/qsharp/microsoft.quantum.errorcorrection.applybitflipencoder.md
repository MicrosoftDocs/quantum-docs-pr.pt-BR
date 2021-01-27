---
uid: Microsoft.Quantum.ErrorCorrection.ApplyBitFlipEncoder
title: Operação ApplyBitFlipEncoder
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: ApplyBitFlipEncoder
qsharp.summary: >-
  Private operation used to implement both the bit flip encoder and decoder.

  Note that this encoder can make use of in-place coherent recovery, in which case it will "cause" the error described by the initial state of `auxQubits`. In particular, if `auxQubits` are initially in the state $\ket{10}$, this will cause an $X_1$ error on the encoded qubit.
ms.openlocfilehash: cc70cc409cb472a747899838d3a9ad2d78f6b5ab
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827703"
---
# <a name="applybitflipencoder-operation"></a>Operação ApplyBitFlipEncoder

Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Operação privada usada para implementar o codificador de flip bit e o decodificador.

Observe que esse codificador pode fazer uso de recuperação coerente in-loco; nesse caso, ele "causará" o erro descrito pelo estado inicial de `auxQubits` .
Em particular, se `auxQubits` estiver inicialmente no estado $ \ket {10} $, isso causará um erro $X _1 $ no qubit codificado.

```qsharp
operation ApplyBitFlipEncoder (coherentRecovery : Bool, data : Qubit[], scratch : Qubit[]) : Unit is Adj
```


## <a name="input"></a>Entrada

### <a name="coherentrecovery--bool"></a>coherentRecovery: [bool](xref:microsoft.quantum.lang-ref.bool)




### <a name="data--qubit"></a>dados: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="scratch--qubit"></a>Scratch: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]





## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Referências

- doi:10.1103/PhysRevA.85.044302