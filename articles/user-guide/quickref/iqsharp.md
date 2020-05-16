---
title: Comandos magic do IQ#
description: 'Página de referência rápida para comandos mágicos de IQ # com o Q # Jupyter notebooks'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
uid: microsoft.quantum.guide.quickref.iqsharp
ms.openlocfilehash: 0cd1a2289132e2760a21fd9d4f4083696353e271
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83431012"
---
# <a name="iq-magic-commands"></a>Comandos magic do IQ#

### <a name="general"></a>Geral

- `%config`: Define ou obtém as preferências de configuração.
- `%estimate`: Executa uma determinada função ou operação no computador de destino QuantumSimulator.
- `%lsmagic`: Retorna uma lista de todos os comandos mágicos disponíveis no momento.
- `%package`: Fornece a capacidade de carregar um pacote NuGet.
- `%performance`: Relata as métricas de desempenho atuais para este kernel.
- `%simulate`: Executa uma determinada função ou operação no computador de destino QuantumSimulator.
- `%toffoli`: Executa uma determinada função ou operação no computador de destino do simulador de ToffoliSimulator.
- `%who`: Fornece ações relacionadas ao espaço de trabalho atual.
- `%workspace`: Retorna uma lista de todas as operações e funções definidas na sessão atual, interativamente ou carregadas do espaço de trabalho atual.

### <a name="chemistry"></a>Química

- `%chemistry.broombridge`: Carrega e retorna a representação de problema de estrutura eletrônica Broombridge de um determinado arquivo. YAML.
- `%chemistry.encode`: Codifica um Fermion Hamiltonian para um formato consumível por Q #.
- `%chemistry.fh.add_terms`: Adiciona termos a um Fermion Hamiltonian.
- `%chemistry.fh.load`: Carrega o Fermion Hamiltonian para um problema de estrutura eletrônica. O problema é carregado de um arquivo ou passado como um argumento.
- `%chemistry.inputstate.load`: Carrega o problema de estrutura eletrônica do Broombridge e retorna o estado de entrada selecionado.

### <a name="from-microsoftquantumkatas-package"></a>Do pacote Microsoft. Quantum. katas

- `%kata`: Executa um único teste e relata se o teste foi aprovado com êxito.
- `%check_kata`: Verifica a implementação de referência para um único teste de Kata.
    Especificamente, ele substitui a implementação de referência de uma única tarefa na célula e relata se o teste foi aprovado com êxito.
