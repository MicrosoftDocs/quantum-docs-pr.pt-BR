---
uid: Microsoft.Quantum.Arithmetic.AddFxP
title: Operação AddFxP
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddFxP
qsharp.summary: Adds two fixed-point numbers stored in quantum registers.
ms.openlocfilehash: cf1f1379b7e1c32aefb0fccb55f4d13c95c78d8f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694881"
---
# <a name="addfxp-operation"></a><span data-ttu-id="602cc-102">Operação AddFxP</span><span class="sxs-lookup"><span data-stu-id="602cc-102">AddFxP operation</span></span>

<span data-ttu-id="602cc-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="602cc-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="602cc-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="602cc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="602cc-105">Adiciona dois números de ponto fixo armazenados em registros de Quantum.</span><span class="sxs-lookup"><span data-stu-id="602cc-105">Adds two fixed-point numbers stored in quantum registers.</span></span>

```qsharp
operation AddFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="description"></a><span data-ttu-id="602cc-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="602cc-106">Description</span></span>

<span data-ttu-id="602cc-107">Considerando dois registros de ponto fixo, respectivamente nos Estados $ \ket{f_1} $ e $ \ket{f_2} $, o executa a operação $ \ket{f_1} \ket{f_2} \mapsto \ket{f_1} \ket{f_1 + f_2} $.</span><span class="sxs-lookup"><span data-stu-id="602cc-107">Given two fixed-point registers respectively in states $\ket{f_1}$ and $\ket{f_2}$, performs the operation $\ket{f_1} \ket{f_2} \mapsto \ket{f_1} \ket{f_1 + f_2}$.</span></span>

## <a name="input"></a><span data-ttu-id="602cc-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="602cc-108">Input</span></span>

### <a name="fp1--fixedpoint"></a><span data-ttu-id="602cc-109">FP1: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="602cc-109">fp1 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="602cc-110">Primeiro número de ponto fixo</span><span class="sxs-lookup"><span data-stu-id="602cc-110">First fixed-point number</span></span>


### <a name="fp2--fixedpoint"></a><span data-ttu-id="602cc-111">FP2: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="602cc-111">fp2 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="602cc-112">Segundo número de ponto fixo, será atualizado para conter a soma das duas entradas.</span><span class="sxs-lookup"><span data-stu-id="602cc-112">Second fixed-point number, will be updated to contain the sum of the two inputs.</span></span>



## <a name="output--unit"></a><span data-ttu-id="602cc-113">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="602cc-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="602cc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="602cc-114">Remarks</span></span>

<span data-ttu-id="602cc-115">A implementação atual requer que os dois números de ponto fixo tenham a mesma posição de ponto de contagem do bit menos significativo, ou seja, $n _i $ e $p _i $ devem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="602cc-115">The current implementation requires the two fixed-point numbers to have the same point position counting from the least-significant bit, i.e., $n_i$ and $p_i$ must be equal.</span></span>