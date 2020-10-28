---
uid: Microsoft.Quantum.Canon.NoOp
title: Operação NoOp
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: NoOp
qsharp.summary: Performs the identity operation (no-op) on an argument.
ms.openlocfilehash: 987e39577c3b736418234431ed7a915ae461f763
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693949"
---
# <a name="noop-operation"></a>Operação NoOp

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Executa a operação de identidade (não op) em um argumento.

```qsharp
operation NoOp<'T> (input : 'T) : Unit
```


## <a name="description"></a>Descrição

Essa operação usa um valor de qualquer tipo e não faz nada a ele.
Isso pode ser útil sempre que uma entrada de um tipo de operação é esperada, mas nenhuma ação deve ser executada.
Por exemplo, se uma determinada síndrome de correção de erro indicar que nenhum erro ocorreu, `NoOp<Qubit[]>` pode ser o procedimento de recuperação correto.
Da mesma forma, se uma operação espera um procedimento de preparação de estado como entrada, `NoOp<Qubit[]>` pode ser usada para preparar o estado $ \ket{0 \cdots 0} $.

## <a name="input"></a>Entrada

### <a name="input--t"></a>entrada: ' t

Um valor a ser ignorado.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'



## <a name="remarks"></a>Comentários

Em quase todos os casos, o parâmetro de tipo para `NoOp` precisa ser especificado explicitamente. Por exemplo, `NoOp<Qubit>` é idêntico a <xref:microsoft.quantum.intrinsic.i> .

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. intrínseca. I](xref:Microsoft.Quantum.Intrinsic.I)