---
uid: Microsoft.Quantum.Math.RealMod
title: Função RealMod
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: RealMod
qsharp.summary: Computes the modulus between two real numbers.
ms.openlocfilehash: 56da313fabb20655ec358120b8d9b435e4971159
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848356"
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



## <a name="example"></a>Exemplo

```qsharp
    // Returns 3 π / 2.
    let y = RealMod(5.5 * PI(), 2.0 * PI(), 0.0);
    // Returns -1.2, since +3.6 and -1.2 are 4.8 apart on the real line,
    // which is a multiple of 2.4.
    let z = RealMod(3.6, 2.4, -1.2);
```

## <a name="remarks"></a>Comentários

Essa função computa o módulo real encapsulando a linha real sobre o círculo da unidade e, em seguida, localizando o ângulo no círculo da unidade correspondente à entrada.
`minValue`Em seguida, a entrada especifica efetivamente onde recortar o círculo da unidade.