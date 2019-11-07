---
title: Criar um Gerador de Número Quântico Aleatório
description: Crie um projeto em Q# que demonstra conceitos quânticos fundamentais, como sobreposição, criando um gerador de número quântico aleatório.
author: bromeg
ms.author: megbrow@microsoft.com
ms.date: 10/25/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.qrng
ms.openlocfilehash: c3039b92c4b3235a397d5cf31280ac2673706e9d
ms.sourcegitcommit: 2ca4755d1a63431e3cb2d2918a10ad477ec2e368
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2019
ms.locfileid: "73462842"
---
# <a name="quickstart-implement-a-quantum-random-number-generator-in-q"></a>Início Rápido: Implementar um Gerador de Número Quântico Aleatório em Q#
Um exemplo simples de um algoritmo quântico escrito em Q# é um gerador de número quântico aleatório. Esse algoritmo usa a natureza da mecânica quântica para produzir um número aleatório. 

## <a name="prerequisites"></a>Pré-requisitos

- O Microsoft [Quantum development kit](xref:microsoft.quantum.install).
- [Criar um projeto Q#](xref:microsoft.quantum.howto.createproject)


## <a name="write-a-q-operation"></a>Escrever uma operação Q#

### <a name="q-operation-code"></a>Código de operação Q#

1. Substitua o conteúdo do arquivo Operations.qs pelo seguinte código:

    ```qsharp
    namespace Quantum {
        open Microsoft.Quantum.Intrinsic;

        operation QuantumRandomNumberGenerator() : Result {
            using(q = Qubit())  { // Allocate a qubit.
                H(q);             // Put the qubit to superposition. It now has a 50% chance of being 0 or 1.
                let r = M(q);     // Measure the qubit value.
                Reset(q);
                return r;
            }
        }
    }
    ```

Conforme mencionado em nosso artigo [O que é Computação Quântica?](xref:microsoft.quantum.overview.what), um qubit é uma unidade de informações quânticas que podem estar em sobreposição. Quando medido, um qubit pode ser apenas 0 ou 1. No entanto, durante a execução, o estado do qubit representa a probabilidade de ler 0 ou 1 com uma medida. Esse estado probabilístico é conhecido como sobreposição. Podemos usar essa probabilidade para gerar números aleatórios.

Em nossa operação de Q#, apresentamos o tipo de dados `Qubit`, nativo para Q#. Podemos alocar apenas um `Qubit` com uma instrução `using`. Quando é alocado, um qubit está sempre no estado `Zero`. 

Usando a operação `H`, podemos colocar nosso `Qubit` em sobreposição. Para medir um qubit e ler seu valor, use a operação intrínseca `M`.

Ao colocar nosso `Qubit` em sobreposição e medi-lo, nosso resultado será um valor diferente cada vez que o código for invocado. 

Quando um `Qubit` for desalocado, ele deverá ser explicitamente definido de volta para o estado `Zero`; caso contrário, o simulador relatará um erro de tempo de execução. Uma maneira fácil de alcançar isso é invocar `Reset`.

### <a name="visualizing-the-code-with-the-bloch-sphere"></a>Visualizar o código com a esfera Bloch

Na esfera Bloch, o polo norte representa o valor clássico **0** e o polo sul representa o valor clássico **1**. Qualquer sobreposição pode ser representada por um ponto na esfera (representada por uma seta). Quanto mais próxima a extremidade da seta estiver de um polo, maior a probabilidade de o qubit recolher o valor clássico atribuído a esse polo quando medido. Por exemplo, o estado do qubit representado pela seta vermelha abaixo terá uma probabilidade mais alta de dar o valor **0** se medirmos isso.

<img src="./Bloch.svg" width="175">

Podemos usar essa representação para visualizar o que o código está fazendo:

* Primeiro, começamos com um qubit inicializado no estado **0** e aplicamos `H` para criar uma sobreposição na qual as probabilidades de **0** e **1** são as mesmas.

<img src="./H.svg" width="450">

* Em seguida, medimos o qubit e salvamos a saída:

<img src="./Measurement2.svg" width="450">

Como o resultado da medição é completamente aleatório, obtivemos um bit aleatório. Podemos chamar essa operação várias vezes para criar inteiros. Por exemplo, se chamarmos a operação três vezes para obter três bits aleatórios, poderemos criar números aleatórios de 3 bits (ou seja, um número aleatório entre 0 e 7).
