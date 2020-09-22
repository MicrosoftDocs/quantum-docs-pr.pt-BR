---
title: Introdução à Biblioteca de Química Quântica
description: Saiba mais sobre a Biblioteca de Química do Microsoft Quantum e sobre como ela é usada para simular problemas na estrutura eletrônica de computadores quânticos.
author: QuantumWriter
ms.author: ageller
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.chemistry.concepts.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: 15439a34933bd561dc011acf48e669abeb031e33
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835784"
---
# <a name="introduction-to-the-quantum-chemistry-library"></a>Introdução à Biblioteca de Química Quântica

A simulação de sistemas físicos desempenha uma função central na computação quântica há bastante tempo.  Isso acontece porque acredita-se amplamente que a dinâmica quântica seja extremamente complicada para simular em computadores quânticas, o que significa que a complexidade de simular o sistema é dimensionada exponencialmente com o tamanho do sistema quântico em questão.  A simulação de problemas de química e da ciência de materiais continua sendo a aplicação mais estimulante da computação quântica e nos permitiria investigar mecanismos de reação química que estariam, de outra forma, além de nossa capacidade de medir ou simular.  Ela também nos permitiria simular materiais eletrônicos correlacionados, como supercondutores de alta temperatura. A lista de aplicações neste espaço é grande.

A finalidade desta documentação é fornecer uma introdução concisa à simulação de problemas de estrutura eletrônica em computadores quânticos para ajudar o leitor a entender a função de que muitos aspectos da biblioteca de simulação Hamiltoniana desempenham no espaço.  Começamos com uma breve introdução à mecânica quântica e, em seguida, analisamos como os sistemas eletrônicos são modelados com base nela.  Em seguida, discutiremos como essa dinâmica quântica pode ser emulada usando um computador quântico.  Depois disso, discutiremos dois métodos usados para compilar a dinâmica quântica em sequências de etapas: decomposições de Trotter-Suzuki e aplicação de qubits.
