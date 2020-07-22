---
title: Comandos magic do IQ#
description: 'Página de referência rápida para comandos mágicos de IQ # com o Q # Jupyter notebooks'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
uid: microsoft.quantum.guide.quickref.iqsharp
ms.openlocfilehash: 2fb542df8723fa437c82b4a1dfada77e22c1d6e4
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/21/2020
ms.locfileid: "86870525"
---
# <a name="iq-magic-commands"></a>Comandos magic do IQ#

### <a name="general"></a>Geral

- [`%config`](xref:microsoft.quantum.iqsharp.magic-ref.config): Permite a configuração ou consulta de opções de configuração.
- [`%estimate`](xref:microsoft.quantum.iqsharp.magic-ref.estimate): Executa uma determinada função ou operação no computador de destino ResourcesEstimator.
- [`%lsmagic`](xref:microsoft.quantum.iqsharp.magic-ref.lsmagic): Retorna uma lista de todos os comandos mágicos disponíveis no momento.
- [`%package`](xref:microsoft.quantum.iqsharp.magic-ref.package): Fornece a capacidade de carregar um pacote NuGet.
- [`%performance`](xref:microsoft.quantum.iqsharp.magic-ref.performance): Relata as métricas de desempenho atuais para este kernel.
- [`%simulate`](xref:microsoft.quantum.iqsharp.magic-ref.simulate): Executa uma determinada função ou operação no computador de destino QuantumSimulator.
- [`%toffoli`](xref:microsoft.quantum.iqsharp.magic-ref.toffoli): Executa uma determinada função ou operação no computador de destino ToffoliSimulator.
- [`%who`](xref:microsoft.quantum.iqsharp.magic-ref.who): Lista as operações de Q # disponíveis na sessão atual.
- [`%workspace`](xref:microsoft.quantum.iqsharp.magic-ref.workspace): Fornece ações relacionadas ao espaço de trabalho atual.

### <a name="azure-quantum-integration"></a>Integração do azure Quantum

- [`%azure.connect`](xref:microsoft.quantum.iqsharp.magic-ref.azure.connect): Conecta-se a um espaço de trabalho do azure Quantum ou exibe o status da conexão atual.
- [`%azure.execute`](xref:microsoft.quantum.iqsharp.magic-ref.azure.execute): Executa um trabalho em um espaço de trabalho do azure Quantum.
- [`%azure.jobs`](xref:microsoft.quantum.iqsharp.magic-ref.azure.jobs): Exibe uma lista de trabalhos no espaço de trabalho atual do azure Quantum.
- [`%azure.output`](xref:microsoft.quantum.iqsharp.magic-ref.azure.output): Exibe os resultados de um trabalho no espaço de trabalho atual do azure Quantum.
- [`%azure.status`](xref:microsoft.quantum.iqsharp.magic-ref.azure.status): Exibe o status de um trabalho no espaço de trabalho atual do azure Quantum.
- [`%azure.submit`](xref:microsoft.quantum.iqsharp.magic-ref.azure.submit): Envia um trabalho para um espaço de trabalho do azure Quantum.
- [`%azure.target`](xref:microsoft.quantum.iqsharp.magic-ref.azure.target): Define ou exibe o destino de execução ativa para envio de trabalho de Q # em um espaço de trabalho do azure Quantum.

### <a name="chemistry-from-microsoftquantumchemistry-package"></a>Química (do pacote Microsoft. Quantum. química)

- [`%chemistry.broombridge`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.broombridge): Carrega e retorna a representação de problema de estrutura eletrônica Broombridge de um determinado arquivo. YAML.
- [`%chemistry.encode`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.encode): Codifica um Fermion Hamiltonian para um formato consumível por Q #.
- [`%chemistry.fh.add_terms`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.fh.add_terms): Adiciona termos a um Fermion Hamiltonian.
- [`%chemistry.fh.load`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.fh.load): Carrega o Fermion Hamiltonian para um problema de estrutura eletrônica. O problema é carregado de um arquivo ou passado como um argumento.
- [`%chemistry.inputstate.load`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.inputstate.load): Carrega o problema de estrutura eletrônica do Broombridge e retorna o estado de entrada selecionado.

### <a name="katas-from-microsoftquantumkatas-package"></a>Katas (do pacote Microsoft. Quantum. katas)

- [`%kata`](xref:microsoft.quantum.iqsharp.magic-ref.kata): Executa um único teste e relata se o teste foi aprovado com êxito.
- [`%check_kata`](xref:microsoft.quantum.iqsharp.magic-ref.check_kata): Verifica a implementação de referência para um único teste de Kata.
    Especificamente, ele substitui a implementação de referência de uma única tarefa na célula e relata se o teste foi aprovado com êxito.
