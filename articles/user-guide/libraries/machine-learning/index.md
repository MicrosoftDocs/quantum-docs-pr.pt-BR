---
title: Introdução ao Pacote de Aprendizado de Máquina Quântico | Microsoft Docs
description: Introdução ao Pacote de Aprendizado de Máquina Quântico
author: QuantumWriter
ms.author: alexeib
ms.date: 12/5/2019
ms.topic: conceptual
uid: microsoft.quantum.machine-learning.concepts.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: 1e36948a216a06d76b99cd451bbfac6f5defd7c8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858788"
---
# <a name="introduction-to-the-quantum-machine-learning-library"></a>Introdução à Biblioteca de Aprendizado de Máquina Quântico

A Biblioteca de Machine Learning do Quantum é uma API escrita em Q# que permite executar experimentos de machine learning quântico/clássico híbrido. A biblioteca possibilita:

- Carregar seus próprios dados para classificação com simuladores quânticos

- Usar exemplos e tutoriais para ter uma introdução ao campo do aprendizado de máquina quântico

Você pode esperar um baixo desempenho em comparação com as estruturas clássicas de aprendizado de máquina atuais (lembre-se de que tudo é executado além da simulação de um dispositivo quântico que já consome muitos recursos de computação).

A finalidade desta documentação é:

- Fazer uma apresentação concisa das ferramentas de aprendizado de máquina (escritas em Q\#) para aprendizado quântico/clássico híbrido.
- Apresentar conceitos de aprendizado de máquina e, especificamente, sua realização em classificadores centrados no circuito quântico (também conhecidos como classificadores sequenciais quânticos).
- Fornecer um conjunto de tutoriais com as noções básicas para começar a usar as ferramentas fornecidas pela biblioteca.
- Discutir os métodos de treinamento e validação desses classificadores e como eles são convertidos nas operações em Q\# específicas fornecidas pela biblioteca.

O modelo implementado nesta biblioteca é baseado no esquema de treinamento quântico clássico apresentado em [Classificadores quânticos centrados no circuito](https://arxiv.org/abs/1804.00633)
