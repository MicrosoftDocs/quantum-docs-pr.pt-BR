---
uid: Microsoft.Quantum.Canon.ControlledOnBitString
title: Função ControlledOnBitString
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnBitString
qsharp.summary: Returns a unitary operation that applies an oracle on the target register if the control register state corresponds to a specified bit mask.
ms.openlocfilehash: 9435406506fc99fe211f5dce628b21c18ee4f9fe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216652"
---
# <a name="controlledonbitstring-function"></a><span data-ttu-id="3fc01-102">Função ControlledOnBitString</span><span class="sxs-lookup"><span data-stu-id="3fc01-102">ControlledOnBitString function</span></span>

<span data-ttu-id="3fc01-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3fc01-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3fc01-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3fc01-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3fc01-105">Retorna uma operação unitário que aplica um Oracle no registro de destino se o estado de registro de controle corresponder a uma máscara de bits especificada.</span><span class="sxs-lookup"><span data-stu-id="3fc01-105">Returns a unitary operation that applies an oracle on the target register if the control register state corresponds to a specified bit mask.</span></span>

```qsharp
function ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="description"></a><span data-ttu-id="3fc01-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="3fc01-106">Description</span></span>

<span data-ttu-id="3fc01-107">A saída dessa função é uma operação que pode ser representada por uma transformação unitário $U $ de modo que \begin{align} U \ket{b_0 b_1 \cdots b_ {n-1}} \ket{\psi} = \ket{b_0 b_1 \cdots b_ {n-1}} \otimes \begin{cases} V \ket{\psi} & \textrm{if} (b_0 b_1 \cdots b_ {n-1}) = \texttt{bits} \\ \\ \ket{\psi} & \textrm{otherwise} \end{cases}, \end{align} em que $V $ é uma transformação unitário que representa a ação da `oracle` operação.</span><span class="sxs-lookup"><span data-stu-id="3fc01-107">The output of this function is an operation that can be represented by a unitary transformation $U$ such that \begin{align} U \ket{b_0 b_1 \cdots b_{n - 1}} \ket{\psi} = \ket{b_0 b_1 \cdots b_{n-1}} \otimes \begin{cases} V \ket{\psi} & \textrm{if} (b_0 b_1 \cdots b_{n - 1}) = \texttt{bits} \\\\ \ket{\psi} & \textrm{otherwise} \end{cases}, \end{align} where $V$ is a unitary transformation that represents the action of the `oracle` operation.</span></span>

## <a name="input"></a><span data-ttu-id="3fc01-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="3fc01-108">Input</span></span>

### <a name="bits--bool"></a><span data-ttu-id="3fc01-109">bits: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="3fc01-109">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="3fc01-110">A cadeia de caracteres de bits para controlar a operação unitário especificada.</span><span class="sxs-lookup"><span data-stu-id="3fc01-110">The bit string to control the given unitary operation on.</span></span>


### <a name="oracle--t--unit--is-adj--ctl"></a><span data-ttu-id="3fc01-111">Oracle: T' = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="3fc01-111">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="3fc01-112">A operação unitário a ser aplicada no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="3fc01-112">The unitary operation to be applied on the target register.</span></span>



## <a name="output--qubitt--unit--is-adj--ctl"></a><span data-ttu-id="3fc01-113">Saída: ([qubit](xref:microsoft.quantum.lang-ref.qubit)[], t) => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj + CTL</span><span class="sxs-lookup"><span data-stu-id="3fc01-113">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="3fc01-114">Uma operação unitário que se aplica ao `oracle` registro de destino se o estado de registro de controle corresponder à máscara de bits `bits` .</span><span class="sxs-lookup"><span data-stu-id="3fc01-114">A unitary operation that applies `oracle` on the target register if the control register state corresponds to the bit mask `bits`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="3fc01-115">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="3fc01-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3fc01-116">T'</span><span class="sxs-lookup"><span data-stu-id="3fc01-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="3fc01-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3fc01-117">Remarks</span></span>

<span data-ttu-id="3fc01-118">O padrão fornecido por `bits` pode ser menor que `controlRegister` , nesse caso, qubits de controle adicional são ignorados (ou seja, nenhum controlado em $ \ket {0} $ nem $ \ket {1} $).</span><span class="sxs-lookup"><span data-stu-id="3fc01-118">The pattern given by `bits` may be shorter than `controlRegister`, in which case additional control qubits are ignored (that is, neither controlled on $\ket{0}$ nor $\ket{1}$).</span></span>
<span data-ttu-id="3fc01-119">Se `bits` for maior que `controlRegister` , um erro será gerado.</span><span class="sxs-lookup"><span data-stu-id="3fc01-119">If `bits` is longer than `controlRegister`, an error is raised.</span></span>

<span data-ttu-id="3fc01-120">Dada uma matriz booliana `bits` e uma operação unitário `oracle` , a saída dessa função é uma operação que executa as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="3fc01-120">Given a Boolean array `bits` and a unitary operation `oracle`, the output of this function is an operation that performs the following steps:</span></span>

* <span data-ttu-id="3fc01-121">Aplique uma `X` operação a cada qubit do registro de controle que corresponda ao `false` elemento de `bits` ;</span><span class="sxs-lookup"><span data-stu-id="3fc01-121">apply an `X` operation to each qubit of the control register that corresponds to `false` element of the `bits`;</span></span>
* <span data-ttu-id="3fc01-122">aplicar `Controlled oracle` aos registros de destino e controle;</span><span class="sxs-lookup"><span data-stu-id="3fc01-122">apply `Controlled oracle` to the control and target registers;</span></span>
* <span data-ttu-id="3fc01-123">Aplique uma `X` operação a cada qubit do registro de controle que corresponde ao `false` elemento de `bits` novamente para retornar o registro de controle para o estado original.</span><span class="sxs-lookup"><span data-stu-id="3fc01-123">apply an `X` operation to each qubit of the control register that corresponds to `false` element of the `bits` again to return the control register to the original state.</span></span>

<span data-ttu-id="3fc01-124">A saída de `Controlled` functor é um caso especial de `ControlledOnBitString` onde `bits` é igual a `[true, ..., true]` .</span><span class="sxs-lookup"><span data-stu-id="3fc01-124">The output of the `Controlled` functor is a special case of `ControlledOnBitString` where `bits` is equal to `[true, ..., true]`.</span></span>