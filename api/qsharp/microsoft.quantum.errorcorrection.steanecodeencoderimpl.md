---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoderImpl
title: Operação SteaneCodeEncoderImpl
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeEncoderImpl
qsharp.summary: Private operation used to implement both the Steane code encoder and decoder.
ms.openlocfilehash: 3a9a1b11ed9255f18135e3717de7e9e1ec891298
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200417"
---
# <a name="steanecodeencoderimpl-operation"></a><span data-ttu-id="034fc-102">Operação SteaneCodeEncoderImpl</span><span class="sxs-lookup"><span data-stu-id="034fc-102">SteaneCodeEncoderImpl operation</span></span>

<span data-ttu-id="034fc-103">Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="034fc-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="034fc-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="034fc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="034fc-105">Operação privada usada para implementar o codificador de código Steane e o decodificador.</span><span class="sxs-lookup"><span data-stu-id="034fc-105">Private operation used to implement both the Steane code encoder and decoder.</span></span>

```qsharp
operation SteaneCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="034fc-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="034fc-106">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="034fc-107">dados: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="034fc-107">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="034fc-108">uma matriz que mantém 1 qubit que é a qubit de entrada.</span><span class="sxs-lookup"><span data-stu-id="034fc-108">an array holding 1 qubit which is the input qubit.</span></span>


### <a name="scratch--qubit"></a><span data-ttu-id="034fc-109">Scratch: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="034fc-109">scratch : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="034fc-110">uma matriz que contém 6 qubits que adicionam redundância.</span><span class="sxs-lookup"><span data-stu-id="034fc-110">an array holding 6 qubits which add redundancy.</span></span>



## <a name="output--unit"></a><span data-ttu-id="034fc-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="034fc-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

