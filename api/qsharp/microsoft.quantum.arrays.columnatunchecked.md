---
uid: Microsoft.Quantum.Arrays.ColumnAtUnchecked
title: Função ColumnAtUnchecked
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAtUnchecked
qsharp.summary: This function does not check for matrix shape
ms.openlocfilehash: 17211c1ae1fe12fcadf34a9411f9b0cf0cdcab50
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694506"
---
# <a name="columnatunchecked-function"></a><span data-ttu-id="13115-102">Função ColumnAtUnchecked</span><span class="sxs-lookup"><span data-stu-id="13115-102">ColumnAtUnchecked function</span></span>

<span data-ttu-id="13115-103">Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="13115-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="13115-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="13115-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="13115-105">Esta função não verifica a forma de matriz</span><span class="sxs-lookup"><span data-stu-id="13115-105">This function does not check for matrix shape</span></span>

```qsharp
function ColumnAtUnchecked<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="13115-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="13115-106">Description</span></span>

<span data-ttu-id="13115-107">Essa função pode ser usada em outras funções multidimensionais, que já verificam a matriz de entrada em busca de uma forma retangular válida.</span><span class="sxs-lookup"><span data-stu-id="13115-107">This function can be used in other multidimensional functions, which already check the input matrix for a valid rectangular shape.</span></span>

## <a name="input"></a><span data-ttu-id="13115-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="13115-108">Input</span></span>

### <a name="column--int"></a><span data-ttu-id="13115-109">coluna: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="13115-109">column : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="matrix--t"></a><span data-ttu-id="13115-110">matriz: t [] []</span><span class="sxs-lookup"><span data-stu-id="13115-110">matrix : 'T[][]</span></span>





## <a name="output--t"></a><span data-ttu-id="13115-111">Saída: ' T' []</span><span class="sxs-lookup"><span data-stu-id="13115-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="13115-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="13115-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="13115-113">T'</span><span class="sxs-lookup"><span data-stu-id="13115-113">'T</span></span>

