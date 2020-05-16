---
title: 'Desenvolver com o Q # Jupyter notebooks'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: 38db14ccc5f2406043ff4baee3f562385cdf47a8
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426388"
---
# <a name="develop-with-q-jupyter-notebooks"></a>Desenvolver com o Q # Jupyter notebooks

Instale o QDK para desenvolver operações Q # em notebooks do Q # Jupyter.

Os notebooks Jupyter permitem a execução de código in-loco juntamente com instruções, observações e outros conteúdos. Esse ambiente é ideal para escrever código Q # com explicações incorporadas ou tutoriais interativos de computação Quantum. Aqui está o que você precisa fazer para começar a criar seus próprios notebooks de Q#.

IQ# (pronunciado i-q-sharp) é uma extensão usada principalmente pelo Jupyter e pelo Python para o SDK do .NET Core que fornece a funcionalidade principal para compilar e simular operações Q#.

> [!NOTE]
> * Em Jupyter notebooks do Q #, você só pode executar o código Q # e as operações não podem ser chamadas de programas de host externos (por exemplo, arquivos Python ou C#). Esse ambiente não será apropriado se o seu objetivo for combinar um programa host clássico externo com o programa Quantum.

1. Pré-requisitos

    - [Python](https://www.python.org/downloads/) 3,6 ou posterior
    - [Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/install.html)
    - [SDK do .NET Core 3,1 ou posterior](https://www.microsoft.com/net/download)

1. Instalar o pacote `iqsharp`

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. Verificar a instalação criando um aplicativo `Hello World`

    - Execute o seguinte comando para iniciar o servidor de notebook:

        ```bash
        jupyter notebook
        ```

    - Para abrir a cópia do bloco de anotações Jupyter e cole a URL fornecida pela linha de comando no navegador.

    - Crie um Jupyter Notebook com um kernel do Q# e adicione o seguinte código à primeira célula do notebook:

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - Execute esta célula do notebook:

        ![Célula do Jupyter Notebook com código Q#](~/media/install-guide-jupyter.png)

        Você deverá ver `SayHello` na saída da célula. Durante a execução em Jupyter notebooks, o código Q# é compilado e o notebook gera o nome das operações encontradas.


    - Em uma nova célula, execute a operação que você acabou de criar (em um simulador) usando o `%simulate` comando:

        ![Célula do Jupyter Notebook com a mágica %simulate](~/media/install-guide-jupyter-simulate.png)

        Você deve ver a mensagem impressa na tela junto com o resultado da operação que você chamou (aqui, vemos a tupla vazia `()` porque nossa operação simplesmente retorna um `Unit` tipo).

## <a name="next-steps"></a>Próximas etapas

Agora que você instalou o Quantum development kit em seu ambiente preferido, escreva e execute [seu primeiro programa quântico](xref:microsoft.quantum.quickstarts.qrng).
