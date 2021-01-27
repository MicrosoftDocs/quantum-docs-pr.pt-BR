---
uid: Microsoft.Quantum.Diagnostics.DumpOperation
title: Operação DumpOperation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpOperation
qsharp.summary: Given an operation, displays diagnostics about the operation that are made available by the current execution target.
ms.openlocfilehash: cde188806506c586c4c77a7f9b2b43ad0e10ef1b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829270"
---
# <a name="dumpoperation-operation"></a>Operação DumpOperation

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dada uma operação, exibe o diagnóstico sobre a operação disponibilizada pelo destino de execução atual.

```qsharp
operation DumpOperation (nQubits : Int, op : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a>Entrada

### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

O número de qubits em que a operação fornecida funciona.


### <a name="op--qubit--unit--is-adj"></a>op: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj

A operação a ser diagnosticada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Exemplo

Quando executado no destino do simulador do Quantum, o trecho a seguir produzirá a matriz $ $ \begin{aligned} \left (\begin{Matrix} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \end{Matrix}\right) \end{aligned}.
$$

```qsharp
operation DumpCnot() : Unit {
    DumpOperation(2, ApplyToFirstTwoQubitsCA(CNOT, _));
}
```

## <a name="remarks"></a>Comentários

Chamar esta operação não tem nenhum efeito observável de em Q #. Os diagnósticos exatos que são exibidos, se houver, dependem do ambiente de destino e do editor de execução atual.
Por exemplo, quando usado no simulador de Quantum de estado completo, é exibida uma matriz unitário usada para representar `op` .

Observe que, quando executado em simuladores que admitem uma ambiguidade de fase global (por exemplo: o simulador de estado completo), representações retornadas podem variar até uma fase global.

Da mesma forma, a ordenação de representações de matriz de linhas e colunas pode variar com as convenções usadas por cada simulador que dá suporte a essa operação.