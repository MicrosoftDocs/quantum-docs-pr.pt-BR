---
uid: Microsoft.Quantum.ErrorCorrection.QECC
title: Tipo definido pelo usuário QECC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: QECC
qsharp.summary: Represents an error-correcting code as defined by its encoder, decoder, and syndrome measurement procedure.
ms.openlocfilehash: 6a00875f53928da4e0b8da6a3e32e37a551a56b2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693448"
---
# <a name="qecc-user-defined-type"></a><span data-ttu-id="24ba9-102">Tipo definido pelo usuário QECC</span><span class="sxs-lookup"><span data-stu-id="24ba9-102">QECC user defined type</span></span>

<span data-ttu-id="24ba9-103">Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="24ba9-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="24ba9-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="24ba9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="24ba9-105">Representa um código de correção de erro conforme definido por seu codificador, decodificador e procedimento de medição da síndrome.</span><span class="sxs-lookup"><span data-stu-id="24ba9-105">Represents an error-correcting code as defined by its encoder, decoder, and syndrome measurement procedure.</span></span>

```qsharp

newtype QECC = (Microsoft.Quantum.ErrorCorrection.EncodeOp, Microsoft.Quantum.ErrorCorrection.DecodeOp, Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp);
```
