---
uid: Microsoft.Quantum.ErrorCorrection.InjectPi4YRotation
title: Operação InjectPi4YRotation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: InjectPi4YRotation
qsharp.summary: Rotates a single qubit by π/4 about the Y-axis.
ms.openlocfilehash: 4ff0abe67a6d18204e417a45f8d8f1d092d02b88
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200791"
---
# <a name="injectpi4yrotation-operation"></a><span data-ttu-id="fab7e-102">Operação InjectPi4YRotation</span><span class="sxs-lookup"><span data-stu-id="fab7e-102">InjectPi4YRotation operation</span></span>

<span data-ttu-id="fab7e-103">Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="fab7e-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="fab7e-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fab7e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fab7e-105">Gira um único qubit por π/4 sobre o eixo Y.</span><span class="sxs-lookup"><span data-stu-id="fab7e-105">Rotates a single qubit by π/4 about the Y-axis.</span></span>

```qsharp
operation InjectPi4YRotation (data : Qubit, magic : Qubit) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="fab7e-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="fab7e-106">Description</span></span>

<span data-ttu-id="fab7e-107">Executa uma rotação de π/4 sobre `Y` .</span><span class="sxs-lookup"><span data-stu-id="fab7e-107">Performs a π/4 rotation about `Y`.</span></span>

<span data-ttu-id="fab7e-108">A rotação é executada consumindo um estado mágico; ou seja, uma cópia do estado $ $ \begin{align} \cos\frac{\pi} {8} \ket {0} + \sin \frac{\pi} {8} \ket {1} .</span><span class="sxs-lookup"><span data-stu-id="fab7e-108">The rotation is performed by consuming a magic state; that is, a copy of the state $$ \begin{align} \cos\frac{\pi}{8} \ket{0} + \sin \frac{\pi}{8} \ket{1}.</span></span>
<span data-ttu-id="fab7e-109">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="fab7e-109">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="fab7e-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="fab7e-110">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="fab7e-111">dados: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="fab7e-111">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="fab7e-112">Um qubit a ser girado sobre $Y $ por $ \pi/$4.</span><span class="sxs-lookup"><span data-stu-id="fab7e-112">A qubit to be rotated about $Y$ by $\pi / 4$.</span></span>


### <a name="magic--qubit"></a><span data-ttu-id="fab7e-113">mágica: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="fab7e-113">magic : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="fab7e-114">Um qubit inicialmente no estado mágico.</span><span class="sxs-lookup"><span data-stu-id="fab7e-114">A qubit initially in the magic state.</span></span> <span data-ttu-id="fab7e-115">O aplicativo a seguir dessa operação `magic` é retornado para o estado $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="fab7e-115">Following application of this operation, `magic` is returned to the $\ket{0}$ state.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fab7e-116">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fab7e-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="fab7e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="fab7e-117">Remarks</span></span>

<span data-ttu-id="fab7e-118">Os itens a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="fab7e-118">The following are equivalent:</span></span>

```qsharp
Ry(PI() / 4.0, data);
```

<span data-ttu-id="fab7e-119">e</span><span class="sxs-lookup"><span data-stu-id="fab7e-119">and</span></span>

```qsharp
using (magic = Qubit()) {
    Ry(PI() / 4.0, magic);
    InjectPi4YRotation(data, magic);
    Reset(magic);
}
```

<span data-ttu-id="fab7e-120">Esta operação dá suporte ao `Adjoint` functor, caso em que o mesmo estado mágico é consumido, mas o efeito no qubit de dados é uma rotação de $-\ pi/4 $ $Y $.</span><span class="sxs-lookup"><span data-stu-id="fab7e-120">This operation supports the `Adjoint` functor, in which case the same magic state is consumed, but the effect on the data qubit is a $-\pi/4$ $Y$-rotation.</span></span>