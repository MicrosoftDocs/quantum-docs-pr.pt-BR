---
uid: Microsoft.Quantum.Synthesis.Encoded
title: Função codificada
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Encoded
qsharp.summary: Encode truth table in {1,-1} coding
ms.openlocfilehash: 44f6b247e6bfab7b55c46146cb63f8b6d219955b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855490"
---
# <a name="encoded-function"></a>Função codificada

Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Codificar a tabela verdade na {1,-1} codificação

```qsharp
function Encoded (table : Bool[]) : Int[]
```


## <a name="input"></a>Entrada

### <a name="table--bool"></a>tabela: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Verdade, tabela como matriz de valores da verdade



## <a name="output--int"></a>Saída: [int](xref:microsoft.quantum.lang-ref.int)[]

Verdadeira tabela como matriz de {1,-1} inteiros

## <a name="example"></a>Exemplo

```qsharp
Encoded([false, false, false, true]); // [1, 1, 1, -1]
```