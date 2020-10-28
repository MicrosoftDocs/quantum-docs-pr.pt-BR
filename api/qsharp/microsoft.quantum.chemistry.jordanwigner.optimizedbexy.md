---
uid: Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEXY
title: Operação OptimizedBEXY
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: OptimizedBEXY
qsharp.summary: A unitary $U$ that applies the Pauli string on $(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0$ on qubits $0..p$ conditioned on an index $z\in\{0,1\}$ and $p$. That is, $$ \begin{align} U\ket{z}\ket{p}\ket{\psi} = \ket{z}\ket{p}(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0\ket{\psi} \end{align} $$
ms.openlocfilehash: 359d347fc57be46200a218646911a7a400b4a96d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693685"
---
# <a name="optimizedbexy-operation"></a><span data-ttu-id="16b40-102">Operação OptimizedBEXY</span><span class="sxs-lookup"><span data-stu-id="16b40-102">OptimizedBEXY operation</span></span>

<span data-ttu-id="16b40-103">Namespace: [Microsoft. Quantum. química. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="16b40-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="16b40-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="16b40-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="16b40-105">Um unitário $U $ que aplica a cadeia de caracteres Pauli em $ (X ^ {z + 1} \_ pY ^ {z} \_ p) z \_ {p-1}... Z_0 $ em qubits $0.. p $ conditioned em um índice $z na \{ 0, 1 \} $ e $p $.</span><span class="sxs-lookup"><span data-stu-id="16b40-105">A unitary $U$ that applies the Pauli string on $(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0$ on qubits $0..p$ conditioned on an index $z\in\{0,1\}$ and $p$.</span></span> <span data-ttu-id="16b40-106">Ou seja, $ $ \begin{align} U\ket {z} \ ket {p} \ ket {\ psi} = \ket{z}\ket{p} (X ^ {z + 1} \_ pY ^ {z} \_ p) z \_ {p-1}... Z_0 \ket{\psi} \end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="16b40-106">That is, $$ \begin{align} U\ket{z}\ket{p}\ket{\psi} = \ket{z}\ket{p}(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0\ket{\psi} \end{align} $$</span></span>

```qsharp
operation OptimizedBEXY (pauliBasis : Qubit, indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian, targetRegister : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="16b40-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="16b40-107">Input</span></span>

### <a name="paulibasis--qubit"></a><span data-ttu-id="16b40-108">pauliBasis: [qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="16b40-108">pauliBasis : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="16b40-109">Quando esse qubit está no estado $ \ket {0} $, $X $ é aplicado.</span><span class="sxs-lookup"><span data-stu-id="16b40-109">When this qubit is in state $\ket{0}$, $X$ is applied.</span></span> <span data-ttu-id="16b40-110">Quando está no estado $ \ket {1} $, $Y $ é aplicado.</span><span class="sxs-lookup"><span data-stu-id="16b40-110">When it is in state $\ket{1}$, $Y$ is applied.</span></span>


### <a name="indexregister--littleendian"></a><span data-ttu-id="16b40-111">indexRegister: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="16b40-111">indexRegister : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="16b40-112">O estado $ \ket{p} $ deste registro determina o qubit no qual $X $ ou $Y $ é aplicado.</span><span class="sxs-lookup"><span data-stu-id="16b40-112">The state $\ket{p}$ of this register determines the qubit on which $X$ or $Y$ is applied.</span></span>


### <a name="targetregister--qubit"></a><span data-ttu-id="16b40-113">targetRegister: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="16b40-113">targetRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="16b40-114">Registro de qubits em que os operadores Pauli são aplicados.</span><span class="sxs-lookup"><span data-stu-id="16b40-114">Register of qubits on which the Pauli operators are applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="16b40-115">Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="16b40-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="16b40-116">Referências</span><span class="sxs-lookup"><span data-stu-id="16b40-116">References</span></span>

- <span data-ttu-id="16b40-117">Codificação eletrônica de Spectra em circuitos Quantum com complexidade T linear Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru fosco, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span><span class="sxs-lookup"><span data-stu-id="16b40-117">Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru Paler, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span></span>