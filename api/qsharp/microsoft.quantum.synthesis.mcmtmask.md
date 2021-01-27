---
uid: Microsoft.Quantum.Synthesis.MCMTMask
title: Tipo definido pelo usuário MCMTMask
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: MCMTMask
qsharp.summary: >-
  A type to represent a multiple-controlled multiple-target Toffoli gate.

  The first integer is a bit mask for control lines.  Bit indexes which are set correspond to control line indexes.

  The second integer is a bit mask for target lines.  Bit indexes which are set correspond to target line indexes.

  The bit indexes of both integers must be disjoint.
ms.openlocfilehash: 50bec0f9aca95afab83491db6b742d1f0323371f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855370"
---
# <a name="mcmtmask-user-defined-type"></a><span data-ttu-id="01b46-102">Tipo definido pelo usuário MCMTMask</span><span class="sxs-lookup"><span data-stu-id="01b46-102">MCMTMask user defined type</span></span>

<span data-ttu-id="01b46-103">Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="01b46-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="01b46-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="01b46-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="01b46-105">Um tipo para representar um portão de Toffoli de vários destinos com vários controle.</span><span class="sxs-lookup"><span data-stu-id="01b46-105">A type to represent a multiple-controlled multiple-target Toffoli gate.</span></span>

<span data-ttu-id="01b46-106">O primeiro inteiro é uma máscara de bits para linhas de controle.</span><span class="sxs-lookup"><span data-stu-id="01b46-106">The first integer is a bit mask for control lines.</span></span>  <span data-ttu-id="01b46-107">Os índices de bits definidos correspondem aos índices de linha de controle.</span><span class="sxs-lookup"><span data-stu-id="01b46-107">Bit indexes which are set correspond to control line indexes.</span></span>

<span data-ttu-id="01b46-108">O segundo inteiro é uma máscara de bits para linhas de destino.</span><span class="sxs-lookup"><span data-stu-id="01b46-108">The second integer is a bit mask for target lines.</span></span>  <span data-ttu-id="01b46-109">Os índices de bits definidos correspondem aos índices de linha de destino.</span><span class="sxs-lookup"><span data-stu-id="01b46-109">Bit indexes which are set correspond to target line indexes.</span></span>

<span data-ttu-id="01b46-110">Os índices de bits de ambos os inteiros devem ser não contíguos.</span><span class="sxs-lookup"><span data-stu-id="01b46-110">The bit indexes of both integers must be disjoint.</span></span>

```qsharp

newtype MCMTMask = (ControlMask : Int, TargetMask : Int);
```



## <a name="named-items"></a><span data-ttu-id="01b46-111">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="01b46-111">Named Items</span></span>

### <a name="controlmask--int"></a><span data-ttu-id="01b46-112">ControlMask: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="01b46-112">ControlMask : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>


### <a name="targetmask--int"></a><span data-ttu-id="01b46-113">TargetMask: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="01b46-113">TargetMask : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

