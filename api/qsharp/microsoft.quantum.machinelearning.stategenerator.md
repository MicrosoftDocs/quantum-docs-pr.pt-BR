---
uid: Microsoft.Quantum.MachineLearning.StateGenerator
title: Tipo definido pelo usuário StateGenerator
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: StateGenerator
qsharp.summary: Describes an operation that prepares a given input to a sequential classifier.
ms.openlocfilehash: e3026dbae7209acd41924c0038a6f9b2c4b41197
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694981"
---
# <a name="stategenerator-user-defined-type"></a><span data-ttu-id="f639e-102">Tipo definido pelo usuário StateGenerator</span><span class="sxs-lookup"><span data-stu-id="f639e-102">StateGenerator user defined type</span></span>

<span data-ttu-id="f639e-103">Namespace: [Microsoft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="f639e-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="f639e-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f639e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f639e-105">Descreve uma operação que prepara uma determinada entrada para um classificador sequencial.</span><span class="sxs-lookup"><span data-stu-id="f639e-105">Describes an operation that prepares a given input to a sequential classifier.</span></span>

```qsharp

newtype StateGenerator = (NQubits : Int, Prepare : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="f639e-106">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="f639e-106">Named Items</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="f639e-107">NQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f639e-107">NQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f639e-108">O número de qubits em que a entrada codificada é definida.</span><span class="sxs-lookup"><span data-stu-id="f639e-108">The number of qubits on which the encoded input is defined.</span></span>
### <a name="prepare--littleendian--unit-adj--ctl"></a><span data-ttu-id="f639e-109">Preparar: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) da => [unidade](xref:microsoft.quantum.lang-ref.unit) do ano + CTL</span><span class="sxs-lookup"><span data-stu-id="f639e-109">Prepare : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="f639e-110">Uma operação que prepara a entrada codificada em um registro little-endian de `NQubits` qubits.</span><span class="sxs-lookup"><span data-stu-id="f639e-110">An operation which prepares the encoded input on a little-endian register of `NQubits` qubits.</span></span>