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
ms.openlocfilehash: 55b1ef70eed1eb47ab0c6b30e2b8203c38c9a67a
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833605"
---
# <a name="classical-mathematical-functions"></a>Funções matemáticas clássicas #

Essas funções são usadas principalmente para trabalhar com os Q# tipos de dados internos `Int` , `Double` e `Range` .

A <xref:microsoft.quantum.intrinsic.random> operação tem assinatura `(Double[] => Int)` .
Ele usa uma matriz de duplicatas como entrada e retorna um índice selecionado aleatoriamente para a matriz como um `Int` .
A probabilidade de selecionar um índice específico é proporcional ao valor do elemento de matriz nesse índice. n elementos da matriz que são iguais a zero são ignorados e seus índices nunca são retornados.
Se qualquer elemento de matriz for menor que zero, ou se nenhum elemento de matriz for maior que zero, a operação falhará.
