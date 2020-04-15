---
title: Aplicativos de exemplo de química do Quantum
description: Explore aplicativos de exemplo da biblioteca de química do Microsoft Quantum.
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples
ms.openlocfilehash: 5168fc8592d34a32ba67e5a0c4793aa17599fd35
ms.sourcegitcommit: 9d1c045cf1a2c3e19030cb38dbc7496dbd24ab58
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2020
ms.locfileid: "77906484"
---
# <a name="quantum-chemistry-examples"></a>Exemplos de química quântica

Nos conceitos de química quântica, criamos manualmente o exemplo de Hamiltonianos fermiônicos. Agora, combinamos os algoritmos de simulação química descritos em [Simulando a Dinâmica Hamiltoniana](xref:microsoft.quantum.libraries.standard.algorithms) com a [estimativa de fase quântica](xref:microsoft.quantum.libraries.characterization) na biblioteca de cânones. Essa combinação nos permite obter estimativas dos níveis de energia na molécula representada, que é uma das principais aplicações da química quântica em um computador quântico. 

Em vez de especificar os termos do Hamiltoniano um por um, também trabalhamos com alguns exemplos que nos permitem executar experimentos de química quântica em escala. Começamos com exemplos que carregam um Hamiltoniano químico codificado no [esquema de Broombridge](xref:microsoft.quantum.libraries.chemistry.schema.broombridge).

Para moléculas grandes demais para serem simuladas no [simulador de estado completo](xref:microsoft.quantum.machines.full-state-simulator), experimentos científicos interessantes ainda podem ser realizados. Por exemplo, os custos com recursos para executar simulações químicas grandes ainda podem ser avaliados usando o [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro).

Agora, vamos ilustrar as aplicações interessantes da biblioteca de simulação química por meio de alguns dos exemplos fornecidos.
