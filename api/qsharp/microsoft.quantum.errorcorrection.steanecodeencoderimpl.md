---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoderImpl
title: Operação SteaneCodeEncoderImpl
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeEncoderImpl
qsharp.summary: Private operation used to implement both the Steane code encoder and decoder.
ms.openlocfilehash: b843422a6007d01de9b57ec659c229b8ab0ad2e6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693439"
---
# <a name="steanecodeencoderimpl-operation"></a><span data-ttu-id="b42d9-102">Operação SteaneCodeEncoderImpl</span><span class="sxs-lookup"><span data-stu-id="b42d9-102">SteaneCodeEncoderImpl operation</span></span>

<span data-ttu-id="b42d9-103">Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="b42d9-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="b42d9-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b42d9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b42d9-105">Operação privada usada para implementar o codificador de código Steane e o decodificador.</span><span class="sxs-lookup"><span data-stu-id="b42d9-105">Private operation used to implement both the Steane code encoder and decoder.</span></span>

```qsharp
operation SteaneCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="b42d9-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="b42d9-106">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="b42d9-107">dados: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b42d9-107">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b42d9-108">uma matriz que mantém 1 qubit que é a qubit de entrada.</span><span class="sxs-lookup"><span data-stu-id="b42d9-108">an array holding 1 qubit which is the input qubit.</span></span>


### <a name="scratch--qubit"></a><span data-ttu-id="b42d9-109">Scratch: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b42d9-109">scratch : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b42d9-110">uma matriz que contém 6 qubits que adicionam redundância.</span><span class="sxs-lookup"><span data-stu-id="b42d9-110">an array holding 6 qubits which add redundancy.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b42d9-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b42d9-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

