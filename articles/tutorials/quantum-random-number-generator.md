---
title: Criar um Gerador de Número Quântico Aleatório
description: Crie um projeto em Q# que demonstra conceitos quânticos fundamentais, como sobreposição, criando um gerador de número quântico aleatório.
author: bromeg
ms.author: megbrow@microsoft.com
ms.date: 10/25/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.qrng
ms.openlocfilehash: 18e8975e513a87c0a67a6dbb5586cc7dab5a93fb
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274223"
---
# <a name="tutorial-implement-a-quantum-random-number-generator-in-q"></a>Tutorial: Implementar um gerador de número quântico aleatório em Q\#

Um exemplo simples de um algoritmo quântico escrito em Q# é um gerador de número quântico aleatório. Esse algoritmo usa a natureza da mecânica quântica para produzir um número aleatório.

## <a name="prerequisites"></a>Pré-requisitos

- O Microsoft [Quantum development kit](xref:microsoft.quantum.install).
- A criação de um projeto Q# para [usar o Q# na linha de comando](xref:microsoft.quantum.install.standalone) ou com um [programa host Python](xref:microsoft.quantum.install.python) ou com um [programa host C#](xref:microsoft.quantum.install.cs).

## <a name="write-a-q-operation"></a>Escrever uma operação Q#

### <a name="q-operation-code"></a>Código de operação Q#

1. Substitua o conteúdo do arquivo Program.qs pelo seguinte código:

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-15,34":::

Conforme mencionado em nosso artigo [Noções básicas sobre computação quântica](xref:microsoft.quantum.overview.understanding), um qubit é uma unidade de informações quânticas que podem estar em superposição. Quando medido, um qubit pode ser apenas 0 ou 1. No entanto, durante a execução, o estado do qubit representa a probabilidade de ler 0 ou 1 com uma medida. Esse estado probabilístico é conhecido como sobreposição. Podemos usar essa probabilidade para gerar números aleatórios.

Em nossa operação de Q#, apresentamos o tipo de dados `Qubit`, nativo para Q#. Podemos alocar apenas um `Qubit` com uma instrução `using`. Quando é alocado, um qubit está sempre no estado `Zero`. 

Usando a operação `H`, podemos colocar nosso `Qubit` em sobreposição. Para medir um qubit e ler seu valor, use a operação intrínseca `M`.

Ao colocar nosso `Qubit` em sobreposição e medi-lo, nosso resultado será um valor diferente cada vez que o código for invocado.

Quando um `Qubit` é desalocado, ele deve ser explicitamente definido de volta para o `Zero` estado; caso contrário, o simulador relatará um erro de tempo de execução. Uma maneira fácil de alcançar isso é invocar `Reset`.

### <a name="visualizing-the-code-with-the-bloch-sphere"></a>Visualizar o código com a esfera Bloch

Na esfera Bloch, o polo norte representa o valor clássico **0** e o polo sul representa o valor clássico **1**. Qualquer sobreposição pode ser representada por um ponto na esfera (representada por uma seta). Quanto mais próxima a extremidade da seta estiver de um polo, maior a probabilidade de o qubit recolher o valor clássico atribuído a esse polo quando medido. Por exemplo, o estado do qubit representado pela seta vermelha abaixo terá uma probabilidade mais alta de dar o valor **0** se medirmos isso.

<img src="~/media/qrng-Bloch.png" width="175" alt="A qubit state with a high probability of measuring zero">

Podemos usar essa representação para visualizar o que o código está fazendo:

* Primeiro, começamos com um qubit inicializado no estado **0** e aplicamos `H` para criar uma sobreposição na qual as probabilidades de **0** e **1** são as mesmas.

<img src="~/media/qrng-H.png" width="450" alt="Preparing a qubit in superposition">

* Em seguida, medimos o qubit e salvamos a saída:

<img src="~/media/qrng-meas.png" width="450" alt="Measuring a qubit and saving the output">

Como o resultado da medição é completamente aleatório, obtivemos um bit aleatório. Podemos chamar essa operação várias vezes para criar inteiros. Por exemplo, se chamarmos a operação três vezes para obter três bits aleatórios, poderemos criar números aleatórios de 3 bits (ou seja, um número aleatório entre 0 e 7).


## <a name="creating-a-complete-random-number-generator"></a>Criar um gerador de número aleatório completo

Agora que temos uma operação Q# que gera bits aleatórios, podemos usá-la para criar um gerador de número quântico aleatório completo. Podemos usar os aplicativos de linha de comando Q# ou um programa host.



### <a name="q-command-line-applications-with-visual-studio-or-visual-studio-code"></a>[Aplicativos de linha de comando Q# com o Visual Studio ou com o Visual Studio Code](#tab/tabid-qsharp)

Para criar um aplicativo de linha de comando Q# completo, adicione o seguinte ponto de entrada ao programa Q#: 

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="17-33":::

O executável executará a operação ou a função marcada com o atributo `@EntryPoint()` em um simulador ou em um avaliador de recurso, dependendo da configuração do projeto e das opções de linha de comando.

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-34":::

No Visual Studio, basta pressionar Ctrl + F5 para executar o script.

No VS Code, compile o Program.qs pela primeira vez digitando o seguinte no terminal:

```dotnetcli
dotnet build
```

Para as próximas execuções, não é necessário compilá-lo novamente. Para executá-lo, digite o seguinte comando e pressione Enter:

```dotnetcli
dotnet run --no-build
```

### <a name="python-with-visual-studio-code-or-the-command-line"></a>[Python com Visual Studio Code ou a linha de comando](#tab/tabid-python)

Para executar o novo programa Q# no Python, salve o seguinte código como `host.py`:

:::code language="python" source="~/quantum/samples/interoperability/qrng/host.py" range="11-30":::

Em seguida, execute o programa host do Python na linha de comando:

```bash
$ python host.py
Preparing Q# environment...
..The random number generated is 42
```

### <a name="c-with-visual-studio-code-or-visual-studio"></a>[C# com o Visual Studio Code ou com o Visual Studio](#tab/tabid-csharp)

Para executar o novo programa Q# no C#, modifique `Driver.cs` para incluir o seguinte código C#:

:::code language="csharp" source="~/quantum/samples/interoperability/qrng/Host.cs" range="4-39":::

Em seguida, você pode executar o programa host C# na linha de comando (no Visual Studio, você deve pressionar F5):

```bash
$ dotnet run
The random number generated is 42
```

***
