---
uid: Microsoft.Quantum.ErrorCorrection._ExtractLogicalQubitFromSteaneCode
title: _ExtractLogicalQubitFromSteaneCode operação
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: _ExtractLogicalQubitFromSteaneCode
qsharp.summary: >-
  Syndrome measurement and the inverse of embedding.

  $X$- and $Z$-stabilizers are not treated equally, which is due to the particular choice of the encoding circuit. This asymmetry leads to a different syndrome extraction routine. One could measure the syndrome by measuring multi-qubit Pauli operator directly on the code state, but for the distillation purpose the logical qubit is returned into a single qubit, in course of which the syndrome measurements can be done without further ancillas.
ms.openlocfilehash: 71390feb84660cc9bf7bb12b64eac6d3ca512387
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693492"
---
# <a name="_extractlogicalqubitfromsteanecode-operation"></a><span data-ttu-id="be38e-102">_ExtractLogicalQubitFromSteaneCode operação</span><span class="sxs-lookup"><span data-stu-id="be38e-102">_ExtractLogicalQubitFromSteaneCode operation</span></span>

<span data-ttu-id="be38e-103">Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="be38e-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="be38e-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="be38e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="be38e-105">Medição da síndrome e o inverso da incorporação.</span><span class="sxs-lookup"><span data-stu-id="be38e-105">Syndrome measurement and the inverse of embedding.</span></span>

<span data-ttu-id="be38e-106">$X $-e $Z $-estabilizadores não são tratados igualmente, o que se deve à escolha específica do circuito de codificação.</span><span class="sxs-lookup"><span data-stu-id="be38e-106">$X$- and $Z$-stabilizers are not treated equally, which is due to the particular choice of the encoding circuit.</span></span>
<span data-ttu-id="be38e-107">Essa assimetria leva a uma rotina de extração de síndrome diferente.</span><span class="sxs-lookup"><span data-stu-id="be38e-107">This asymmetry leads to a different syndrome extraction routine.</span></span>
<span data-ttu-id="be38e-108">É possível medir a síndrome, medindo o operador qubit Pauli diretamente no estado do código, mas, para a finalidade do detalhamento, o qubit lógico é retornado em um único qubit, o que faz com que as medidas da síndrome possam ser feitas sem mais ancillas.</span><span class="sxs-lookup"><span data-stu-id="be38e-108">One could measure the syndrome by measuring multi-qubit Pauli operator directly on the code state, but for the distillation purpose the logical qubit is returned into a single qubit, in course of which the syndrome measurements can be done without further ancillas.</span></span>

```qsharp
operation _ExtractLogicalQubitFromSteaneCode (code : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit, Int, Int)
```


## <a name="input"></a><span data-ttu-id="be38e-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="be38e-109">Input</span></span>

### <a name="code--logicalregister"></a><span data-ttu-id="be38e-110">código: [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="be38e-110">code : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>





## <a name="output--qubitintint"></a><span data-ttu-id="be38e-111">Saída: ([qubit](xref:microsoft.quantum.lang-ref.qubit),[int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="be38e-111">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>

<span data-ttu-id="be38e-112">O qubit lógico e um par de inteiros para $X $-síndrome e $Z $-síndrome.</span><span class="sxs-lookup"><span data-stu-id="be38e-112">The logical qubit and a pair of integers for $X$-syndrome and $Z$-syndrome.</span></span>
<span data-ttu-id="be38e-113">Elas representam o índice do código qubit em que um único $X $-ou $Z $-Error teria causado a síndrome medida.</span><span class="sxs-lookup"><span data-stu-id="be38e-113">They represent the index of the code qubit on which a single $X$- or $Z$-error would have caused the measured syndrome.</span></span>

## <a name="remarks"></a><span data-ttu-id="be38e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="be38e-114">Remarks</span></span>

<span data-ttu-id="be38e-115">Observe que essa operação não está marcada como `internal` , pois os testes de unidade dependem diretamente dessa operação.</span><span class="sxs-lookup"><span data-stu-id="be38e-115">Note that this operation is not marked as `internal`, as unit tests directly depend on this operation.</span></span> <span data-ttu-id="be38e-116">Como uma melhoria futura, os testes de unidade devem ser refatoráveis para depender apenas dos chamadores públicos diretamente.</span><span class="sxs-lookup"><span data-stu-id="be38e-116">As a future improvement, unit tests should be refactored to depend only on public callables directly.</span></span>

> [!WARNING]
> <span data-ttu-id="be38e-117">Essa rotina é adaptada a um circuito de codificação específico para o código de 7 qubit de Steane; Se o circuito de codificação for modificado, o resultado da síndrome poderá ter que ser interpretado de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="be38e-117">This routine is tailored to a particular encoding circuit for Steane's 7 qubit code; if the encoding circuit is modified then the syndrome outcome might have to be interpreted differently.</span></span>