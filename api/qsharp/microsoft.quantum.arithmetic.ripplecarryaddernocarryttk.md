---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderNoCarryTTK
title: Operação RippleCarryAdderNoCarryTTK
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderNoCarryTTK
qsharp.summary: Reversible, in-place ripple-carry addition of two integers without carry out.
ms.openlocfilehash: 59451b4f5c992f900a27139332059af7427b9b93
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694528"
---
# <a name="ripplecarryaddernocarryttk-operation"></a><span data-ttu-id="fe95b-102">Operação RippleCarryAdderNoCarryTTK</span><span class="sxs-lookup"><span data-stu-id="fe95b-102">RippleCarryAdderNoCarryTTK operation</span></span>

<span data-ttu-id="fe95b-103">Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="fe95b-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="fe95b-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fe95b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fe95b-105">Reversível, ondulado no local, adição de dois inteiros sem execução.</span><span class="sxs-lookup"><span data-stu-id="fe95b-105">Reversible, in-place ripple-carry addition of two integers without carry out.</span></span>

```qsharp
operation RippleCarryAdderNoCarryTTK (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="fe95b-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe95b-106">Description</span></span>

<span data-ttu-id="fe95b-107">Dado dois $n inteiros de $ bit codificados em registros LittleEndian `xs` e `ys` , a operação computa a soma dos dois módulos inteiros módulo $2 ^ n $, em que $n $ é o tamanho do bit das entradas `xs` e `ys` .</span><span class="sxs-lookup"><span data-stu-id="fe95b-107">Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, the operation computes the sum of the two integers modulo $2^n$, where $n$ is the bit size of the inputs `xs` and `ys`.</span></span> <span data-ttu-id="fe95b-108">Ele não computa o bit de execução.</span><span class="sxs-lookup"><span data-stu-id="fe95b-108">It does not compute the carry out bit.</span></span>

## <a name="input"></a><span data-ttu-id="fe95b-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="fe95b-109">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="fe95b-110">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="fe95b-110">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="fe95b-111">LittleEndian qubit registrar o primeiro soma inteiro.</span><span class="sxs-lookup"><span data-stu-id="fe95b-111">LittleEndian qubit register encoding the first integer summand.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="fe95b-112">haves: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="fe95b-112">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="fe95b-113">LittleEndian qubit a codificação do segundo inteiro soma, é modificado para manter o $n $ menos significativo bits da soma.</span><span class="sxs-lookup"><span data-stu-id="fe95b-113">LittleEndian qubit register encoding the second integer summand, is modified to hold the $n$ least significant bits of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fe95b-114">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fe95b-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="fe95b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe95b-115">Remarks</span></span>

<span data-ttu-id="fe95b-116">Esta operação tem a mesma funcionalidade que RippleCarryAdderTTK, mas não retorna o bit de execução.</span><span class="sxs-lookup"><span data-stu-id="fe95b-116">This operation has the same functionality as RippleCarryAdderTTK but does not return the carry bit.</span></span>

## <a name="references"></a><span data-ttu-id="fe95b-117">Referências</span><span class="sxs-lookup"><span data-stu-id="fe95b-117">References</span></span>

- <span data-ttu-id="fe95b-118">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "circuitos de adição Quantum e Fan-out não vinculado", informações de Quantum e computação, Vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="fe95b-118">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530