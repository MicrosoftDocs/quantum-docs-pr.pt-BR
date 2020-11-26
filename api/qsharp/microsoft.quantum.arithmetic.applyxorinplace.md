---
uid: Microsoft.Quantum.Arithmetic.ApplyXorInPlace
title: Operação ApplyXorInPlace
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyXorInPlace
qsharp.summary: Applies a bitwise-XOR operation between a classical integer and an integer represented by a register of qubits.
ms.openlocfilehash: b7fc20ac421d5cff9baa3fe05450c1564f123505
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210092"
---
# <a name="applyxorinplace-operation"></a><span data-ttu-id="b46dd-102">Operação ApplyXorInPlace</span><span class="sxs-lookup"><span data-stu-id="b46dd-102">ApplyXorInPlace operation</span></span>

<span data-ttu-id="b46dd-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="b46dd-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="b46dd-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b46dd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b46dd-105">Aplica uma operação de XOR-bit entre um inteiro clássico e um inteiro representado por um registro de qubits.</span><span class="sxs-lookup"><span data-stu-id="b46dd-105">Applies a bitwise-XOR operation between a classical integer and an integer represented by a register of qubits.</span></span>

```qsharp
operation ApplyXorInPlace (value : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="b46dd-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="b46dd-106">Description</span></span>

<span data-ttu-id="b46dd-107">Aplica `X` operações a qubits em um registro little-endian com base em 1 bits em um inteiro.</span><span class="sxs-lookup"><span data-stu-id="b46dd-107">Applies `X` operations to qubits in a little-endian register based on 1 bits in an integer.</span></span>

<span data-ttu-id="b46dd-108">Vamos indicar `value` por a e permitir que y seja um inteiro não assinado codificado em e, `target` em seguida, `InPlaceXorLE` executa uma operação fornecida pelo seguinte mapa: $ \ket{y}\rightarrow \ket{y\oplus a} $, em que $ \oplus $ é o operador OR exclusivo de bit a ponto.</span><span class="sxs-lookup"><span data-stu-id="b46dd-108">Let us denote `value` by a and let y be an unsigned integer encoded in `target`, then `InPlaceXorLE` performs an operation given by the following map: $\ket{y}\rightarrow \ket{y\oplus a}$ , where $\oplus$ is the bitwise exclusive OR operator.</span></span>

## <a name="input"></a><span data-ttu-id="b46dd-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="b46dd-109">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="b46dd-110">valor: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b46dd-110">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b46dd-111">Um inteiro que é considerado não negativo.</span><span class="sxs-lookup"><span data-stu-id="b46dd-111">An integer which is assumed to be non-negative.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="b46dd-112">destino: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="b46dd-112">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="b46dd-113">Um registro Quantum que é usado para armazenar `value` em codificação little-endian.</span><span class="sxs-lookup"><span data-stu-id="b46dd-113">A quantum register which is used to store `value` in little-endian encoding.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b46dd-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b46dd-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

