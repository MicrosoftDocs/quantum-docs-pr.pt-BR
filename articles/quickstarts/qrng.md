---
title: Criar um Gerador de Número Quântico Aleatório
description: Crie um projeto em Q# que demonstra conceitos quânticos fundamentais, como sobreposição, criando um gerador de número quântico aleatório.
author: bromeg
ms.author: megbrow@microsoft.com
ms.date: 10/25/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.qrng
ms.openlocfilehash: d1ad2c1153814e2fa19a38307b2c668c77eae4e3
ms.sourcegitcommit: b7e205aaa7fa1ca9f0daa163e46154945f4bc965
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/18/2020
ms.locfileid: "77441066"
---
# <a name="quickstart-implement-a-quantum-random-number-generator-in-q"></a>Início Rápido: Implementar um Gerador de Número Quântico Aleatório em Q#
Um exemplo simples de um algoritmo quântico escrito em Q# é um gerador de número quântico aleatório. Esse algoritmo usa a natureza da mecânica quântica para produzir um número aleatório. 

## <a name="prerequisites"></a>Pré-requisitos

- O Microsoft [Quantum development kit](xref:microsoft.quantum.install).
- [Criar um projeto Q#](xref:microsoft.quantum.howto.createproject)


## <a name="write-a-q-operation"></a>Escrever uma operação Q#

### <a name="q-operation-code"></a>Código de operação Q#

1. Substitua o conteúdo do arquivo Operations.qs pelo seguinte código:

 :::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-14":::

Conforme mencionado em nosso artigo [O que é Computação Quântica?](xref:microsoft.quantum.overview.what), um qubit é uma unidade de informações quânticas que podem estar em sobreposição. Quando medido, um qubit pode ser apenas 0 ou 1. No entanto, durante a execução, o estado do qubit representa a probabilidade de ler 0 ou 1 com uma medida. Esse estado probabilístico é conhecido como sobreposição. Podemos usar essa probabilidade para gerar números aleatórios.

Em nossa operação de Q#, apresentamos o tipo de dados `Qubit`, nativo para Q#. Podemos alocar apenas um `Qubit` com uma instrução `using`. Quando é alocado, um qubit está sempre no estado `Zero`. 

Usando a operação `H`, podemos colocar nosso `Qubit` em sobreposição. Para medir um qubit e ler seu valor, use a operação intrínseca `M`.

Ao colocar nosso `Qubit` em sobreposição e medi-lo, nosso resultado será um valor diferente cada vez que o código for invocado. 

Quando um `Qubit` for desalocado, ele deverá ser explicitamente definido de volta para o estado `Zero`; caso contrário, o simulador relatará um erro de tempo de execução. Uma maneira fácil de alcançar isso é invocar `Reset`.

### <a name="visualizing-the-code-with-the-bloch-sphere"></a>Visualizar o código com a esfera Bloch

Na esfera Bloch, o polo norte representa o valor clássico **0** e o polo sul representa o valor clássico **1**. Qualquer sobreposição pode ser representada por um ponto na esfera (representada por uma seta). Quanto mais próxima a extremidade da seta estiver de um polo, maior a probabilidade de o qubit recolher o valor clássico atribuído a esse polo quando medido. Por exemplo, o estado do qubit representado pela seta vermelha abaixo terá uma probabilidade mais alta de dar o valor **0** se medirmos isso.

<img src="~/media/qrng-Bloch.png" width="175">

Podemos usar essa representação para visualizar o que o código está fazendo:

* Primeiro, começamos com um qubit inicializado no estado **0** e aplicamos `H` para criar uma sobreposição na qual as probabilidades de **0** e **1** são as mesmas.

<img src="~/media/qrng-H.png" width="450">

* Em seguida, medimos o qubit e salvamos a saída:

<img src="~/media/qrng-meas.png" width="450">

Como o resultado da medição é completamente aleatório, obtivemos um bit aleatório. Podemos chamar essa operação várias vezes para criar inteiros. Por exemplo, se chamarmos a operação três vezes para obter três bits aleatórios, poderemos criar números aleatórios de 3 bits (ou seja, um número aleatório entre 0 e 7).

## <a name="creating-a-complete-random-number-generator-using-a-host-program"></a>Criar um gerador de número aleatório completo usando um programa de host

Agora que temos uma operação em Q# que gera bits aleatórios, podemos usá-la para criar um gerador de número quântico aleatório completo com um programa de host.

 ### <a name="python-with-visual-studio-code-or-the-command-line"></a>[Python com Visual Studio Code ou a linha de comando](#tab/tabid-python)
 
 Para executar o novo programa Q# no Python, salve o seguinte código como `host.py`:
 
:::code language="python" source="~/quantum/samples/getting-started/qrng/host.py" range="11-30":::

 Em seguida, execute o programa host do Python na linha de comando:
 ```bash
 $ python host.py
 Preparing Q# environment...
 ..The random number generated is 42
 ```
 ### <a name="c-with-visual-studio-code-or-the-command-line"></a>[C# com Visual Studio Code ou a linha de comando](#tab/tabid-csharp)
 
 Para executar o novo programa Q# no C#, modifique `Driver.cs` para incluir o seguinte código C#:
 
 :::code language="csharp" source="~/quantum/samples/getting-started/qrng/Host.cs" range="4-39":::
 
 Em seguida, execute o programa host do C# na linha de comando:
 
 ```bash
 $ dotnet run
 The random number generated is 42
 ```

 ### <a name="c-with-visual-studio-2019"></a>[C# com Visual Studio 2019](#tab/tabid-vs2019)

 Para executar seu novo programa em Q# no C# no Visual Studio, modifique `Driver.cs` para incluir o seguinte código C#:

 :::code language="csharp" source="~/quantum/samples/getting-started/qrng/Host.cs" range="4-39":::

 Em seguida, pressione F5. O programa iniciará a execução e uma nova janela será exibida com o número aleatório gerado: 

 ```bash
 $ dotnet run
 The random number generated is 42
 ```
 ***
