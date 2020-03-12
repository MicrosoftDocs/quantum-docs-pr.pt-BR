---
title: Leiame de mídia
description: Dicas sobre como carregar imagens
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 03/04/2020
ms.topic: readme
ms.openlocfilehash: a4922e28a8fc5ddfb4cbc80302e23869154234d8
ms.sourcegitcommit: d61b388651351e5abd4bfe7a672e88b84a6697f8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2020
ms.locfileid: "79024178"
---
# <a name="readme"></a>ARQUIVO LEIAME
**Importante**: para que as imagens sejam renderizadas corretamente no modo escuro, você deve evitar transparências.
- Para arquivos. jpg, você não precisa fazer nada, pois o formato de arquivo não dá suporte a elementos transparentes.
- Para arquivos. png, você deve adicionar um plano de fundo branco ou alterar o valor do canal alfa para 100. A maneira mais fácil de fazer isso no Windows é abrir o arquivo no Paint e salvar, overwritting o arquivo original.
- Para arquivos. svg, você deve adicionar um retângulo branco na camada mais baixa. Você pode fazer isso com Inkscape:
  - Abra o arquivo. svg.
  - Selecione a ferramenta Criador quadrado e desenhe um retângulo branco na parte superior da figura original.
  - Selecione a ferramenta "selecionar e transformar objetos" clicando na seta escura ou pressionando F1.
  - Ao selecionar o retângulo, clique no elemento da barra de ferramentas "seleção inferior para inferior (final)".
  - Ajuste o retângulo com o mouse ou as teclas de direção.
