---
uid: Microsoft.Quantum.Arrays.IsPermutation
title: Função ismutation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsPermutation
qsharp.summary: Outputs true if and only if a given array represents a permutation.
ms.openlocfilehash: 7e563650f33b0292e1e41f629829a2d3b9e5fd28
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848089"
---
# <a name="ispermutation-function"></a>Função ismutation

Namespace: [Microsoft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gera true se e somente se uma determinada matriz representar uma permutação.

```qsharp
function IsPermutation (permuation : Int[]) : Bool
```


## <a name="description"></a>Descrição

Dada uma matriz `array` de comprimento `n` , retorna true se e somente se cada inteiro de `0` para `n - 1` aparecer exatamente uma vez em `array` , de modo que `array` possa ser interpretado como uma permutação nos `n` elementos.

## <a name="input"></a>Entrada

### <a name="permuation--int"></a>permuation: [int](xref:microsoft.quantum.lang-ref.int)[]

Uma matriz que pode ou não representar uma permutação.



## <a name="output--bool"></a>Saída: [bool](xref:microsoft.quantum.lang-ref.bool)



## <a name="example"></a>Exemplo

O código Q # a seguir imprime a mensagem "todos os diagnósticos foram concluídos com êxito":

```qsharp
Fact(IsPermutation([2, 0, 1], "");
Contradiction(IsPermutation([5, 0, 1], "[5, 0, 1] isn't a permutation");
Message("All diagnostics completed successfully.");
```

## <a name="remarks"></a>Comentários

Uma matriz de comprimento zero é uma simples permuta.