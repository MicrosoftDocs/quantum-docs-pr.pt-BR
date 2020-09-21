---
title: Criar um Gerador de Número Quântico Aleatório
description: Crie um Q# projeto que demonstre os conceitos fundamentais da Quantum, como a superposição, criando um gerador de número aleatório Quantum.
author: bromeg
ms.author: megbrow
ms.date: 10/25/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.qrng
no-loc:
- Q#
- $$v
ms.openlocfilehash: a0e8933e6a77d017db914e4bb969ea05f760a443
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834033"
---
# <a name="tutorial-implement-a-quantum-random-number-generator-in-q"></a>Tutorial: Implementar um gerador de número quântico aleatório em Q\#

Um exemplo simples de um algoritmo Quantum escrito em Q# é um gerador de número aleatório Quantum. Esse algoritmo usa a natureza da mecânica quântica para produzir um número aleatório.

## <a name="prerequisites"></a>Pré-requisitos

- O Microsoft [Quantum development kit](xref:microsoft.quantum.install).
- Crie um Q# projeto para um [ Q# aplicativo](xref:microsoft.quantum.install.standalone), com um [programa de host Python](xref:microsoft.quantum.install.python)ou um [programa de host C#](xref:microsoft.quantum.install.cs).

## <a name="write-a-no-locq-operation"></a>Gravar uma Q# operação

### <a name="no-locq-operation-code"></a>Q# código da operação

1. Substitua o conteúdo do arquivo Program.qs pelo seguinte código:

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-15,34":::

Conforme mencionado em nosso artigo [Noções básicas sobre computação quântica](xref:microsoft.quantum.overview.understanding), um qubit é uma unidade de informações quânticas que podem estar em superposição. Quando medido, um qubit pode ser apenas 0 ou 1. No entanto, quando uma operação está em execução, o estado do qubit representa a probabilidade de ler um 0 ou um 1 com uma medida. Esse estado probabilístico é conhecido como sobreposição. Podemos usar essa probabilidade para gerar números aleatórios.

Em nossa Q# operação, apresentamos o `Qubit` tipo de dados, nativo para Q# . Podemos alocar apenas um `Qubit` com uma instrução `using`. Quando é alocado, um qubit está sempre no estado `Zero`. 

Usando a operação `H`, podemos colocar nosso `Qubit` em sobreposição. Para medir um qubit e ler seu valor, use a operação intrínseca `M`.

Ao colocar nosso `Qubit` em sobreposição e medi-lo, nosso resultado será um valor diferente cada vez que o código for invocado.

Quando um `Qubit` for desalocado, ele precisará ser explicitamente definido de volta para o estado `Zero`; caso contrário, o simulador relatará um erro de runtime. Uma maneira fácil de alcançar isso é invocar `Reset`.

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

Agora que temos uma Q# operação que gera bits aleatórios, podemos usá-lo para criar um gerador de número aleatório de Quantum completo. Podemos usar um Q# aplicativo ou usar um programa host.



### <a name="no-locq-applications-with-visual-studio-or-visual-studio-code"></a>[Q# aplicativos com Visual Studio ou Visual Studio Code](#tab/tabid-qsharp)

Para criar o Q# aplicativo completo, adicione o seguinte ponto de entrada ao seu Q# programa: 

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="17-33":::

O programa executará a operação ou função marcada com o `@EntryPoint()` atributo em um simulador ou avaliador de recurso, dependendo da configuração do projeto e das opções de linha de comando.

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-34":::

No Visual Studio, basta pressionar CTRL + F5 para executar o script.

No VS Code, compile o Program.qs pela primeira vez digitando o seguinte no terminal:

```dotnetcli
dotnet build
```

Para as próximas execuções, não é necessário compilá-lo novamente. Para executá-lo, digite o seguinte comando e pressione Enter:

```dotnetcli
dotnet run --no-build
```

### <a name="python-with-visual-studio-code-or-the-command-prompt"></a>[Python com Visual Studio Code ou o prompt de comando](#tab/tabid-python)

Para executar o novo Q# programa do Python, salve o seguinte código como `host.py` :

:::code language="python" source="~/quantum/samples/interoperability/qrng/host.py" range="11-30":::

Em seguida, você pode executar o programa de host do Python no prompt de comando:

```bash
$ python host.py
Preparing Q# environment...
..The random number generated is 42
```

### <a name="c-with-visual-studio-code-or-visual-studio"></a>[C# com o Visual Studio Code ou com o Visual Studio](#tab/tabid-csharp)

Para executar o novo Q# programa a partir do C#, modifique `Driver.cs` para incluir o seguinte código C#:

:::code language="csharp" source="~/quantum/samples/interoperability/qrng/Host.cs" range="4-39":::

Em seguida, você pode executar o programa de host C# no prompt de comando (no Visual Studio, você deve pressionar F5):

```bash
$ dotnet run
The random number generated is 42
```

***
