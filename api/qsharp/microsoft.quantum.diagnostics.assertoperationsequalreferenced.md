---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced
title: Operação AssertOperationsEqualReferenced
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualReferenced
qsharp.summary: >-
  Given two operations, asserts that they act identically for all input states.

  This assertion is implemented by using the Choi–Jamiołkowski isomorphism to reduce the assertion to one of a qubit state assertion on two entangled registers. Thus, this operation needs only a single call to each operation being tested, but requires twice as many qubits to be allocated. This assertion can be used to ensure, for instance, that an optimized version of an operation acts identically to its naïve implementation, or that an operation which acts on a range of non-quantum inputs agrees with known cases.
ms.openlocfilehash: a3e8791321b4f2ca1885dffeb92c7b13e5491a32
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693549"
---
# <a name="assertoperationsequalreferenced-operation"></a><span data-ttu-id="abc76-102">Operação AssertOperationsEqualReferenced</span><span class="sxs-lookup"><span data-stu-id="abc76-102">AssertOperationsEqualReferenced operation</span></span>

<span data-ttu-id="abc76-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="abc76-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="abc76-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="abc76-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="abc76-105">Dadas duas operações, afirma que elas agem de forma idêntica para todos os Estados de entrada.</span><span class="sxs-lookup"><span data-stu-id="abc76-105">Given two operations, asserts that they act identically for all input states.</span></span>

<span data-ttu-id="abc76-106">Essa declaração é implementada usando o Choi – Jamiołkowski isomorphism para reduzir a asserção para uma de uma declaração de estado qubit em dois registros de confusas.</span><span class="sxs-lookup"><span data-stu-id="abc76-106">This assertion is implemented by using the Choi–Jamiołkowski isomorphism to reduce the assertion to one of a qubit state assertion on two entangled registers.</span></span>
<span data-ttu-id="abc76-107">Portanto, essa operação precisa apenas de uma única chamada para cada operação que está sendo testada, mas requer duas vezes mais qubits a ser alocada.</span><span class="sxs-lookup"><span data-stu-id="abc76-107">Thus, this operation needs only a single call to each operation being tested, but requires twice as many qubits to be allocated.</span></span>
<span data-ttu-id="abc76-108">Essa declaração pode ser usada para garantir, por exemplo, que uma versão otimizada de uma operação atue de forma idêntica à sua implementação ingênua ou que uma operação que atue em uma variedade de entradas não Quantum concorde com casos conhecidos.</span><span class="sxs-lookup"><span data-stu-id="abc76-108">This assertion can be used to ensure, for instance, that an optimized version of an operation acts identically to its naïve implementation, or that an operation which acts on a range of non-quantum inputs agrees with known cases.</span></span>

```qsharp
operation AssertOperationsEqualReferenced (nQubits : Int, actual : (Qubit[] => Unit), expected : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="abc76-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="abc76-109">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="abc76-110">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="abc76-110">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="abc76-111">Número de qubits a serem passadas para cada operação.</span><span class="sxs-lookup"><span data-stu-id="abc76-111">Number of qubits to pass to each operation.</span></span>


### <a name="actual--qubit--unit"></a><span data-ttu-id="abc76-112">real: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de></span><span class="sxs-lookup"><span data-stu-id="abc76-112">actual : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="abc76-113">Operação a ser testada.</span><span class="sxs-lookup"><span data-stu-id="abc76-113">Operation to be tested.</span></span>


### <a name="expected--qubit--unit-adj"></a><span data-ttu-id="abc76-114">esperado: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => adj da [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="abc76-114">expected : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="abc76-115">Operação que define o comportamento esperado para a operação em teste.</span><span class="sxs-lookup"><span data-stu-id="abc76-115">Operation defining the expected behavior for the operation under test.</span></span>



## <a name="output--unit"></a><span data-ttu-id="abc76-116">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="abc76-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="abc76-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="abc76-117">Remarks</span></span>

<span data-ttu-id="abc76-118">Esta operação requer que a operação que está modelando o comportamento esperado seja de modo adjacente, para que o inverso possa ser executado apenas no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="abc76-118">This operation requires that the operation modeling the expected behavior is adjointable, so that the inverse can be performed on the target register alone.</span></span>
<span data-ttu-id="abc76-119">Formalmente, é possível especificar uma operação de transpoção, o que ameniza esse requisito, mas a operação de transpoção não está em geral fisicamente realizable para operações Quantum arbitrárias e, portanto, não é incluída aqui como uma opção.</span><span class="sxs-lookup"><span data-stu-id="abc76-119">Formally, one can specify a transpose operation, which relaxes this requirement, but the transpose operation is not in general physically realizable for arbitrary quantum operations and thus is not included here as an option.</span></span>