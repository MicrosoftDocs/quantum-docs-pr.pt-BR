---
title: Matemática nas Q# bibliotecas padrão
description: Saiba mais sobre as funções matemáticas clássicas nas Q# bibliotecas padrão que são usadas com os tipos de dados internos.
author: cgranade
uid: microsoft.quantum.libraries.math
ms.author: chgranad@microsoft.com
ms.topic: article
no-loc:
- Q#
- $$v
ms.openlocfilehash: 4a3747eaa2c91e482ded3af1279a0e40d922bfb3
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868416"
---
# <a name="classical-mathematical-functions"></a><span data-ttu-id="f32e4-103">Funções matemáticas clássicas</span><span class="sxs-lookup"><span data-stu-id="f32e4-103">Classical Mathematical Functions</span></span> #

<span data-ttu-id="f32e4-104">Essas funções são usadas principalmente para trabalhar com os Q# tipos de dados internos `Int` , `Double` e `Range` .</span><span class="sxs-lookup"><span data-stu-id="f32e4-104">These functions are primarily used to work with the Q# built-in data types `Int`, `Double`, and `Range`.</span></span>

<span data-ttu-id="f32e4-105">A <xref:microsoft.quantum.intrinsic.random> operação tem assinatura `(Double[] => Int)` .</span><span class="sxs-lookup"><span data-stu-id="f32e4-105">The <xref:microsoft.quantum.intrinsic.random> operation has signature `(Double[] => Int)`.</span></span>
<span data-ttu-id="f32e4-106">Ele usa uma matriz de duplicatas como entrada e retorna um índice selecionado aleatoriamente para a matriz como um `Int` .</span><span class="sxs-lookup"><span data-stu-id="f32e4-106">It takes an array of doubles as input, and returns a randomly-selected index into the array as an `Int`.</span></span>
<span data-ttu-id="f32e4-107">A probabilidade de selecionar um índice específico é proporcional ao valor do elemento de matriz nesse índice.</span><span class="sxs-lookup"><span data-stu-id="f32e4-107">The probability of selecting a specific index is proportional to the value of the array element at that index.</span></span> <span data-ttu-id="f32e4-108">n elementos da matriz que são iguais a zero são ignorados e seus índices nunca são retornados.</span><span class="sxs-lookup"><span data-stu-id="f32e4-108">n Array elements that are equal to zero are ignored and their indices are never returned.</span></span>
<span data-ttu-id="f32e4-109">Se qualquer elemento de matriz for menor que zero, ou se nenhum elemento de matriz for maior que zero, a operação falhará.</span><span class="sxs-lookup"><span data-stu-id="f32e4-109">If any array element is less than zero, or if no array element is greater than zero, then the operation fails.</span></span>
