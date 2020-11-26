---
uid: Microsoft.Quantum.Simulation.ApplyBlockEncodingFromBEandQubit
title: Operação ApplyBlockEncodingFromBEandQubit
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: ApplyBlockEncodingFromBEandQubit
qsharp.summary: Conversion of ((LittleEndian, Qubit[]) => () is Adj + Ctl) to BlockEncoding
ms.openlocfilehash: 16d54a982b020f4d4ded5901ec07de44a2d09726
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229606"
---
# <a name="applyblockencodingfrombeandqubit-operation"></a><span data-ttu-id="42ced-102">Operação ApplyBlockEncodingFromBEandQubit</span><span class="sxs-lookup"><span data-stu-id="42ced-102">ApplyBlockEncodingFromBEandQubit operation</span></span>

<span data-ttu-id="42ced-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="42ced-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="42ced-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="42ced-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="42ced-105">Conversão de ((LittleEndian, qubit []) => () é adj + CTL) para BlockEncoding</span><span class="sxs-lookup"><span data-stu-id="42ced-105">Conversion of ((LittleEndian, Qubit[]) => () is Adj + Ctl) to BlockEncoding</span></span>

```qsharp
operation ApplyBlockEncodingFromBEandQubit (op : ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl), auxiliary : Qubit[], system : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="42ced-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="42ced-106">Input</span></span>

### <a name="op--littleendianqubit--unit--is-adj--ctl"></a><span data-ttu-id="42ced-107">op: ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[qubit](xref:microsoft.quantum.lang-ref.qubit)[]) = a [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="42ced-107">op : ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="auxiliary--qubit"></a><span data-ttu-id="42ced-108">auxiliar: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="42ced-108">auxiliary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="system--qubit"></a><span data-ttu-id="42ced-109">sistema: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="42ced-109">system : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--unit"></a><span data-ttu-id="42ced-110">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="42ced-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

