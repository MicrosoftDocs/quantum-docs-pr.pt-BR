---
title: A linguagem de programação Q#
description: Introdução à linguagem Q# para desenvolvimento de programa quântico.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.language.intro
ms.openlocfilehash: b62e6866fc3609d95c26a5eab2a6eac325dfe330
ms.sourcegitcommit: 9d1c045cf1a2c3e19030cb38dbc7496dbd24ab58
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2020
ms.locfileid: "77907368"
---
# <a name="the-q-programming-language"></a>A linguagem de programação Q#

## <a name="introduction"></a>Introdução

Um modelo natural para a computação quântica é tratar o computador quântico como um coprocessador, semelhante àquele usado para GPUs, FPGAs e outros processadores suplementares.
A lógica de controle principal executa o código clássico em um computador "host" clássico.
Quando apropriado e necessário, o programa host pode invocar uma sub-rotina que é executada no processador suplementar.
Quando a sub-rotina é concluída, o programa host obtém acesso aos resultados da sub-rotina.

O Q# (Q-Sharp) é uma linguagem de programação específica de domínio usada para expressar algoritmos quânticos.
Ele deve ser usado para escrever sub-rotinas que são executadas em um processador quântico suplementar, sob o controle de um programa e um computador host clássico.
Até que os processadores quânticos estejam amplamente disponíveis, as sub-rotinas Q# são executadas em um simulador.

O Q# fornece um pequeno conjunto de tipos primitivos, juntamente com duas maneiras (matrizes e tuplas) de criar tipos estruturados.
Ele dá suporte a um modelo de procedimento básico para escrever programas, com loops e instruções if/then.
Os constructos de nível superior no Q# são operações, funções e tipos definidos pelo usuário.

As seguintes seções fornecem detalhes sobre:
- [O modelo de tipo](xref:microsoft.quantum.language.type-model)
- [Expressões](xref:microsoft.quantum.language.expressions)
- [Instruções](xref:microsoft.quantum.language.statements)
- [Estrutura do arquivo](xref:microsoft.quantum.language.file-structure)

## <a name="conventions"></a>Convenções

Estamos trabalhando para garantir que sinais de pontuação comuns sejam usados de forma consistente em todas as situações.
Esperamos que isso torne o Q# mais fácil de ser aprendido e lido, pois esses sinais sempre significam a mesma coisa e o mesmo conceito é sempre representado da mesma maneira.

Especificamente:

- O ponto e vírgula, `;`, é usado para encerrar uma instrução ou uma diretiva de linha única.
  Ele não pode ser usado para nenhuma outra finalidade.
- A vírgula, `,`, é usada para separar elementos de uma sequência. Ela é usada para literais de tupla, literais de matriz, listas de argumentos, definições de tupla e listas de tipos. **Em uma alteração das versões anteriores, não há mais suporte para `;` como um separador de literal de matriz.**
- Os dois-pontos, `:`, são usados para introduzir uma anotação de tipo. Ele é usado principalmente em assinaturas que podem ser chamadas.
  Como os dois-pontos sempre introduzem uma assinatura de tipo, o operador condicional ternário introduzido no 0.3 usa uma barra vertical, `|`, para separar os valores verdadeiros e falsos; portanto, o Q# usa `cond ? tval | fval` em vez dos dois-pontos como separador, como no C.
  
