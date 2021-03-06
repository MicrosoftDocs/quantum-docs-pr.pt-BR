---
uid: Microsoft.Quantum.Preparation.PrepareChoiState
title: Operação PrepareChoiState
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareChoiState
qsharp.summary: Prepares the Choi–Jamiołkowski state for a given operation onto given reference and target registers.
ms.openlocfilehash: cb34078c09f8c28b5b9bbda1bae6936d13ffcc78
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854395"
---
# <a name="preparechoistate-operation"></a>Operação PrepareChoiState

Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Prepara o estado Choi – Jamiołkowski para uma determinada operação em determinados registros de referência e destino.

```qsharp
operation PrepareChoiState (op : (Qubit[] => Unit), reference : Qubit[], target : Qubit[]) : Unit
```


## <a name="input"></a>Entrada

### <a name="op--qubit--unit"></a>op: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de> 

A operação $ \Lambda $ cujo Choi de estado $J (\Lambda)/2 ^ N $ deve ser preparada, em que $N $ é o número de qubits em que os `op` atos atuam.


### <a name="reference--qubit"></a>referência: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Um registro de qubits a partir do estado $ \ket{00\cdots 0} $ a ser usado como uma referência para a ação de `op` .


### <a name="target--qubit"></a>destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Um registro de qubits inicialmente no estado $ \ket{00\cdots 0} $ no qual deve `op` ser aplicado.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

O \Lambda (Choi-Jamiłkowski State $J) $ de um processo Quantum é definido como $ $ \begin{align} J (\Lambda) \mathrel{: =} (\boldone \otimes \Lambda) (| \boldone\rangle \! \rangle\langle \! \langle\boldone |), \end{Align} $ $, em que $ | X\rangle \! \rangle $ é a *vetorização* de uma matriz $X $ na Convenção de empilhamento de coluna. Aprender uma descrição clássica desse Estado fornece informações completas sobre o efeito de $ \Lambda $ agindo em Estados de entrada arbitrários e forma a base do *processo Quantum tomography*.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Preparation. PrepareChoiStateA](xref:Microsoft.Quantum.Preparation.PrepareChoiStateA)
- [Microsoft. Quantum. Preparation. PrepareChoiStateC](xref:Microsoft.Quantum.Preparation.PrepareChoiStateC)
- [Microsoft. Quantum. Preparation. PrepareChoiStateCA](xref:Microsoft.Quantum.Preparation.PrepareChoiStateCA)