---
uid: Microsoft.Quantum.Targeting.RequiresCapability
title: Tipo definido pelo usuário RequiresCapability
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Targeting
qsharp.name: RequiresCapability
qsharp.summary: Compiler-recognized attribute used to mark a callable with the runtime capabilities it requires.
ms.openlocfilehash: 63b1952d402f1bcb81a8f9d0afc3cdf7aa7e5ed8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697042"
---
# <a name="requirescapability-user-defined-type"></a><span data-ttu-id="8273f-102">Tipo definido pelo usuário RequiresCapability</span><span class="sxs-lookup"><span data-stu-id="8273f-102">RequiresCapability user defined type</span></span>

<span data-ttu-id="8273f-103">Namespace: [Microsoft. Quantum. direcionamento](xref:Microsoft.Quantum.Targeting)</span><span class="sxs-lookup"><span data-stu-id="8273f-103">Namespace: [Microsoft.Quantum.Targeting](xref:Microsoft.Quantum.Targeting)</span></span>

<span data-ttu-id="8273f-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8273f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8273f-105">Atributo reconhecido pelo compilador usado para marcar um callable com os recursos de tempo de execução necessários.</span><span class="sxs-lookup"><span data-stu-id="8273f-105">Compiler-recognized attribute used to mark a callable with the runtime capabilities it requires.</span></span>

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype RequiresCapability = (Level : String, Reason : String);
```



## <a name="named-items"></a><span data-ttu-id="8273f-106">Itens nomeados</span><span class="sxs-lookup"><span data-stu-id="8273f-106">Named Items</span></span>

### <a name="level--string"></a><span data-ttu-id="8273f-107">Nível: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="8273f-107">Level : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="8273f-108">O nome do nível de funcionalidade de tempo de execução exigido pelo callable.</span><span class="sxs-lookup"><span data-stu-id="8273f-108">The name of the runtime capability level required by the callable.</span></span>
### <a name="reason--string"></a><span data-ttu-id="8273f-109">Motivo: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="8273f-109">Reason : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="8273f-110">Uma descrição do motivo pelo qual o callable requer esse recurso de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="8273f-110">A description of why the callable requires this runtime capability.</span></span>

## <a name="remarks"></a><span data-ttu-id="8273f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8273f-111">Remarks</span></span>

<span data-ttu-id="8273f-112">Esse atributo é adicionado automaticamente aos chamadores pelo compilador, a menos que uma instância desse atributo já exista no callable.</span><span class="sxs-lookup"><span data-stu-id="8273f-112">This attribute is automatically added to callables by the compiler, unless an instance of this attribute already exists on the callable.</span></span> <span data-ttu-id="8273f-113">Ele não deve ser usado, exceto em casos raros em que o compilador não infere o recurso necessário corretamente.</span><span class="sxs-lookup"><span data-stu-id="8273f-113">It should not be used except in rare cases where the compiler does not infer the required capability correctly.</span></span>

<span data-ttu-id="8273f-114">Abaixo está a lista de nomes de nível de capacidade, em ordem crescente de recursos ou decrescentes de restrições:</span><span class="sxs-lookup"><span data-stu-id="8273f-114">Below is the list of capability level names, in order of increasing capabilities or decreasing restrictions:</span></span>

## `"BasicQuantumFunctionality"`

<span data-ttu-id="8273f-115">Os resultados da medida não podem ser comparados para igualdade.</span><span class="sxs-lookup"><span data-stu-id="8273f-115">Measurement results cannot be compared for equality.</span></span>

## `"BasicMeasurementFeedback"`

<span data-ttu-id="8273f-116">Os resultados da medição podem ser comparados somente para igualdade em expressões condicionais If-Statement em operações.</span><span class="sxs-lookup"><span data-stu-id="8273f-116">Measurement results can be compared for equality only in if-statement conditional expressions in operations.</span></span> <span data-ttu-id="8273f-117">O bloco de uma instrução If que depende de um resultado não pode conter instruções SET para variáveis mutáveis declaradas fora do bloco ou instruções de retorno.</span><span class="sxs-lookup"><span data-stu-id="8273f-117">The block of an if-statement that depends on a result cannot contain set statements for mutable variables declared outside the block, or return statements.</span></span>

## `"FullComputation"`

<span data-ttu-id="8273f-118">Nenhuma restrição de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="8273f-118">No runtime restrictions.</span></span> <span data-ttu-id="8273f-119">Qualquer programa Q # pode ser executado.</span><span class="sxs-lookup"><span data-stu-id="8273f-119">Any Q# program can be executed.</span></span>