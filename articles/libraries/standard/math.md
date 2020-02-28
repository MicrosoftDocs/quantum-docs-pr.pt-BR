---
title: 'Matemática nas bibliotecas padrão do Q #'
description: 'Saiba mais sobre as funções matemáticas clássicas nas bibliotecas padrão do Q # que são usadas com os tipos de dados internos.'
author: cgranade
uid: microsoft.quantum.libraries.math
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: bec866472abc0d4327cdc570306341375395f492
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906144"
---
# <a name="classical-mathematical-functions"></a><span data-ttu-id="0d8df-103">Funções matemáticas clássicas</span><span class="sxs-lookup"><span data-stu-id="0d8df-103">Classical Mathematical Functions</span></span> #

<span data-ttu-id="0d8df-104">Essas funções são usadas principalmente para trabalhar com os tipos de dados internos Q # `Int`, `Double`e `Range`.</span><span class="sxs-lookup"><span data-stu-id="0d8df-104">These functions are primarily used to work with the Q# built-in data types `Int`, `Double`, and `Range`.</span></span>

<span data-ttu-id="0d8df-105">A operação de <xref:microsoft.quantum.intrinsic.random> tem `(Double[] => Int)`de assinatura.</span><span class="sxs-lookup"><span data-stu-id="0d8df-105">The <xref:microsoft.quantum.intrinsic.random> operation has signature `(Double[] => Int)`.</span></span>
<span data-ttu-id="0d8df-106">Ele usa uma matriz de duplicatas como entrada e retorna um índice selecionado aleatoriamente para a matriz como um `Int`.</span><span class="sxs-lookup"><span data-stu-id="0d8df-106">It takes an array of doubles as input, and returns a randomly-selected index into the array as an `Int`.</span></span>
<span data-ttu-id="0d8df-107">A probabilidade de selecionar um índice específico é proporcional ao valor do elemento de matriz nesse índice.</span><span class="sxs-lookup"><span data-stu-id="0d8df-107">The probability of selecting a specific index is proportional to the value of the array element at that index.</span></span> <span data-ttu-id="0d8df-108">n elementos da matriz que são iguais a zero são ignorados e seus índices nunca são retornados.</span><span class="sxs-lookup"><span data-stu-id="0d8df-108">n Array elements that are equal to zero are ignored and their indices are never returned.</span></span>
<span data-ttu-id="0d8df-109">Se qualquer elemento de matriz for menor que zero, ou se nenhum elemento de matriz for maior que zero, a operação falhará.</span><span class="sxs-lookup"><span data-stu-id="0d8df-109">If any array element is less than zero, or if no array element is greater than zero, then the operation fails.</span></span>
