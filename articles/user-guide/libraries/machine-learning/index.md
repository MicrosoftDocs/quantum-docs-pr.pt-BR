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
# <a name="introduction-to-the-quantum-machine-learning-library"></a><span data-ttu-id="3e4a8-103">Introdução à Biblioteca de Aprendizado de Máquina Quântico</span><span class="sxs-lookup"><span data-stu-id="3e4a8-103">Introduction to the Quantum Machine Learning Library</span></span>

<span data-ttu-id="3e4a8-104">A Biblioteca de Machine Learning do Quantum é uma API escrita em Q# que permite executar experimentos de machine learning quântico/clássico híbrido.</span><span class="sxs-lookup"><span data-stu-id="3e4a8-104">The Quantum Machine Learning Library is an API, written in Q#, that gives you the ability to run hybrid quantum/classical machine learning experiments.</span></span> <span data-ttu-id="3e4a8-105">A biblioteca possibilita:</span><span class="sxs-lookup"><span data-stu-id="3e4a8-105">The library gives you the ability to:</span></span>

- <span data-ttu-id="3e4a8-106">Carregar seus próprios dados para classificação com simuladores quânticos</span><span class="sxs-lookup"><span data-stu-id="3e4a8-106">Load your own data to classify with quantum simulators</span></span>

- <span data-ttu-id="3e4a8-107">Usar exemplos e tutoriais para ter uma introdução ao campo do aprendizado de máquina quântico</span><span class="sxs-lookup"><span data-stu-id="3e4a8-107">Use samples and tutorials to get introduced to the field of quantum machine learning</span></span>

<span data-ttu-id="3e4a8-108">Você pode esperar um baixo desempenho em comparação com as estruturas clássicas de aprendizado de máquina atuais (lembre-se de que tudo é executado além da simulação de um dispositivo quântico que já consome muitos recursos de computação).</span><span class="sxs-lookup"><span data-stu-id="3e4a8-108">You can expect low performance compared to current classical machine learning frameworks (remember that everything is running on top of the simulation of a quantum device that is already computationally expensive).</span></span>

<span data-ttu-id="3e4a8-109">A finalidade desta documentação é:</span><span class="sxs-lookup"><span data-stu-id="3e4a8-109">The purpose of this documentation is:</span></span>

- <span data-ttu-id="3e4a8-110">Fazer uma apresentação concisa das ferramentas de aprendizado de máquina (escritas em Q\#) para aprendizado quântico/clássico híbrido.</span><span class="sxs-lookup"><span data-stu-id="3e4a8-110">A concise introduction to machine learning tools (written in Q\#) for hybrid quantum/classical learning.</span></span>
- <span data-ttu-id="3e4a8-111">Apresentar conceitos de aprendizado de máquina e, especificamente, sua realização em classificadores centrados no circuito quântico (também conhecidos como classificadores sequenciais quânticos).</span><span class="sxs-lookup"><span data-stu-id="3e4a8-111">Introduce machine learning concepts and specifically their realization in quantum circuit centric classifiers (also known as quantum sequential classifiers).</span></span>
- <span data-ttu-id="3e4a8-112">Fornecer um conjunto de tutoriais com as noções básicas para começar a usar as ferramentas fornecidas pela biblioteca.</span><span class="sxs-lookup"><span data-stu-id="3e4a8-112">Provide a set of tutorials on the basics to start using the tools provided by the library.</span></span>
- <span data-ttu-id="3e4a8-113">Discutir os métodos de treinamento e validação desses classificadores e como eles são convertidos nas operações em Q\# específicas fornecidas pela biblioteca.</span><span class="sxs-lookup"><span data-stu-id="3e4a8-113">Discuss the training and validation methods for such classifiers and how they translate into specific Q\# operations provided by the library.</span></span>

<span data-ttu-id="3e4a8-114">O modelo implementado nesta biblioteca é baseado no esquema de treinamento quântico clássico apresentado em [Classificadores quânticos centrados no circuito](https://arxiv.org/abs/1804.00633)</span><span class="sxs-lookup"><span data-stu-id="3e4a8-114">The model implemented in this library is based on the quantum-classical training scheme presented in [Circuit-centric quantum classifiers](https://arxiv.org/abs/1804.00633)</span></span>
