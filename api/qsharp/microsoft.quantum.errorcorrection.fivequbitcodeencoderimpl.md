---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoderImpl
title: Operação FiveQubitCodeEncoderImpl
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCodeEncoderImpl
qsharp.summary: Private operation used to implement both the 5 qubit encoder and decoder.
ms.openlocfilehash: 29b0f47ddffeae3ed4dfda4084304427418e02fd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693460"
---
# <a name="fivequbitcodeencoderimpl-operation"></a><span data-ttu-id="c92b5-102">Operação FiveQubitCodeEncoderImpl</span><span class="sxs-lookup"><span data-stu-id="c92b5-102">FiveQubitCodeEncoderImpl operation</span></span>

<span data-ttu-id="c92b5-103">Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="c92b5-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="c92b5-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c92b5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c92b5-105">Operação privada usada para implementar o codificador 5 qubit e o decodificador.</span><span class="sxs-lookup"><span data-stu-id="c92b5-105">Private operation used to implement both the 5 qubit encoder and decoder.</span></span>

```qsharp
operation FiveQubitCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="c92b5-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="c92b5-106">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="c92b5-107">dados: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c92b5-107">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c92b5-108">uma matriz que mantém 1 qubit que é a qubit de entrada.</span><span class="sxs-lookup"><span data-stu-id="c92b5-108">an array holding 1 qubit which is the input qubit.</span></span>


### <a name="scratch--qubit"></a><span data-ttu-id="c92b5-109">Scratch: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c92b5-109">scratch : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c92b5-110">uma matriz que contém 4 qubits que adiciona redundância.</span><span class="sxs-lookup"><span data-stu-id="c92b5-110">an array holding 4 qubits which add redundancy.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c92b5-111">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c92b5-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="c92b5-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c92b5-112">Remarks</span></span>

<span data-ttu-id="c92b5-113">O codificador específico escolhido foi tirado do papel V. Kliuchnikov e D. Maslov, "otimização de circuitos de Clifford", Phys. Rev. Phys. Rev. A 88, 052307 (2013); https://arxiv.org/abs/1305.0810, Figura 4b) e requer um total de 11 Gates.</span><span class="sxs-lookup"><span data-stu-id="c92b5-113">The particular encoder chosen was taken from the paper V. Kliuchnikov and D. Maslov, "Optimization of Clifford Circuits," Phys. Rev. Phys. Rev. A 88, 052307 (2013); https://arxiv.org/abs/1305.0810, Figure 4b) and requires a total of 11 gates.</span></span>