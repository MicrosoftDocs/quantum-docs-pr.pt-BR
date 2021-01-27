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
# <a name="assertqubitisinstatewithintolerance-operation"></a><span data-ttu-id="8ac90-102">Operação AssertQubitIsInStateWithinTolerance</span><span class="sxs-lookup"><span data-stu-id="8ac90-102">AssertQubitIsInStateWithinTolerance operation</span></span>

<span data-ttu-id="8ac90-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="8ac90-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="8ac90-104">Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="8ac90-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="8ac90-105">Declara que um qubit no estado esperado.</span><span class="sxs-lookup"><span data-stu-id="8ac90-105">Asserts that a qubit in the expected state.</span></span>

<span data-ttu-id="8ac90-106">`expected` representa um vetor complexo, $ \ket{\psi} = \begin{bmatrix}a & b\end {bmatrix} ^ {\mathrm{T}} $.</span><span class="sxs-lookup"><span data-stu-id="8ac90-106">`expected` represents a complex vector, $\ket{\psi} = \begin{bmatrix}a & b\end{bmatrix}^{\mathrm{T}}$.</span></span>
<span data-ttu-id="8ac90-107">O primeiro elemento das tuplas que representa cada $a $, $b $ é a parte real do número complexo, enquanto o segundo é a parte imaginária.</span><span class="sxs-lookup"><span data-stu-id="8ac90-107">The first element of the tuples representing each of $a$, $b$ is the real part of the complex number, while the second one is the imaginary part.</span></span>
<span data-ttu-id="8ac90-108">O último argumento define a tolerância com a qual a declaração é feita.</span><span class="sxs-lookup"><span data-stu-id="8ac90-108">The last argument defines the tolerance with which assertion is made.</span></span>

```qsharp
operation AssertQubitIsInStateWithinTolerance (expected : (Microsoft.Quantum.Math.Complex, Microsoft.Quantum.Math.Complex), register : Qubit, tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="8ac90-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="8ac90-109">Input</span></span>

### <a name="expected--complexcomplex"></a><span data-ttu-id="8ac90-110">esperado: ([complexo](xref:Microsoft.Quantum.Math.Complex),[complexo](xref:Microsoft.Quantum.Math.Complex))</span><span class="sxs-lookup"><span data-stu-id="8ac90-110">expected : ([Complex](xref:Microsoft.Quantum.Math.Complex),[Complex](xref:Microsoft.Quantum.Math.Complex))</span></span>

<span data-ttu-id="8ac90-111">Amplitudes complexas esperadas para $ \ket {0} $ e $ \ket {1} $, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="8ac90-111">Expected complex amplitudes for $\ket{0}$ and $\ket{1}$, respectively.</span></span>


### <a name="register--qubit"></a><span data-ttu-id="8ac90-112">registrar: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="8ac90-112">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="8ac90-113">Qubit cujo estado deve ser declarado.</span><span class="sxs-lookup"><span data-stu-id="8ac90-113">Qubit whose state is to be asserted.</span></span> <span data-ttu-id="8ac90-114">Observe que esse qubit é considerado separáveis de outros qubits alocados, e não confusas.</span><span class="sxs-lookup"><span data-stu-id="8ac90-114">Note that this qubit is assumed to be separable from other allocated qubits, and not entangled.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="8ac90-115">tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8ac90-115">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8ac90-116">A tolerância aditiva pela qual as amplitudes reais têm permissão para se desviar do esperado.</span><span class="sxs-lookup"><span data-stu-id="8ac90-116">Additive tolerance by which actual amplitudes are allowed to deviate from expected.</span></span>
<span data-ttu-id="8ac90-117">Consulte os comentários abaixo para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="8ac90-117">See remarks below for details.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8ac90-118">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8ac90-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="8ac90-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8ac90-119">Example</span></span>

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

## <a name="remarks"></a><span data-ttu-id="8ac90-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ac90-120">Remarks</span></span>

<span data-ttu-id="8ac90-121">O código Mathematica a seguir pode ser usado para verificar expressões para mi, MX, My, MZ:</span><span class="sxs-lookup"><span data-stu-id="8ac90-121">The following Mathematica code can be used to verify expressions for mi, mx, my, mz:</span></span>

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

<span data-ttu-id="8ac90-122">A tolerância é a $L \_ {\infty} $ Distance entre 3 vetores de dimensão real (x ₂, x ₃, x ₄) definido por $ \langle\psi | \psi\rangle = x \_ 1 I + x \_ 2 x + x \_ 3 y + x \_ 4 Z $ e real vector (y ₂, y ₃, y ₄) definido por ρ = y ₁ I + y ₂ x + y ₃ Y + Y ₄ Z, em que ρ é a matriz de densidade correspondente ao estado do registro.</span><span class="sxs-lookup"><span data-stu-id="8ac90-122">The tolerance is the $L\_{\infty}$ distance between 3 dimensional real vector (x₂,x₃,x₄) defined by $\langle\psi|\psi\rangle = x\_1 I + x\_2 X + x\_3 Y + x\_4 Z$ and real vector (y₂,y₃,y₄) defined by ρ = y₁I + y₂X + y₃Y + y₄Z where ρ is the density matrix corresponding to the state of the register.</span></span>
<span data-ttu-id="8ac90-123">Isso só é verdade na suposição de que TR (ρ) e Tr (| ψ ⟩ ⟨ ψ |) são 1 (por exemplo, x ₁ = 1/2, y ₁ = 1/2).</span><span class="sxs-lookup"><span data-stu-id="8ac90-123">This is only true under the assumption that Tr(ρ) and Tr(|ψ⟩⟨ψ|) are both 1 (e.g. x₁ = 1/2, y₁ = 1/2).</span></span>
<span data-ttu-id="8ac90-124">Se esse não for o caso, a função declara que a distância de l ∞ entre (x ₂-x ₁, x ₃-x ₁, x ₄-x ₁, x ₄ + x ₁) e (y ₂-y ₁, y ₃-y ₁, y ₄-y ₁, y ₄ + y ₁) é menor do que o parâmetro de tolerância.</span><span class="sxs-lookup"><span data-stu-id="8ac90-124">If this is not the case, the function asserts that l∞ distance between (x₂-x₁,x₃-x₁,x₄-x₁,x₄+x₁) and (y₂-y₁,y₃-y₁,y₄-y₁,y₄+y₁) is less than the tolerance parameter.</span></span>