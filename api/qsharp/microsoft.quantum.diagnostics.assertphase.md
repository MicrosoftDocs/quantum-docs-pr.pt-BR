---
uid: Microsoft.Quantum.Diagnostics.AssertPhase
title: Operação AssertPhase
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertPhase
qsharp.summary: Asserts that the phase of an equal superposition state has the expected value.
ms.openlocfilehash: 59fa0f2f68b4de271b972aef776ee5097fd5c201
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830074"
---
# <a name="assertphase-operation"></a>Operação AssertPhase

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Declara que a fase de um estado de superposição igual tem o valor esperado.

```qsharp
operation AssertPhase (expected : Double, qubit : Qubit, tolerance : Double) : Unit
```


## <a name="description"></a>Descrição

Esta operação declara que a fase $ \phi $ de um estado Quantum que pode ser expressa como $ \frac{e ^ {i t}} {\sqrt {2} } (e ^ {i\phi} \ ket {0} + e ^ {-i\phi} \ ket {1} ) $ para algum real $t $ arbitrário tem o valor esperado.

## <a name="input"></a>Entrada

### <a name="expected--double"></a>esperado: [duplo](xref:microsoft.quantum.lang-ref.double)

O valor esperado de $ \phi na (-\pi, \pi] $.


### <a name="qubit--qubit"></a>qubit: [qubit](xref:microsoft.quantum.lang-ref.qubit)

O qubit que armazena o estado esperado.


### <a name="tolerance--double"></a>tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)

Tolerância absoluta na diferença entre real e esperado.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Exemplo

A seguinte declaração é realizada com sucesso: `qubit` está no estado $ \ket{\psi} = e ^ {i 0,5} \ sqrt {1/2} \ ket {0} + e ^ {i 0.5} \ sqrt {1/2} \ ket {1} $;

- `AssertPhase(0.0,qubit,10e-10);`

`qubit` está no estado $ \ket{\psi} = e ^ {i 0,5} \ sqrt {1/2} \ ket {0} + e ^ {-i 0.5} \ sqrt {1/2} \ ket {1} $;

- `AssertPhase(0.5,qubit,10e-10);`

`qubit` está no estado $ \ket{\psi} = e ^ {-i 2.2} \ sqrt {1/2} \ ket {0} + e ^ {i 0.2} \ sqrt {1/2} \ ket {1} $;

- `AssertPhase(-1.2,qubit,10e-10);`