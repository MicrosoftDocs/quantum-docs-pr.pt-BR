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
# <a name="classical-mathematical-functions"></a>Funções matemáticas clássicas #

Essas funções são usadas principalmente para trabalhar com os tipos de dados internos Q # `Int`, `Double`e `Range`.

A operação de <xref:microsoft.quantum.intrinsic.random> tem `(Double[] => Int)`de assinatura.
Ele usa uma matriz de duplicatas como entrada e retorna um índice selecionado aleatoriamente para a matriz como um `Int`.
A probabilidade de selecionar um índice específico é proporcional ao valor do elemento de matriz nesse índice. n elementos da matriz que são iguais a zero são ignorados e seus índices nunca são retornados.
Se qualquer elemento de matriz for menor que zero, ou se nenhum elemento de matriz for maior que zero, a operação falhará.
