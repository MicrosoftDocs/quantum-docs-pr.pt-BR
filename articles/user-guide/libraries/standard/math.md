---
title: 'Matemática nas :::no-loc(Q#)::: bibliotecas padrão'
description: 'Saiba mais sobre as funções matemáticas clássicas nas :::no-loc(Q#)::: bibliotecas padrão que são usadas com os tipos de dados internos.'
author: cgranade
uid: microsoft.quantum.libraries.math
ms.author: chgranad
ms.topic: article
no-loc:
- ':::no-loc(Q#):::'
- ':::no-loc($$v):::'
ms.openlocfilehash: 6de1574341d67c569cd2f040ec533e263fdd386e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92692064"
---
# <a name="classical-mathematical-functions"></a><span data-ttu-id="79456-103">Funções matemáticas clássicas</span><span class="sxs-lookup"><span data-stu-id="79456-103">Classical Mathematical Functions</span></span> #

<span data-ttu-id="79456-104">Essas funções são usadas principalmente para trabalhar com os :::no-loc(Q#)::: tipos de dados internos `Int` , `Double` e `Range` .</span><span class="sxs-lookup"><span data-stu-id="79456-104">These functions are primarily used to work with the :::no-loc(Q#)::: built-in data types `Int`, `Double`, and `Range`.</span></span>

<span data-ttu-id="79456-105">A <xref:Microsoft.Quantum.Intrinsic.Random> operação tem assinatura `(Double[] => Int)` .</span><span class="sxs-lookup"><span data-stu-id="79456-105">The <xref:Microsoft.Quantum.Intrinsic.Random> operation has signature `(Double[] => Int)`.</span></span>
<span data-ttu-id="79456-106">Ele usa uma matriz de duplicatas como entrada e retorna um índice selecionado aleatoriamente para a matriz como um `Int` .</span><span class="sxs-lookup"><span data-stu-id="79456-106">It takes an array of doubles as input, and returns a randomly-selected index into the array as an `Int`.</span></span>
<span data-ttu-id="79456-107">A probabilidade de selecionar um índice específico é proporcional ao valor do elemento de matriz nesse índice.</span><span class="sxs-lookup"><span data-stu-id="79456-107">The probability of selecting a specific index is proportional to the value of the array element at that index.</span></span> <span data-ttu-id="79456-108">n elementos da matriz que são iguais a zero são ignorados e seus índices nunca são retornados.</span><span class="sxs-lookup"><span data-stu-id="79456-108">n Array elements that are equal to zero are ignored and their indices are never returned.</span></span>
<span data-ttu-id="79456-109">Se qualquer elemento de matriz for menor que zero, ou se nenhum elemento de matriz for maior que zero, a operação falhará.</span><span class="sxs-lookup"><span data-stu-id="79456-109">If any array element is less than zero, or if no array element is greater than zero, then the operation fails.</span></span>
