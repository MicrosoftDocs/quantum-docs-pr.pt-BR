---
title: Matemática nas Q# bibliotecas padrão
description: Saiba mais sobre as funções matemáticas clássicas nas Q# bibliotecas padrão que são usadas com os tipos de dados internos.
author: cgranade
uid: microsoft.quantum.libraries.math
ms.author: chgranad
ms.topic: article
no-loc:
- Q#
- $$v
ms.openlocfilehash: 6de1574341d67c569cd2f040ec533e263fdd386e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92692064"
---
# <a name="classical-mathematical-functions"></a>Funções matemáticas clássicas #

Essas funções são usadas principalmente para trabalhar com os Q# tipos de dados internos `Int` , `Double` e `Range` .

A <xref:Microsoft.Quantum.Intrinsic.Random> operação tem assinatura `(Double[] => Int)` .
Ele usa uma matriz de duplicatas como entrada e retorna um índice selecionado aleatoriamente para a matriz como um `Int` .
A probabilidade de selecionar um índice específico é proporcional ao valor do elemento de matriz nesse índice. n elementos da matriz que são iguais a zero são ignorados e seus índices nunca são retornados.
Se qualquer elemento de matriz for menor que zero, ou se nenhum elemento de matriz for maior que zero, a operação falhará.
