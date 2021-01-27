---
uid: Microsoft.Quantum.Canon.ApplyControlledOnBitString
title: Operação ApplyControlledOnBitString
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnBitString
qsharp.summary: Applies a unitary operation on the target register, controlled on a a state specified by a given bit mask.
ms.openlocfilehash: 82adc74e23e1d50cb6436176a973fdd1a0eeb3bd
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841939"
---
# <a name="applycontrolledonbitstring-operation"></a><span data-ttu-id="604ed-102">Operação ApplyControlledOnBitString</span><span class="sxs-lookup"><span data-stu-id="604ed-102">ApplyControlledOnBitString operation</span></span>

<span data-ttu-id="604ed-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="604ed-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="604ed-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="604ed-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="604ed-105">Aplica uma operação unitário no registro de destino, controlada em um estado especificado por uma determinada máscara de bits.</span><span class="sxs-lookup"><span data-stu-id="604ed-105">Applies a unitary operation on the target register, controlled on a a state specified by a given bit mask.</span></span>

```qsharp
operation ApplyControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="604ed-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="604ed-106">Input</span></span>

### <a name="bits--bool"></a><span data-ttu-id="604ed-107">bits: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="604ed-107">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="604ed-108">A cadeia de caracteres de bits para controlar a operação unitário especificada.</span><span class="sxs-lookup"><span data-stu-id="604ed-108">The bit string to control the given unitary operation on.</span></span>


### <a name="oracle--t--unit--is-adj--ctl"></a><span data-ttu-id="604ed-109">Oracle: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="604ed-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="604ed-110">A operação unitário a ser aplicada no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="604ed-110">The unitary operation to be applied on the target register.</span></span>


### <a name="controlregister--qubit"></a><span data-ttu-id="604ed-111">controlRegister: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="604ed-111">controlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="604ed-112">Um registro do Quantum que controla a aplicação do `oracle` .</span><span class="sxs-lookup"><span data-stu-id="604ed-112">A quantum register that controls application of `oracle`.</span></span>


### <a name="targetregister--t"></a><span data-ttu-id="604ed-113">targetRegister: ' t</span><span class="sxs-lookup"><span data-stu-id="604ed-113">targetRegister : 'T</span></span>

<span data-ttu-id="604ed-114">O registro de destino a ser passado `oracle` como uma entrada.</span><span class="sxs-lookup"><span data-stu-id="604ed-114">The target register to be passed to `oracle` as an input.</span></span>



## <a name="output--unit"></a><span data-ttu-id="604ed-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="604ed-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="604ed-116">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="604ed-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="604ed-117">T'</span><span class="sxs-lookup"><span data-stu-id="604ed-117">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="604ed-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="604ed-118">Remarks</span></span>

<span data-ttu-id="604ed-119">O padrão fornecido por `bits` pode ser menor que `controlRegister` , nesse caso, qubits de controle adicional são ignorados (ou seja, nenhum controlado em $ \ket {0} $ nem $ \ket {1} $).</span><span class="sxs-lookup"><span data-stu-id="604ed-119">The pattern given by `bits` may be shorter than `controlRegister`, in which case additional control qubits are ignored (that is, neither controlled on $\ket{0}$ nor $\ket{1}$).</span></span>
<span data-ttu-id="604ed-120">Se `bits` for maior que `controlRegister` , um erro será gerado.</span><span class="sxs-lookup"><span data-stu-id="604ed-120">If `bits` is longer than `controlRegister`, an error is raised.</span></span>

<span data-ttu-id="604ed-121">Por exemplo, `bits = [0,1,0,0,1]` significa que `oracle` será aplicado se e somente se `controlRegister` estiver no estado $ \ket {0} \ket {1} \ket {0} \ket {0} \ket {1} $.</span><span class="sxs-lookup"><span data-stu-id="604ed-121">For example, `bits = [0,1,0,0,1]` means that `oracle` is applied if and only if `controlRegister` is in the state $\ket{0}\ket{1}\ket{0}\ket{0}\ket{1}$.</span></span>