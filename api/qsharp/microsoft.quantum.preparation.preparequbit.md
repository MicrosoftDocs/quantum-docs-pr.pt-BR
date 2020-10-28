---
uid: Microsoft.Quantum.Preparation.PrepareQubit
title: Operação PrepareQubit
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareQubit
qsharp.summary: >-
  Prepares a qubit in the +1 (`Zero`) eigenstate of the given Pauli operator. If the identity operator is given, then the qubit is prepared in the maximally mixed state.

  If the qubit was initially in the $\ket{0}$ state, this operation prepares the qubit in the $+1$ eigenstate of a given Pauli operator, or, for `PauliI`, in the maximally mixed state instead (see <xref:microsoft.quantum.preparation.preparesinglequbitidentity>).

  If the qubit was in a state other than $\ket{0}$, this operation applies the following gates: $H$ for `PauliX`, $HS$ for `PauliY`, $I$ for `PauliZ` and <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI`.
ms.openlocfilehash: 5f42bf26a8f9638ea88c035a18846050c3776b45
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92695068"
---
# <a name="preparequbit-operation"></a><span data-ttu-id="2e1c9-102">Operação PrepareQubit</span><span class="sxs-lookup"><span data-stu-id="2e1c9-102">PrepareQubit operation</span></span>

<span data-ttu-id="2e1c9-103">Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="2e1c9-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="2e1c9-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2e1c9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2e1c9-105">Prepara um qubit no eigenstate + 1 ( `Zero` ) do operador Pauli fornecido.</span><span class="sxs-lookup"><span data-stu-id="2e1c9-105">Prepares a qubit in the +1 (`Zero`) eigenstate of the given Pauli operator.</span></span>
<span data-ttu-id="2e1c9-106">Se o operador Identity for fornecido, o qubit será preparado no estado de forma máxima mista.</span><span class="sxs-lookup"><span data-stu-id="2e1c9-106">If the identity operator is given, then the qubit is prepared in the maximally mixed state.</span></span>

<span data-ttu-id="2e1c9-107">Se o qubit estava inicialmente no estado $ \ket {0} $, essa operação prepara o qubit na eigenstate $ + $1 de um determinado operador Pauli, ou, para `PauliI` , no estado máximo misto em vez disso (consulte <xref:microsoft.quantum.preparation.preparesinglequbitidentity> ).</span><span class="sxs-lookup"><span data-stu-id="2e1c9-107">If the qubit was initially in the $\ket{0}$ state, this operation prepares the qubit in the $+1$ eigenstate of a given Pauli operator, or, for `PauliI`, in the maximally mixed state instead (see <xref:microsoft.quantum.preparation.preparesinglequbitidentity>).</span></span>

<span data-ttu-id="2e1c9-108">Se o qubit estava em um estado diferente de $ \ket {0} $, essa operação aplica os seguintes Gates: $H $ para `PauliX` , $HS $ para `PauliY` , $I $ para `PauliZ` e <xref:microsoft.quantum.preparation.preparesinglequbitidentity> para `PauliI` .</span><span class="sxs-lookup"><span data-stu-id="2e1c9-108">If the qubit was in a state other than $\ket{0}$, this operation applies the following gates: $H$ for `PauliX`, $HS$ for `PauliY`, $I$ for `PauliZ` and <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI`.</span></span>

```qsharp
operation PrepareQubit (basis : Pauli, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="2e1c9-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="2e1c9-109">Input</span></span>

### <a name="basis--pauli"></a><span data-ttu-id="2e1c9-110">base: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="2e1c9-110">basis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="2e1c9-111">Um operador Pauli $P $.</span><span class="sxs-lookup"><span data-stu-id="2e1c9-111">A Pauli operator $P$.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="2e1c9-112">qubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="2e1c9-112">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="2e1c9-113">Um qubit a ser preparado.</span><span class="sxs-lookup"><span data-stu-id="2e1c9-113">A qubit to be prepared.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2e1c9-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2e1c9-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

