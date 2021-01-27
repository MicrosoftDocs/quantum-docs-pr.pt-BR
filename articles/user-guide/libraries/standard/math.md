---
title: Matemática nas Q# bibliotecas padrão
description: Saiba mais sobre as funções matemáticas clássicas nas Q# bibliotecas padrão que são usadas com os tipos de dados internos.
author: cgranade
uid: microsoft.quantum.libraries.math
ms.author: chgranad
ms.topic: conceptual
no-loc:
- Q#
- $$v
ms.openlocfilehash: a2e2656f42213c8ae9e984f63f3ebf4058520532
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853991"
---
# <a name="classical-mathematical-functions"></a><span data-ttu-id="8a8e3-103">Funções matemáticas clássicas</span><span class="sxs-lookup"><span data-stu-id="8a8e3-103">Classical Mathematical Functions</span></span> #

<span data-ttu-id="8a8e3-104">Essas funções são usadas principalmente para trabalhar com os Q# tipos de dados internos `Int` , `Double` e `Range` .</span><span class="sxs-lookup"><span data-stu-id="8a8e3-104">These functions are primarily used to work with the Q# built-in data types `Int`, `Double`, and `Range`.</span></span>

<span data-ttu-id="8a8e3-105">A <xref:Microsoft.Quantum.Intrinsic.Random> operação tem assinatura `(Double[] => Int)` .</span><span class="sxs-lookup"><span data-stu-id="8a8e3-105">The <xref:Microsoft.Quantum.Intrinsic.Random> operation has signature `(Double[] => Int)`.</span></span>
<span data-ttu-id="8a8e3-106">Ele usa uma matriz de duplicatas como entrada e retorna um índice selecionado aleatoriamente para a matriz como um `Int` .</span><span class="sxs-lookup"><span data-stu-id="8a8e3-106">It takes an array of doubles as input, and returns a randomly-selected index into the array as an `Int`.</span></span>
<span data-ttu-id="8a8e3-107">A probabilidade de selecionar um índice específico é proporcional ao valor do elemento de matriz nesse índice.</span><span class="sxs-lookup"><span data-stu-id="8a8e3-107">The probability of selecting a specific index is proportional to the value of the array element at that index.</span></span> <span data-ttu-id="8a8e3-108">n elementos da matriz que são iguais a zero são ignorados e seus índices nunca são retornados.</span><span class="sxs-lookup"><span data-stu-id="8a8e3-108">n Array elements that are equal to zero are ignored and their indices are never returned.</span></span>
<span data-ttu-id="8a8e3-109">Se qualquer elemento de matriz for menor que zero, ou se nenhum elemento de matriz for maior que zero, a operação falhará.</span><span class="sxs-lookup"><span data-stu-id="8a8e3-109">If any array element is less than zero, or if no array element is greater than zero, then the operation fails.</span></span>
