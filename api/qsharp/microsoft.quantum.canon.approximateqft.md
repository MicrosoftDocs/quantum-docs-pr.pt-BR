---
uid: Microsoft.Quantum.Canon.ApproximateQFT
title: Operação ApproximateQFT
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximateQFT
qsharp.summary: Apply the Approximate Quantum Fourier Transform (AQFT) to a quantum register.
ms.openlocfilehash: 31fd87c0f61292142c7493cc29cad1082a9a2d67
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850315"
---
# <a name="approximateqft-operation"></a>Operação ApproximateQFT

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplique a transformação de Fourier de Quantum aproximada (AQFT) a um registro do Quantum.

```qsharp
operation ApproximateQFT (a : Int, qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="a--int"></a>r: [int](xref:microsoft.quantum.lang-ref.int)

parâmetro de aproximação que determina em qual nível as rotações Z controladas que ocorrem no circuito QFT são removidas.

O parâmetro de aproximação a determina o nível de remoção das rotações Z, ou seja, um ∈ {0.. n} e todas as rotações Z 2π/2K em que k>a são removidas do circuito QFT. É conhecido que para k >= log ₂ (n) + log ₂ (1/ε) + 3 um pode ser associado | | QFT-AQFT | |<ε.


### <a name="qs--bigendian"></a>QS: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)

registro da Quantum de n qubits para o qual a transformação de Fourier de Quantum aproximada é aplicada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

AQFT requer Gates de rotação Z do formato 2π/2K e Hadamard Gates.

Presume-se que a entrada e a saída sejam codificadas na codificação big endian.

## <a name="references"></a>Referências

- [*M. Roetteler, th. Beth*, APL. Algebra Eng. Commun. Compute. 19 (3): 177-193 (2008)](http://doi.org/10.1007/s00200-008-0072-2)
- [*D. Coppersmith* arXiv: Quant-pH/0201067v1](https://arxiv.org/abs/quant-ph/0201067)