---
uid: Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance
title: Operação AssertQubitIsInStateWithinTolerance
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubitIsInStateWithinTolerance
qsharp.summary: >-
  Asserts that a qubit in the expected state.

  `expected` represents a complex vector, $\ket{\psi} = \begin{bmatrix}a & b\end{bmatrix}^{\mathrm{T}}$. The first element of the tuples representing each of $a$, $b$ is the real part of the complex number, while the second one is the imaginary part. The last argument defines the tolerance with which assertion is made.
ms.openlocfilehash: b40c5c4f731190c8c0d00d33718680e5448bf767
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829794"
---
# <a name="assertqubitisinstatewithintolerance-operation"></a>Operação AssertQubitIsInStateWithinTolerance

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Declara que um qubit no estado esperado.

`expected` representa um vetor complexo, $ \ket{\psi} = \begin{bmatrix}a & b\end {bmatrix} ^ {\mathrm{T}} $.
O primeiro elemento das tuplas que representa cada $a $, $b $ é a parte real do número complexo, enquanto o segundo é a parte imaginária.
O último argumento define a tolerância com a qual a declaração é feita.

```qsharp
operation AssertQubitIsInStateWithinTolerance (expected : (Microsoft.Quantum.Math.Complex, Microsoft.Quantum.Math.Complex), register : Qubit, tolerance : Double) : Unit
```


## <a name="input"></a>Entrada

### <a name="expected--complexcomplex"></a>esperado: ([complexo](xref:Microsoft.Quantum.Math.Complex),[complexo](xref:Microsoft.Quantum.Math.Complex))

Amplitudes complexas esperadas para $ \ket {0} $ e $ \ket {1} $, respectivamente.


### <a name="register--qubit"></a>registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit cujo estado deve ser declarado. Observe que esse qubit é considerado separáveis de outros qubits alocados, e não confusas.


### <a name="tolerance--double"></a>tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)

A tolerância aditiva pela qual as amplitudes reais têm permissão para se desviar do esperado.
Consulte os comentários abaixo para obter detalhes.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Exemplo

```qsharp
using (qubits = Qubit[2]) {
    // Both qubits are initialized as |0〉: a=(1 + 0*i), b=(0 + 0*i)
    AssertQubitIsInStateWithinTolerance((Complex(1., 0.), Complex(0., 0.)), qubits[0], 1e-5);
    AssertQubitIsInStateWithinTolerance((Complex(1., 0.), Complex(0., 0.)), qubits[1], 1e-5);
    Y(qubits[1]);
    // Y |0〉 = i |1〉: a=(0 + 0*i), b=(0 + 1*i)
    AssertQubitIsInStateWithinTolerance((Complex(0., 0.), Complex(0., 1.)), qubits[1], 1e-5);
}
```

## <a name="remarks"></a>Comentários

O código Mathematica a seguir pode ser usado para verificar expressões para mi, MX, My, MZ:

```mathematica
{Id, X, Y, Z} = Table[PauliMatrix[k], {k, 0, 3}];
st = {{ reA + I imA }, { reB + I imB} };
M = st . ConjugateTranspose[st];
mx = Tr[M.X] // ComplexExpand;
my = Tr[M.Y] // ComplexExpand;
mz = Tr[M.Z] // ComplexExpand;
mi = Tr[M.Id] // ComplexExpand;
2 m == Id mi + X mx + Z mz + Y my // ComplexExpand // Simplify
```

A tolerância é a $L \_ {\infty} $ Distance entre 3 vetores de dimensão real (x ₂, x ₃, x ₄) definido por $ \langle\psi | \psi\rangle = x \_ 1 I + x \_ 2 x + x \_ 3 y + x \_ 4 Z $ e real vector (y ₂, y ₃, y ₄) definido por ρ = y ₁ I + y ₂ x + y ₃ Y + Y ₄ Z, em que ρ é a matriz de densidade correspondente ao estado do registro.
Isso só é verdade na suposição de que TR (ρ) e Tr (| ψ ⟩ ⟨ ψ |) são 1 (por exemplo, x ₁ = 1/2, y ₁ = 1/2).
Se esse não for o caso, a função declara que a distância de l ∞ entre (x ₂-x ₁, x ₃-x ₁, x ₄-x ₁, x ₄ + x ₁) e (y ₂-y ₁, y ₃-y ₁, y ₄-y ₁, y ₄ + y ₁) é menor do que o parâmetro de tolerância.