---
uid: Microsoft.Quantum.Synthesis.MCMTMask
title: Tipo definido pelo usuário MCMTMask
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: MCMTMask
qsharp.summary: >-
  A type to represent a multiple-controlled multiple-target Toffoli gate.

  The first integer is a bit mask for control lines.  Bit indexes which are set correspond to control line indexes.

  The second integer is a bit mask for target lines.  Bit indexes which are set correspond to target line indexes.

  The bit indexes of both integers must be disjoint.
ms.openlocfilehash: 0d3ca12d55fa4b5e8332d50939954de29e39b715
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697094"
---
# <a name="mcmtmask-user-defined-type"></a><span data-ttu-id="d7074-102">Tipo definido pelo usuário MCMTMask</span><span class="sxs-lookup"><span data-stu-id="d7074-102">MCMTMask user defined type</span></span>

<span data-ttu-id="d7074-103">Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="d7074-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="d7074-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d7074-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d7074-105">Um tipo para representar um portão de Toffoli de vários destinos com vários controle.</span><span class="sxs-lookup"><span data-stu-id="d7074-105">A type to represent a multiple-controlled multiple-target Toffoli gate.</span></span>

<span data-ttu-id="d7074-106">O primeiro inteiro é uma máscara de bits para linhas de controle.</span><span class="sxs-lookup"><span data-stu-id="d7074-106">The first integer is a bit mask for control lines.</span></span>  <span data-ttu-id="d7074-107">Os índices de bits definidos correspondem aos índices de linha de controle.</span><span class="sxs-lookup"><span data-stu-id="d7074-107">Bit indexes which are set correspond to control line indexes.</span></span>

<span data-ttu-id="d7074-108">O segundo inteiro é uma máscara de bits para linhas de destino.</span><span class="sxs-lookup"><span data-stu-id="d7074-108">The second integer is a bit mask for target lines.</span></span>  <span data-ttu-id="d7074-109">Os índices de bits definidos correspondem aos índices de linha de destino.</span><span class="sxs-lookup"><span data-stu-id="d7074-109">Bit indexes which are set correspond to target line indexes.</span></span>

<span data-ttu-id="d7074-110">Os índices de bits de ambos os inteiros devem ser não contíguos.</span><span class="sxs-lookup"><span data-stu-id="d7074-110">The bit indexes of both integers must be disjoint.</span></span>

```qsharp

newtype MCMTMask = (ControlMask : Int, TargetMask : Int);
```



## <a name="named-items"></a><span data-ttu-id="d7074-111">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="d7074-111">Named Items</span></span>

### <a name="controlmask--int"></a><span data-ttu-id="d7074-112">ControlMask: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d7074-112">ControlMask : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>


### <a name="targetmask--int"></a><span data-ttu-id="d7074-113">TargetMask: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d7074-113">TargetMask : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

