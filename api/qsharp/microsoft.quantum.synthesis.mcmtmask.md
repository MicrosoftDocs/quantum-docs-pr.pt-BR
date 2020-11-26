---
uid: Microsoft.Quantum.Synthesis.MCMTMask
title: Tipo definido pelo usuário MCMTMask
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: MCMTMask
qsharp.summary: >-
  A type to represent a multiple-controlled multiple-target Toffoli gate.

  The first integer is a bit mask for control lines.  Bit indexes which are set correspond to control line indexes.

  The second integer is a bit mask for target lines.  Bit indexes which are set correspond to target line indexes.

  The bit indexes of both integers must be disjoint.
ms.openlocfilehash: 3c2debbb1f2019c7188dcb00f8ac09154fd4fd4f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203002"
---
# <a name="mcmtmask-user-defined-type"></a><span data-ttu-id="09811-102">Tipo definido pelo usuário MCMTMask</span><span class="sxs-lookup"><span data-stu-id="09811-102">MCMTMask user defined type</span></span>

<span data-ttu-id="09811-103">Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="09811-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="09811-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="09811-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="09811-105">Um tipo para representar um portão de Toffoli de vários destinos com vários controle.</span><span class="sxs-lookup"><span data-stu-id="09811-105">A type to represent a multiple-controlled multiple-target Toffoli gate.</span></span>

<span data-ttu-id="09811-106">O primeiro inteiro é uma máscara de bits para linhas de controle.</span><span class="sxs-lookup"><span data-stu-id="09811-106">The first integer is a bit mask for control lines.</span></span>  <span data-ttu-id="09811-107">Os índices de bits definidos correspondem aos índices de linha de controle.</span><span class="sxs-lookup"><span data-stu-id="09811-107">Bit indexes which are set correspond to control line indexes.</span></span>

<span data-ttu-id="09811-108">O segundo inteiro é uma máscara de bits para linhas de destino.</span><span class="sxs-lookup"><span data-stu-id="09811-108">The second integer is a bit mask for target lines.</span></span>  <span data-ttu-id="09811-109">Os índices de bits definidos correspondem aos índices de linha de destino.</span><span class="sxs-lookup"><span data-stu-id="09811-109">Bit indexes which are set correspond to target line indexes.</span></span>

<span data-ttu-id="09811-110">Os índices de bits de ambos os inteiros devem ser não contíguos.</span><span class="sxs-lookup"><span data-stu-id="09811-110">The bit indexes of both integers must be disjoint.</span></span>

```qsharp

newtype MCMTMask = (ControlMask : Int, TargetMask : Int);
```



## <a name="named-items"></a><span data-ttu-id="09811-111">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="09811-111">Named Items</span></span>

### <a name="controlmask--int"></a><span data-ttu-id="09811-112">ControlMask: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="09811-112">ControlMask : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>


### <a name="targetmask--int"></a><span data-ttu-id="09811-113">TargetMask: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="09811-113">TargetMask : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

