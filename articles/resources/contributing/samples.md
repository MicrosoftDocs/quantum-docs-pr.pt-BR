---
title: Colaborando com exemplos no Microsoft QDK
description: Saiba como contribuir com código de exemplo para a Microsoft Quantum Development Kit (QDK).
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.samples
no-loc:
- Q#
- $$v
ms.openlocfilehash: 20da0e1765a242c172cc595f03d7791a0e8b8d2d
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867498"
---
# <a name="contributing-samples-to-the-quantum-development-kit"></a>Colaborando com exemplos do kit de desenvolvimento Quantum

Se você estiver interessado em contribuir com código para o [repositório de exemplos](https://github.com/Microsoft/Quantum), obrigado por tornar a comunidade de desenvolvimento do Quantum um lugar melhor!

## <a name="the-quantum-development-kit-samples-repository"></a>O repositório de exemplos do kit de desenvolvimento Quantum

Para ajudá-lo a preparar sua contribuição para ajudar o máximo possível, é útil dar uma olhada rápida em como o repositório de exemplos é apresentado:

```plaintext
microsoft/Quantum
📁 samples/
  📁 algorithms/
    📁 chsh-game/
      📝 CHSHGame.csproj
      📝 Game.qs
      📝 Host.cs
      📝 host.py
      📝 README.md
     ⋮
  📁 arithmetic/
  📁 characterization/
  📁 chemistry/
   ⋮
```

Ou seja, os exemplos no [repositório Microsoft/Quantum](https://github.com/microsoft/Quantum) são divididos por área de assunto em pastas diferentes, como `algorithms/` , `arithmetic/` ou `characterization/` .
Dentro da pasta de cada área de assunto, cada amostra consiste em uma única pasta que coleta tudo o que um usuário precisará para explorar e usar esse exemplo.

## <a name="how-samples-are-structured"></a>Como os exemplos são estruturados

Examinando os arquivos que compõem cada pasta, vamos nos aprofundar no [`algorithms/chsh-game/`](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/chsh-game) exemplo.

| Arquivo              | Descrição                                                |
|-------------------|------------------------------------------------------------|
| `CHSHGame.csproj` | Q#projeto usado para criar o exemplo com o SDK do .NET Core |
| `Game.qs`         | Q#operações e funções para o exemplo                 |
| `Host.cs`         | Programa de host C# usado para executar o exemplo                     |
| `host.py`         | Programa de host Python usado para executar o exemplo                 |
| `README.md`       | Documentação sobre o que o exemplo faz e como usá-lo    |

Nem todos os exemplos terão exatamente o mesmo conjunto de arquivos (por exemplo: alguns exemplos podem ser somente em C#, outros podem não ter um host Python ou alguns exemplos podem exigir que arquivos de dados auxiliar funcionem).

## <a name="anatomy-of-a-helpful-readme-file"></a>Anatomia de um arquivo LEIAme útil

No entanto, um arquivo especialmente importante é o `README.md` arquivo, pois é isso que os usuários precisam para começar com seu exemplo!

Cada um `README.md` deve começar com alguns metadados que ajudam a docs.Microsoft.com/samples a encontrar sua contribuição.

> [!div class="nextstepaction"]
> [Veja como o exemplo chsh-Game é renderizado](https://docs.microsoft.com/samples/microsoft/quantum/validating-quantum-mechanics/)

Esses metadados são fornecidos como um [cabeçalho YAML](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#yaml-header) que indica em quais idiomas sua amostra abrange (normalmente, isso será `qsharp` , `csharp` e `python` ) e quais produtos sua amostra cobre (normalmente, apenas `qdk` ).

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="1-11":::

> [!IMPORTANT]
> A `page_type: sample` chave no cabeçalho é necessária para que seu exemplo apareça em docs.Microsoft.com/Samples.
> Da mesma forma, as `product` `language` chaves e são críticas para ajudar os usuários a localizar e executar seu exemplo.

Depois disso, é útil dar uma breve introdução que diz o que o seu novo exemplo faz:

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="13-21":::

Os usuários do seu exemplo também apreciarão saber o que precisam para executá-lo (por exemplo: os usuários precisam apenas do próprio kit de desenvolvimento Quantum ou precisam de software adicional, como node.js?):

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="23-25":::

Com tudo em vigor, você pode dizer aos usuários como executar seu exemplo:

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="27-50":::

Por fim, é útil informar aos usuários o que cada arquivo do seu exemplo faz e onde eles podem ir para mais informações:

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="52-61":::

> [!WARNING]
> Certifique-se de usar URLs absolutas aqui, pois seu exemplo será exibido em uma URL diferente quando renderizado em docs.microsoft.com/samples!
