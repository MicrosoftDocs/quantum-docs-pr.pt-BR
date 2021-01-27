---
uid: Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp
title: Tipo definido pelo usuário SyndromeMeasOp
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SyndromeMeasOp
qsharp.summary: Represents an operation that is used to measure the syndrome of an error-correcting code block.
ms.openlocfilehash: 36336f9e47e5f360cf5e19ffb6e15b4af88b2580
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850045"
---
# <a name="syndromemeasop-user-defined-type"></a>Tipo definido pelo usuário SyndromeMeasOp

Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Representa uma operação que é usada para medir a síndrome de um bloco de código com correção de erros.

```qsharp

newtype SyndromeMeasOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => Microsoft.Quantum.ErrorCorrection.Syndrome));
```



## <a name="example"></a>Exemplo

Meça os síndromes do código de inversão de bits $S = \langle ZZI, IZZ \rangle $ usando o rascunho qubits em uma maneira não tolerante a falhas:

```qsharp
    let syndMeasOp = SyndromeMeasOp(MeasureStabilizerGenerators([
            [PauliZ, PauliZ, PauliI],
            [PauliI, PauliZ, PauliZ]
        ], _, MeasureWithScratch));
```

## <a name="remarks"></a>Comentários

A assinatura `(LogicalRegister => Syndrome)` representa uma operação que atua em conjunto no qubits em `LogicalRegister` e em algumas qubits auxiliares seguidos por uma medida do qubits auxiliar para extrair um `Syndrome` valor que representa a `Result[]` dessas medições.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. ErrorCorrection. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [Microsoft. Quantum. ErrorCorrection. síndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)