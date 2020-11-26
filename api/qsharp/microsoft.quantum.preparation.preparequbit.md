---
uid: Microsoft.Quantum.Preparation.PrepareQubit
title: Operação PrepareQubit
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareQubit
qsharp.summary: >-
  > [!WARNING]

  > PrepareQubit has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PreparePauliEigenstate> instead.


  Prepares a qubit in the +1 (`Zero`) eigenstate of the given Pauli operator. If the identity operator is given, then the qubit is prepared in the maximally mixed state.

  If the qubit was initially in the $\ket{0}$ state, this operation prepares the qubit in the $+1$ eigenstate of a given Pauli operator, or, for `PauliI`, in the maximally mixed state instead (see <xref:microsoft.quantum.preparation.preparesinglequbitidentity>).

  If the qubit was in a state other than $\ket{0}$, this operation applies the following gates: $H$ for `PauliX`, $HS$ for `PauliY`, $I$ for `PauliZ` and <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI`.
ms.openlocfilehash: 84674d70d6a038ceaf1c637b22afa1b724d90795
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193515"
---
# <a name="preparequbit-operation"></a><span data-ttu-id="0b188-102">Operação PrepareQubit</span><span class="sxs-lookup"><span data-stu-id="0b188-102">PrepareQubit operation</span></span>

<span data-ttu-id="0b188-103">Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="0b188-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="0b188-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0b188-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="0b188-105">PrepareQubit foi preterido.</span><span class="sxs-lookup"><span data-stu-id="0b188-105">PrepareQubit has been deprecated.</span></span> <span data-ttu-id="0b188-106">Use <xref:Microsoft.Quantum.Preparation.PreparePauliEigenstate> em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="0b188-106">Please use <xref:Microsoft.Quantum.Preparation.PreparePauliEigenstate> instead.</span></span>

<span data-ttu-id="0b188-107">Prepara um qubit no eigenstate + 1 ( `Zero` ) do operador Pauli fornecido.</span><span class="sxs-lookup"><span data-stu-id="0b188-107">Prepares a qubit in the +1 (`Zero`) eigenstate of the given Pauli operator.</span></span>
<span data-ttu-id="0b188-108">Se o operador Identity for fornecido, o qubit será preparado no estado de forma máxima mista.</span><span class="sxs-lookup"><span data-stu-id="0b188-108">If the identity operator is given, then the qubit is prepared in the maximally mixed state.</span></span>

<span data-ttu-id="0b188-109">Se o qubit estava inicialmente no estado $ \ket {0} $, essa operação prepara o qubit na eigenstate $ + $1 de um determinado operador Pauli, ou, para `PauliI` , no estado máximo misto em vez disso (consulte <xref:microsoft.quantum.preparation.preparesinglequbitidentity> ).</span><span class="sxs-lookup"><span data-stu-id="0b188-109">If the qubit was initially in the $\ket{0}$ state, this operation prepares the qubit in the $+1$ eigenstate of a given Pauli operator, or, for `PauliI`, in the maximally mixed state instead (see <xref:microsoft.quantum.preparation.preparesinglequbitidentity>).</span></span>

<span data-ttu-id="0b188-110">Se o qubit estava em um estado diferente de $ \ket {0} $, essa operação aplica os seguintes Gates: $H $ para `PauliX` , $HS $ para `PauliY` , $I $ para `PauliZ` e <xref:microsoft.quantum.preparation.preparesinglequbitidentity> para `PauliI` .</span><span class="sxs-lookup"><span data-stu-id="0b188-110">If the qubit was in a state other than $\ket{0}$, this operation applies the following gates: $H$ for `PauliX`, $HS$ for `PauliY`, $I$ for `PauliZ` and <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI`.</span></span>

```qsharp
operation PrepareQubit (basis : Pauli, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="0b188-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="0b188-111">Input</span></span>

### <a name="basis--pauli"></a><span data-ttu-id="0b188-112">base: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="0b188-112">basis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="0b188-113">Um operador Pauli $P $.</span><span class="sxs-lookup"><span data-stu-id="0b188-113">A Pauli operator $P$.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="0b188-114">qubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="0b188-114">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="0b188-115">Um qubit a ser preparado.</span><span class="sxs-lookup"><span data-stu-id="0b188-115">A qubit to be prepared.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0b188-116">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0b188-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

