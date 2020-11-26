---
uid: Microsoft.Quantum.Canon.NoOp
title: Operação NoOp
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: NoOp
qsharp.summary: Performs the identity operation (no-op) on an argument.
ms.openlocfilehash: 35b6b62cab35f941f04b150dcca763457ddaa084
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205959"
---
# <a name="noop-operation"></a><span data-ttu-id="bda0c-102">Operação NoOp</span><span class="sxs-lookup"><span data-stu-id="bda0c-102">NoOp operation</span></span>

<span data-ttu-id="bda0c-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="bda0c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="bda0c-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="bda0c-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="bda0c-105">Executa a operação de identidade (não op) em um argumento.</span><span class="sxs-lookup"><span data-stu-id="bda0c-105">Performs the identity operation (no-op) on an argument.</span></span>

```qsharp
operation NoOp<'T> (input : 'T) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="bda0c-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="bda0c-106">Description</span></span>

<span data-ttu-id="bda0c-107">Essa operação usa um valor de qualquer tipo e não faz nada a ele.</span><span class="sxs-lookup"><span data-stu-id="bda0c-107">This operation takes a value of any type and does nothing to it.</span></span>
<span data-ttu-id="bda0c-108">Isso pode ser útil sempre que uma entrada de um tipo de operação é esperada, mas nenhuma ação deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="bda0c-108">This can be useful whenever an input of an operation type is expected, but no action should be taken.</span></span>
<span data-ttu-id="bda0c-109">Por exemplo, se uma determinada síndrome de correção de erro indicar que nenhum erro ocorreu, `NoOp<Qubit[]>` pode ser o procedimento de recuperação correto.</span><span class="sxs-lookup"><span data-stu-id="bda0c-109">For instance, if a particular error correction syndrome indicates that no error has occurred, `NoOp<Qubit[]>` may be the correct recovery procedure.</span></span>
<span data-ttu-id="bda0c-110">Da mesma forma, se uma operação espera um procedimento de preparação de estado como entrada, `NoOp<Qubit[]>` pode ser usada para preparar o estado $ \ket{0 \cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="bda0c-110">Similarly, if an operation expects a state preparation procedure as input, `NoOp<Qubit[]>` can be used to prepare the state $\ket{0 \cdots 0}$.</span></span>

## <a name="input"></a><span data-ttu-id="bda0c-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="bda0c-111">Input</span></span>

### <a name="input--t"></a><span data-ttu-id="bda0c-112">entrada: ' t</span><span class="sxs-lookup"><span data-stu-id="bda0c-112">input : 'T</span></span>

<span data-ttu-id="bda0c-113">Um valor a ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="bda0c-113">A value to be ignored.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bda0c-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bda0c-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="bda0c-115">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="bda0c-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="bda0c-116">T'</span><span class="sxs-lookup"><span data-stu-id="bda0c-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="bda0c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="bda0c-117">Remarks</span></span>

<span data-ttu-id="bda0c-118">Em quase todos os casos, o parâmetro de tipo para `NoOp` precisa ser especificado explicitamente.</span><span class="sxs-lookup"><span data-stu-id="bda0c-118">In almost all cases, the type parameter for `NoOp` needs to be specified explicitly.</span></span> <span data-ttu-id="bda0c-119">Por exemplo, `NoOp<Qubit>` é idêntico a <xref:microsoft.quantum.intrinsic.i> .</span><span class="sxs-lookup"><span data-stu-id="bda0c-119">For instance, `NoOp<Qubit>` is identical to <xref:microsoft.quantum.intrinsic.i>.</span></span>

## <a name="see-also"></a><span data-ttu-id="bda0c-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="bda0c-120">See Also</span></span>

- [<span data-ttu-id="bda0c-121">Microsoft. Quantum. intrínseca. I</span><span class="sxs-lookup"><span data-stu-id="bda0c-121">Microsoft.Quantum.Intrinsic.I</span></span>](xref:Microsoft.Quantum.Intrinsic.I)