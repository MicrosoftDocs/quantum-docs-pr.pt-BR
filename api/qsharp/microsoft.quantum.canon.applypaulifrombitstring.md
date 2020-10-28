---
uid: Microsoft.Quantum.Canon.ApplyPauliFromBitString
title: Operação ApplyPauliFromBitString
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauliFromBitString
qsharp.summary: Applies a Pauli operator on each qubit in an array if the corresponding bit of a Boolean array matches a given input.
ms.openlocfilehash: 09754accb92c1339b781003e5722e3c8f5884e6f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694242"
---
# <a name="applypaulifrombitstring-operation"></a><span data-ttu-id="10881-102">Operação ApplyPauliFromBitString</span><span class="sxs-lookup"><span data-stu-id="10881-102">ApplyPauliFromBitString operation</span></span>

<span data-ttu-id="10881-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="10881-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="10881-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="10881-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="10881-105">Aplica um operador Pauli em cada qubit em uma matriz se o bit correspondente de uma matriz booliana corresponde a uma determinada entrada.</span><span class="sxs-lookup"><span data-stu-id="10881-105">Applies a Pauli operator on each qubit in an array if the corresponding bit of a Boolean array matches a given input.</span></span>

```qsharp
operation ApplyPauliFromBitString (pauli : Pauli, bitApply : Bool, bits : Bool[], qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="10881-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="10881-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="10881-107">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="10881-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="10881-108">Operador Pauli a ser aplicado a `qubits[idx]` Where `bitsApply == bits[idx]`</span><span class="sxs-lookup"><span data-stu-id="10881-108">Pauli operator to apply to `qubits[idx]` where `bitsApply == bits[idx]`</span></span>


### <a name="bitapply--bool"></a><span data-ttu-id="10881-109">bitApply: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="10881-109">bitApply : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="10881-110">aplicar Pauli se bit for esse valor</span><span class="sxs-lookup"><span data-stu-id="10881-110">apply Pauli if bit is this value</span></span>


### <a name="bits--bool"></a><span data-ttu-id="10881-111">bits: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="10881-111">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="10881-112">Registro booliano que especifica quais qubit correspondentes no `qubits` devem ser operados em</span><span class="sxs-lookup"><span data-stu-id="10881-112">Boolean register specifying which corresponding qubit in `qubits` should be operated on</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="10881-113">qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="10881-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="10881-114">Quantum registra-se para aplicar seletivamente o operador Pauli especificado</span><span class="sxs-lookup"><span data-stu-id="10881-114">Quantum register on which to selectively apply the specified Pauli operator</span></span>



## <a name="output--unit"></a><span data-ttu-id="10881-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="10881-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="10881-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="10881-116">Remarks</span></span>

<span data-ttu-id="10881-117">A matriz booliana e o registro do Quantum devem ser de comprimento igual.</span><span class="sxs-lookup"><span data-stu-id="10881-117">The Boolean array and the quantum register must be of equal length.</span></span>