---
uid: Microsoft.Quantum.Math.RealMod
title: Função RealMod
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: RealMod
qsharp.summary: Computes the modulus between two real numbers.
ms.openlocfilehash: 20916d8462288395384aa875bfae4f042ba6b6ad
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228246"
---
# <a name="realmod-function"></a>Função RealMod

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Computa o módulo entre dois números reais.

```qsharp
function RealMod (value : Double, modulo : Double, minValue : Double) : Double
```


## <a name="input"></a>Entrada

### <a name="value--double"></a>valor: [duplo](xref:microsoft.quantum.lang-ref.double)

Um número real $x $ para pegar o módulo de.


### <a name="modulo--double"></a>módulo: [duplo](xref:microsoft.quantum.lang-ref.double)

Um número real para pegar o módulo de $x $ com relação a.


### <a name="minvalue--double"></a>minValue: [Double](xref:microsoft.quantum.lang-ref.double)

O menor valor a ser retornado por essa função.



## <a name="output--double"></a>Saída: [duplo](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>Comentários

Essa função computa o módulo real encapsulando a linha real sobre o círculo da unidade e, em seguida, localizando o ângulo no círculo da unidade correspondente à entrada.
`minValue`Em seguida, a entrada especifica efetivamente onde recortar o círculo da unidade.