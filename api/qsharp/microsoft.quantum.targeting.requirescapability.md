---
uid: Microsoft.Quantum.Targeting.RequiresCapability
title: Tipo definido pelo usuário RequiresCapability
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Targeting
qsharp.name: RequiresCapability
qsharp.summary: Compiler-recognized attribute used to mark a callable with the runtime capabilities it requires.
ms.openlocfilehash: 5e0db49d6f73398ac36003eb0f44e3a6520b7f1e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855145"
---
# <a name="requirescapability-user-defined-type"></a>Tipo definido pelo usuário RequiresCapability

Namespace: [Microsoft. Quantum. direcionamento](xref:Microsoft.Quantum.Targeting)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Atributo reconhecido pelo compilador usado para marcar um callable com os recursos de tempo de execução necessários.

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype RequiresCapability = (Level : String, Reason : String);
```



## <a name="named-items"></a>Itens nomeados

### <a name="level--string"></a>Nível: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)

O nome do nível de funcionalidade de tempo de execução exigido pelo callable.
### <a name="reason--string"></a>Motivo: [cadeia de caracteres](xref:microsoft.quantum.lang-ref.string)

Uma descrição do motivo pelo qual o callable requer esse recurso de tempo de execução.

## <a name="remarks"></a>Comentários

Esse atributo é adicionado automaticamente aos chamadores pelo compilador, a menos que uma instância desse atributo já exista no callable. Ele não deve ser usado, exceto em casos raros em que o compilador não infere o recurso necessário corretamente.

Abaixo está a lista de nomes de nível de capacidade, em ordem crescente de recursos ou decrescentes de restrições:

## `"BasicQuantumFunctionality"`

Os resultados da medida não podem ser comparados para igualdade.

## `"BasicMeasurementFeedback"`

Os resultados da medição podem ser comparados somente para igualdade em expressões condicionais If-Statement em operações. O bloco de uma instrução If que depende de um resultado não pode conter instruções SET para variáveis mutáveis declaradas fora do bloco ou instruções de retorno.

## `"FullComputation"`

Nenhuma restrição de tempo de execução. Qualquer programa Q # pode ser executado.