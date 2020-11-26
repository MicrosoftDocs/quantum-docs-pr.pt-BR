---
uid: Microsoft.Quantum.Targeting.RequiresCapability
title: Tipo definido pelo usuário RequiresCapability
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Targeting
qsharp.name: RequiresCapability
qsharp.summary: Compiler-recognized attribute used to mark a callable with the runtime capabilities it requires.
ms.openlocfilehash: 0d9e4eb294b3ce91058c204d5dba37ea29b4ac28
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96231000"
---
# <a name="requirescapability-user-defined-type"></a><span data-ttu-id="a6b3c-102">Tipo definido pelo usuário RequiresCapability</span><span class="sxs-lookup"><span data-stu-id="a6b3c-102">RequiresCapability user defined type</span></span>

<span data-ttu-id="a6b3c-103">Namespace: [Microsoft. Quantum. direcionamento](xref:Microsoft.Quantum.Targeting)</span><span class="sxs-lookup"><span data-stu-id="a6b3c-103">Namespace: [Microsoft.Quantum.Targeting](xref:Microsoft.Quantum.Targeting)</span></span>

<span data-ttu-id="a6b3c-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="a6b3c-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="a6b3c-105">Atributo reconhecido pelo compilador usado para marcar um callable com os recursos de tempo de execução necessários.</span><span class="sxs-lookup"><span data-stu-id="a6b3c-105">Compiler-recognized attribute used to mark a callable with the runtime capabilities it requires.</span></span>

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype RequiresCapability = (Level : String, Reason : String);
```



## <a name="named-items"></a><span data-ttu-id="a6b3c-106">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="a6b3c-106">Named Items</span></span>

### <a name="level--string"></a><span data-ttu-id="a6b3c-107">Nível: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="a6b3c-107">Level : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="a6b3c-108">O nome do nível de funcionalidade de tempo de execução exigido pelo callable.</span><span class="sxs-lookup"><span data-stu-id="a6b3c-108">The name of the runtime capability level required by the callable.</span></span>
### <a name="reason--string"></a><span data-ttu-id="a6b3c-109">Motivo: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="a6b3c-109">Reason : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="a6b3c-110">Uma descrição do motivo pelo qual o callable requer esse recurso de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="a6b3c-110">A description of why the callable requires this runtime capability.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6b3c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6b3c-111">Remarks</span></span>

<span data-ttu-id="a6b3c-112">Esse atributo é adicionado automaticamente aos chamadores pelo compilador, a menos que uma instância desse atributo já exista no callable.</span><span class="sxs-lookup"><span data-stu-id="a6b3c-112">This attribute is automatically added to callables by the compiler, unless an instance of this attribute already exists on the callable.</span></span> <span data-ttu-id="a6b3c-113">Ele não deve ser usado, exceto em casos raros em que o compilador não infere o recurso necessário corretamente.</span><span class="sxs-lookup"><span data-stu-id="a6b3c-113">It should not be used except in rare cases where the compiler does not infer the required capability correctly.</span></span>

<span data-ttu-id="a6b3c-114">Abaixo está a lista de nomes de nível de capacidade, em ordem crescente de recursos ou decrescentes de restrições:</span><span class="sxs-lookup"><span data-stu-id="a6b3c-114">Below is the list of capability level names, in order of increasing capabilities or decreasing restrictions:</span></span>

## `"BasicQuantumFunctionality"`

<span data-ttu-id="a6b3c-115">Os resultados da medida não podem ser comparados para igualdade.</span><span class="sxs-lookup"><span data-stu-id="a6b3c-115">Measurement results cannot be compared for equality.</span></span>

## `"BasicMeasurementFeedback"`

<span data-ttu-id="a6b3c-116">Os resultados da medição podem ser comparados somente para igualdade em expressões condicionais If-Statement em operações.</span><span class="sxs-lookup"><span data-stu-id="a6b3c-116">Measurement results can be compared for equality only in if-statement conditional expressions in operations.</span></span> <span data-ttu-id="a6b3c-117">O bloco de uma instrução If que depende de um resultado não pode conter instruções SET para variáveis mutáveis declaradas fora do bloco ou instruções de retorno.</span><span class="sxs-lookup"><span data-stu-id="a6b3c-117">The block of an if-statement that depends on a result cannot contain set statements for mutable variables declared outside the block, or return statements.</span></span>

## `"FullComputation"`

<span data-ttu-id="a6b3c-118">Nenhuma restrição de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="a6b3c-118">No runtime restrictions.</span></span> <span data-ttu-id="a6b3c-119">Qualquer programa Q # pode ser executado.</span><span class="sxs-lookup"><span data-stu-id="a6b3c-119">Any Q# program can be executed.</span></span>