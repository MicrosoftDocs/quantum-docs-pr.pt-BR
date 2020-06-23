---
title: Introdução ao Pacote de Aprendizado de Máquina Quântico | Microsoft Docs
description: Introdução ao Pacote de Aprendizado de Máquina Quântico
author: QuantumWriter
ms.author: alexeib@microsoft.com
ms.date: 12/5/2019
ms.topic: article
uid: microsoft.quantum.machine-learning.concepts.intro
ms.openlocfilehash: 7f22d5d3212890abc764f88693937b534466170f
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85273224"
---
# <a name="introduction-to-the-quantum-machine-learning-library"></a>Introdução à Biblioteca de Aprendizado de Máquina Quântico

A Biblioteca de Aprendizado de Máquina Quântico é uma API escrita em Q# que permite executar experimentos de aprendizado de máquina quântico/clássico híbrido. A biblioteca possibilita:

- Carregar seus próprios dados para classificação com simuladores quânticos

- Usar exemplos e tutoriais para ter uma introdução ao campo do aprendizado de máquina quântico

Você pode esperar um baixo desempenho em comparação com as estruturas clássicas de aprendizado de máquina atuais (lembre-se de que tudo é executado além da simulação de um dispositivo quântico que já consome muitos recursos de computação).

A finalidade desta documentação é:

- Fazer uma apresentação concisa das ferramentas de aprendizado de máquina (escritas em Q\#) para aprendizado quântico/clássico híbrido.
- Apresentar conceitos de aprendizado de máquina e, especificamente, sua realização em classificadores centrados no circuito quântico (também conhecidos como classificadores sequenciais quânticos).
- Fornecer um conjunto de tutoriais com as noções básicas para começar a usar as ferramentas fornecidas pela biblioteca.
- Discutir os métodos de treinamento e validação desses classificadores e como eles são convertidos nas operações em Q\# específicas fornecidas pela biblioteca.

O modelo implementado nesta biblioteca é baseado no esquema de treinamento quântico clássico apresentado em [Classificadores quânticos centrados no circuito](https://arxiv.org/abs/1804.00633)
