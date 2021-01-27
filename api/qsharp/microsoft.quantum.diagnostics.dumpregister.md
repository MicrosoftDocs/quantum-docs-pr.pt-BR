---
uid: Microsoft.Quantum.Diagnostics.DumpRegister
title: Função DumpRegister
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpRegister
qsharp.summary: Dumps the current target machine's status associated with the given qubits.
ms.openlocfilehash: 835c7a9edb22b4be630ebfc04587c12b3ff668b2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829225"
---
# <a name="dumpregister-function"></a>Função DumpRegister

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Despeja o status atual da máquina de destino associada ao qubits fornecido.

```qsharp
function DumpRegister<'T> (location : 'T, qubits : Qubit[]) : Unit
```


## <a name="input"></a>Entrada

### <a name="location--t"></a>local: ' t

Fornece informações sobre onde gerar o despejo do estado.


### <a name="qubits--qubit"></a>qubits: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

A lista de qubits a ser reportada.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

Nenhum.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'



## <a name="remarks"></a>Comentários

Esse método permite que você despeje as informações associadas ao estado do determinado qubits em um arquivo ou em algum outro local.
As informações reais geradas e a semântica de `location` são específicas para cada computador de destino. No entanto, fornecer uma tupla vazia como um local ( `()` ) normalmente significa gerar a saída para o console.

Para o simulador de estado completo local distribuído como parte do kit de desenvolvimento Quantum, esse método espera uma cadeia de caracteres com o caminho para um arquivo no qual ele gravará o estado de determinado qubits (ou seja, a função Wave do subsistema correspondente) como uma matriz unidimensional de números complexos, na qual cada elemento representa as amplitudes da probabilidade de medir o estado correspondente.
Se o qubits fornecido for confusas com algum outro qubit e seu estado não puder ser separado, ele apenas relatará que o qubits é confusas.