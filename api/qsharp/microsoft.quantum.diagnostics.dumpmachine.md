---
uid: Microsoft.Quantum.Diagnostics.DumpMachine
title: Função DumpMachine
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpMachine
qsharp.summary: Dumps the current target machine's status.
ms.openlocfilehash: e7eb2dfce060b61e27deae31e3c1fc6dc3d7655c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202100"
---
# <a name="dumpmachine-function"></a>Função DumpMachine

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Despeja o status do computador de destino atual.

```qsharp
function DumpMachine<'T> (location : 'T) : Unit
```


## <a name="input"></a>Entrada

### <a name="location--t"></a>local: ' t

Fornece informações sobre onde gerar o despejo da máquina.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

nenhuma.

## <a name="type-parameters"></a>Parâmetros de tipo

### <a name="t"></a>T'



## <a name="remarks"></a>Comentários

Esse método permite despejar informações sobre o status atual do computador de destino em um arquivo ou em algum outro local.
As informações reais geradas e a semântica de `location` são específicas para cada computador de destino. No entanto, fornecer uma tupla vazia como um local ( `()` ) ou simplesmente omitir o `location` parâmetro normalmente significa gerar a saída para o console.

Para o simulador de estado completo local distribuído como parte do kit de desenvolvimento Quantum, esse método espera uma cadeia de caracteres com o caminho para um arquivo no qual ele gravará a função Wave como uma matriz unidimensional de números complexos, na qual cada elemento representa as amplitudes da probabilidade de medir o estado correspondente.