---
title: Desenvolvimento com Jupyter Notebooks do Q#
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: 9117794d6cf6f05fa34e05c21fad8977d0e76505
ms.sourcegitcommit: c8ebc5d7d8581444754f5d7bfaca2f25601f1b14
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2020
ms.locfileid: "84577813"
---
# <a name="develop-with-q-jupyter-notebooks"></a>Desenvolvimento com Jupyter Notebooks do Q#

Instale o QDK para desenvolver operações Q # em notebooks do Q # Jupyter.

Os notebooks Jupyter permitem a execução de código in-loco juntamente com instruções, observações e outros conteúdos. Esse ambiente é ideal para escrever código Q # com explicações incorporadas ou tutoriais interativos de computação Quantum. Aqui está o que você precisa fazer para começar a criar seus próprios notebooks de Q#.

IQ# (pronunciado i-q-sharp) é uma extensão usada principalmente pelo Jupyter e pelo Python para o SDK do .NET Core que fornece a funcionalidade principal para compilar e simular operações Q#.

> [!NOTE]
> * Em Jupyter notebooks do Q #, você só pode executar o código Q # e as operações não podem ser chamadas de programas de host externos (por exemplo, arquivos Python ou C#). Esse ambiente não será apropriado se o seu objetivo for combinar um programa host clássico externo com o programa Quantum.

1. Pré-requisitos

    - [Python](https://www.python.org/downloads/) 3,6 ou posterior
    - [Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/install.html)
    - [SDK do .NET Core 3,1](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. Instalar o pacote `iqsharp`

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. Verificar a instalação criando um aplicativo `Hello World`

    - Execute o seguinte comando para iniciar o servidor de notebook:

        ```
        jupyter notebook
        ```

    - Para abrir o Jupyter Notebook, copie e cole a URL fornecida pela linha de comando em seu navegador.

    - Crie um Jupyter Notebook com um kernel Q # e adicione o seguinte código à primeira célula do bloco de anotações:

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - Execute esta célula do notebook:

        ![Jupyter Notebook célula com código Q #](~/media/install-guide-jupyter.png)

        Você deverá ver `SayHello` na saída da célula. Quando executado no Jupyter Notebook, o código Q # é compilado e o notebook gera o nome da (s) operação (ões) que encontrar.


    - Em uma nova célula, execute a operação que você acabou de criar (em um simulador) usando o `%simulate` comando:

        ![Jupyter Notebook célula com% simula mágica](~/media/install-guide-jupyter-simulate.png)

        Você deve ver a mensagem impressa na tela junto com o resultado da operação que você chamou (aqui, vemos a tupla vazia `()` porque nossa operação simplesmente retorna um `Unit` tipo).

## <a name="next-steps"></a>Próximas etapas

Agora que você instalou o QDK para os notebooks do Q # Jupyter, você pode escrever e executar [seu primeiro programa Quantum](xref:microsoft.quantum.quickstarts.qrng) escrevendo o código de q # diretamente no ambiente de Jupyter notebook.

Para obter mais exemplos do que você pode fazer com o Q # Jupyter notebooks, consulte:
- [Introdução à Q # e Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/). Lá, você encontrará um Jupyter Notebook Q # que mostra como usar o Q # nesse ambiente.
- [Quantum katas](xref:microsoft.quantum.overview.katas), uma coleção de código aberto de tutoriais individualizados e conjuntos de exercícios de programação na forma de Jupyter notebooks de Q #. Os [notebooks do tutorial Katas do Quantum](https://github.com/microsoft/QuantumKatas#tutorial-topics) são um bom ponto de partida. O Quantum katas tem como objetivo ensinar os elementos de computação Quantum e a programação Q # ao mesmo tempo. Eles são um excelente exemplo do tipo de conteúdo que você pode criar com os notebooks Q # Jupyter.
