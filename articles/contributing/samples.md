---
title: Colaborando com exemplos no Microsoft QDK
description: Saiba como contribuir com código de exemplo para a Microsoft Quantum Development Kit (QDK).
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.samples
ms.openlocfilehash: 3bd0de04a448c74eea6c3e8e3a15dcbb19f9d705
ms.sourcegitcommit: d61b388651351e5abd4bfe7a672e88b84a6697f8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2020
ms.locfileid: "79024144"
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

Ou seja, os exemplos no [repositório Microsoft/Quantum](https://github.com/microsoft/Quantum) são divididos por área de assunto em pastas diferentes, como `algorithms/`, `arithmetic/`ou `characterization/`.
Dentro da pasta de cada área de assunto, cada amostra consiste em uma única pasta que coleta tudo o que um usuário precisará para explorar e usar esse exemplo.

## <a name="how-samples-are-structured"></a>Como os exemplos são estruturados

Examinando os arquivos que compõem cada pasta, vamos nos aprofundar no exemplo de [`algorithms/chsh-game/`](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/chsh-game) .

| Arquivo              | DESCRIÇÃO                                                |
|-------------------|------------------------------------------------------------|
| `CHSHGame.csproj` | Projeto Q # usado para criar o exemplo com o SDK do .NET Core |
| `Game.qs`         | Q # operações e funções para o exemplo                 |
| `Host.cs`         | C#programa de host usado para executar o exemplo                     |
| `host.py`         | Programa de host Python usado para executar o exemplo                 |
| `README.md`       | Documentação sobre o que o exemplo faz e como usá-lo    |

Nem todos os exemplos terão exatamente o mesmo conjunto de arquivos (por exemplo: alguns exemplos podem ser C#apenas, outros podem não ter um host Python ou alguns exemplos podem exigir que arquivos de dados auxiliar funcionem).

## <a name="anatomy-of-a-helpful-readme-file"></a>Anatomia de um arquivo LEIAme útil

No entanto, um arquivo especialmente importante é o arquivo de `README.md`, pois é isso que os usuários precisam para começar com seu exemplo!

Cada `README.md` deve começar com alguns metadados que ajudam a docs.microsoft.com/samples a encontrar sua contribuição.

> [!div class="nextstepaction"]
> [Veja como o exemplo chsh-Game é renderizado](https://docs.microsoft.com/samples/microsoft/quantum/validating-quantum-mechanics/)

Esses metadados são fornecidos como um [cabeçalho YAML](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#yaml-header) que indica em quais idiomas seu exemplo abrange (normalmente, isso será `qsharp`, `csharp`e `python`) e quais produtos sua amostra abrange (normalmente, apenas `qdk`).

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="1-11":::

> [!IMPORTANT]
> A chave de `page_type: sample` no cabeçalho é necessária para que seu exemplo apareça em docs.microsoft.com/samples.
> Da mesma forma, as chaves `product` e `language` são críticas para ajudar os usuários a localizar e executar seu exemplo.

Depois disso, é útil dar uma breve introdução que diz o que o seu novo exemplo faz:

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="13-21":::

Os usuários do seu exemplo também apreciarão saber o que precisam para executá-lo (por exemplo: os usuários precisam apenas do próprio kit de desenvolvimento Quantum ou precisam de software adicional, como node. js?):

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="23-25":::

Com tudo em vigor, você pode dizer aos usuários como executar seu exemplo:

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="27-50":::

Por fim, é útil informar aos usuários o que cada arquivo do seu exemplo faz e onde eles podem ir para mais informações:

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="52-61":::

> [!WARNING]
> Certifique-se de usar URLs absolutas aqui, pois seu exemplo será exibido em uma URL diferente quando renderizado em docs.microsoft.com/samples!
