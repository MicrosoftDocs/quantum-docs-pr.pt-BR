---
title: Q#Comandos mágicos
description: Página de referência rápida para Q# comandos mágicos com Q# notebooks Jupyter
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: reference
uid: microsoft.quantum.guide.quickref.iqsharp
no-loc:
- Q#
- $$v
ms.openlocfilehash: bb6517b782a82c1cb159951af41df9bfde51c0bb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858526"
---
# <a name="ino-locq-magic-commands"></a>Q#Comandos mágicos

### <a name="general"></a>Geral

- [`%config`](xref:microsoft.quantum.iqsharp.magic-ref.config): Permite a configuração ou consulta de opções de configuração.
- [`%estimate`](xref:microsoft.quantum.iqsharp.magic-ref.estimate): Executa uma determinada função ou operação no computador de destino ResourcesEstimator.
- [`%lsmagic`](xref:microsoft.quantum.iqsharp.magic-ref.lsmagic): Retorna uma lista de todos os comandos mágicos disponíveis no momento.
- [`%lsopen`](xref:microsoft.quantum.iqsharp.magic-ref.lsopen): Lista namespaces abertos no momento e seus aliases.
- [`%package`](xref:microsoft.quantum.iqsharp.magic-ref.package): Fornece a capacidade de carregar um pacote NuGet.
- [`%performance`](xref:microsoft.quantum.iqsharp.magic-ref.performance): Relata as métricas de desempenho atuais para este kernel.
- [`%project`](xref:microsoft.quantum.iqsharp.magic-ref.project): Fornece a capacidade de exibir ou adicionar Q# referências de projeto. 
- [`%simulate`](xref:microsoft.quantum.iqsharp.magic-ref.simulate): Executa uma determinada função ou operação no computador de destino QuantumSimulator.
- [`%toffoli`](xref:microsoft.quantum.iqsharp.magic-ref.toffoli): Executa uma determinada função ou operação no computador de destino ToffoliSimulator.
- [`%who`](xref:microsoft.quantum.iqsharp.magic-ref.who): Lista as Q# operações disponíveis na sessão atual.
- [`%workspace`](xref:microsoft.quantum.iqsharp.magic-ref.workspace): Fornece ações relacionadas ao espaço de trabalho atual.

### <a name="azure-quantum-integration"></a>Integração do azure Quantum

- [`%azure.connect`](xref:microsoft.quantum.iqsharp.magic-ref.azure.connect): Conecta-se a um espaço de trabalho do azure Quantum ou exibe o status da conexão atual.
- [`%azure.execute`](xref:microsoft.quantum.iqsharp.magic-ref.azure.execute): Envia um trabalho para um espaço de trabalho do azure Quantum e aguarda a conclusão.
- [`%azure.jobs`](xref:microsoft.quantum.iqsharp.magic-ref.azure.jobs): Exibe uma lista de trabalhos no espaço de trabalho atual do azure Quantum.
- [`%azure.output`](xref:microsoft.quantum.iqsharp.magic-ref.azure.output): Exibe os resultados de um trabalho no espaço de trabalho atual do azure Quantum.
- [`%azure.status`](xref:microsoft.quantum.iqsharp.magic-ref.azure.status): Exibe o status de um trabalho no espaço de trabalho atual do azure Quantum.
- [`%azure.submit`](xref:microsoft.quantum.iqsharp.magic-ref.azure.submit): Envia um trabalho para um espaço de trabalho do azure Quantum.
- [`%azure.target`](xref:microsoft.quantum.iqsharp.magic-ref.azure.target): Define ou exibe o destino de execução ativa para Q# envio de trabalho em um espaço de trabalho do azure Quantum.

### <a name="chemistry-from-microsoftquantumchemistry-package"></a>Química (do pacote Microsoft. Quantum. química)

- [`%chemistry.broombridge`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.broombridge): Carrega e retorna a representação de problema de estrutura eletrônica Broombridge de um determinado arquivo. YAML.
- [`%chemistry.encode`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.encode): Codifica um Fermion Hamiltonian para um formato consumível pelo Q# .
- [`%chemistry.fh.add_terms`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.fh.add_terms): Adiciona termos a um Fermion Hamiltonian.
- [`%chemistry.fh.load`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.fh.load): Carrega o Fermion Hamiltonian para um problema de estrutura eletrônica. O problema é carregado de um arquivo ou passado como um argumento.
- [`%chemistry.inputstate.load`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.inputstate.load): Carrega o problema de estrutura eletrônica do Broombridge e retorna o estado de entrada selecionado.

### <a name="katas-from-microsoftquantumkatas-package"></a>Katas (do pacote Microsoft. Quantum. katas)

- [`%kata`](xref:microsoft.quantum.iqsharp.magic-ref.kata): Executa um único teste e relata se o teste foi aprovado com êxito.
- [`%check_kata`](xref:microsoft.quantum.iqsharp.magic-ref.check_kata): Verifica a implementação de referência para um único teste de Kata.
    Especificamente, ele substitui a implementação de referência de uma única tarefa na célula e relata se o teste foi aprovado com êxito.
