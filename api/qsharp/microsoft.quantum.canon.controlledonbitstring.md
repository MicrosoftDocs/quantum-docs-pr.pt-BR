---
uid: Microsoft.Quantum.Canon.ControlledOnBitString
title: Função ControlledOnBitString
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnBitString
qsharp.summary: Returns a unitary operation that applies an oracle on the target register if the control register state corresponds to a specified bit mask.
ms.openlocfilehash: ca5a6e116eff187060f7a160e42836b170f0362d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694047"
---
# <a name="controlledonbitstring-function"></a><span data-ttu-id="e8327-102">Função ControlledOnBitString</span><span class="sxs-lookup"><span data-stu-id="e8327-102">ControlledOnBitString function</span></span>

<span data-ttu-id="e8327-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e8327-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e8327-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e8327-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e8327-105">Retorna uma operação unitário que aplica um Oracle no registro de destino se o estado de registro de controle corresponder a uma máscara de bits especificada.</span><span class="sxs-lookup"><span data-stu-id="e8327-105">Returns a unitary operation that applies an oracle on the target register if the control register state corresponds to a specified bit mask.</span></span>

```qsharp
function ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="description"></a><span data-ttu-id="e8327-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="e8327-106">Description</span></span>

<span data-ttu-id="e8327-107">A saída dessa função é uma operação que pode ser representada por uma transformação unitário $U $ de modo que \begin{align} U \ket{b_0 b_1 \cdots b_ {n-1}} \ket{\psi} = \ket{b_0 b_1 \cdots b_ {n-1}} \otimes \begin{cases} V \ket{\psi} & \textrm{if} (b_0 b_1 \cdots b_ {n-1}) = \texttt{bits} \\ \\ \ket{\psi} & \textrm{otherwise} \end{cases}, \end{align} em que $V $ é uma transformação unitário que representa a ação da `oracle` operação.</span><span class="sxs-lookup"><span data-stu-id="e8327-107">The output of this function is an operation that can be represented by a unitary transformation $U$ such that \begin{align} U \ket{b_0 b_1 \cdots b_{n - 1}} \ket{\psi} = \ket{b_0 b_1 \cdots b_{n-1}} \otimes \begin{cases} V \ket{\psi} & \textrm{if} (b_0 b_1 \cdots b_{n - 1}) = \texttt{bits} \\\\ \ket{\psi} & \textrm{otherwise} \end{cases}, \end{align} where $V$ is a unitary transformation that represents the action of the `oracle` operation.</span></span>

## <a name="input"></a><span data-ttu-id="e8327-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="e8327-108">Input</span></span>

### <a name="bits--bool"></a><span data-ttu-id="e8327-109">bits: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="e8327-109">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="e8327-110">A cadeia de caracteres de bits para controlar a operação unitário especificada.</span><span class="sxs-lookup"><span data-stu-id="e8327-110">The bit string to control the given unitary operation on.</span></span>


### <a name="oracle--t--unit-adj--ctl"></a><span data-ttu-id="e8327-111">Oracle: t => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL</span><span class="sxs-lookup"><span data-stu-id="e8327-111">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="e8327-112">A operação unitário a ser aplicada no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="e8327-112">The unitary operation to be applied on the target register.</span></span>



## <a name="output--qubitt--unit-adj--ctl"></a><span data-ttu-id="e8327-113">Saída: ([qubit](xref:microsoft.quantum.lang-ref.qubit)[], t) => [unidade](xref:microsoft.quantum.lang-ref.unit) de ano + CTL</span><span class="sxs-lookup"><span data-stu-id="e8327-113">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="e8327-114">Uma operação unitário que se aplica ao `oracle` registro de destino se o estado de registro de controle corresponder à máscara de bits `bits` .</span><span class="sxs-lookup"><span data-stu-id="e8327-114">A unitary operation that applies `oracle` on the target register if the control register state corresponds to the bit mask `bits`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e8327-115">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="e8327-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e8327-116">T'</span><span class="sxs-lookup"><span data-stu-id="e8327-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="e8327-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8327-117">Remarks</span></span>

<span data-ttu-id="e8327-118">O padrão fornecido por `bits` pode ser menor que `controlRegister` , nesse caso, qubits de controle adicional são ignorados (ou seja, nenhum controlado em $ \ket {0} $ nem $ \ket {1} $).</span><span class="sxs-lookup"><span data-stu-id="e8327-118">The pattern given by `bits` may be shorter than `controlRegister`, in which case additional control qubits are ignored (that is, neither controlled on $\ket{0}$ nor $\ket{1}$).</span></span>
<span data-ttu-id="e8327-119">Se `bits` for maior que `controlRegister` , um erro será gerado.</span><span class="sxs-lookup"><span data-stu-id="e8327-119">If `bits` is longer than `controlRegister`, an error is raised.</span></span>

<span data-ttu-id="e8327-120">Dada uma matriz booliana `bits` e uma operação unitário `oracle` , a saída dessa função é uma operação que executa as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="e8327-120">Given a Boolean array `bits` and a unitary operation `oracle`, the output of this function is an operation that performs the following steps:</span></span>

* <span data-ttu-id="e8327-121">Aplique uma `X` operação a cada qubit do registro de controle que corresponda ao `false` elemento de `bits` ;</span><span class="sxs-lookup"><span data-stu-id="e8327-121">apply an `X` operation to each qubit of the control register that corresponds to `false` element of the `bits`;</span></span>
* <span data-ttu-id="e8327-122">aplicar `Controlled oracle` aos registros de destino e controle;</span><span class="sxs-lookup"><span data-stu-id="e8327-122">apply `Controlled oracle` to the control and target registers;</span></span>
* <span data-ttu-id="e8327-123">Aplique uma `X` operação a cada qubit do registro de controle que corresponde ao `false` elemento de `bits` novamente para retornar o registro de controle para o estado original.</span><span class="sxs-lookup"><span data-stu-id="e8327-123">apply an `X` operation to each qubit of the control register that corresponds to `false` element of the `bits` again to return the control register to the original state.</span></span>

<span data-ttu-id="e8327-124">A saída de `Controlled` functor é um caso especial de `ControlledOnBitString` onde `bits` é igual a `[true, ..., true]` .</span><span class="sxs-lookup"><span data-stu-id="e8327-124">The output of the `Controlled` functor is a special case of `ControlledOnBitString` where `bits` is equal to `[true, ..., true]`.</span></span>