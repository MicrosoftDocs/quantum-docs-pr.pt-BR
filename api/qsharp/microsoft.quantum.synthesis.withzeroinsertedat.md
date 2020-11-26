---
uid: Microsoft.Quantum.Synthesis.WithZeroInsertedAt
title: Função WithZeroInsertedAt
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: WithZeroInsertedAt
qsharp.summary: Insert a 0-bit into an integer
ms.openlocfilehash: 414b703151b9152aa69709d9c28e68e5ae63506f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228858"
---
# <a name="withzeroinsertedat-function"></a>Função WithZeroInsertedAt

Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Inserir um 0-bit em um número inteiro

```qsharp
function WithZeroInsertedAt (position : Int, value : Int) : Int
```


## <a name="description"></a>Descrição

Essa operação usa um número inteiro, insere um 0 no bit `position` e retorna o valor atualizado como um inteiro.  Por exemplo, inserir um 0 na posição 2 no número 10 (US $10 _ {10} = 1010_ {2} $) retorna o número 18 ($18 _ {10} = 10010_ {2} $).

## <a name="input"></a>Entrada

### <a name="position--int"></a>posição: [int](xref:microsoft.quantum.lang-ref.int)

A posição na qual 0 é inserido


### <a name="value--int"></a>valor: [int](xref:microsoft.quantum.lang-ref.int)

O valor que é modificado



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)

Valor modificado