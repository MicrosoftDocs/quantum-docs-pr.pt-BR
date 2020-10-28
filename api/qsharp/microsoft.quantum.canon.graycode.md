---
uid: Microsoft.Quantum.Canon.GrayCode
title: Função GrayCode
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: GrayCode
qsharp.summary: Creates Gray code sequences
ms.openlocfilehash: fc673ae21a952788b5beb74c1bad94ee9fe54480
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694007"
---
# <a name="graycode-function"></a>Função GrayCode

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Agrupa [](https://nuget.org/packages/)


Cria sequências de código cinza

```qsharp
function GrayCode (n : Int) : (Int, Int)[]
```


## <a name="input"></a>Entrada

### <a name="n--int"></a>n: [int](xref:microsoft.quantum.lang-ref.int)

Número de bits



## <a name="output--intint"></a>Saída: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []

Matriz de tuplas. O primeiro valor na tupla é o valor no segundo valor da sequência GrayCode na tupla é a posição para alterar o valor atual para obter o próximo.