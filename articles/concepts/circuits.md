---
title: Circuitos do Quantum
description: Saiba como representar visualmente operações Quantum simples e complexas com diagramas de circuito Quantum.
author: QuantumWriter
uid: microsoft.quantum.concepts.circuits
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 80d9df00159090768ea442e519c34043a99b050c
ms.sourcegitcommit: d61b388651351e5abd4bfe7a672e88b84a6697f8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2020
ms.locfileid: "79022693"
---
# <a name="quantum-circuits"></a><span data-ttu-id="c0b06-103">Circuitos Quantum</span><span class="sxs-lookup"><span data-stu-id="c0b06-103">Quantum Circuits</span></span>
<span data-ttu-id="c0b06-104">Considere por um momento a transformação unitário $ \Text{CNOT} _{01}(H\otimes 1) $.</span><span class="sxs-lookup"><span data-stu-id="c0b06-104">Consider for a moment the unitary transformation $\text{ CNOT}_{01}(H\otimes 1)$.</span></span>
<span data-ttu-id="c0b06-105">Essa sequência de portão é de importância fundamental para a computação Quantum porque ela cria um estado confusas de duas qubit de maneira máxima:</span><span class="sxs-lookup"><span data-stu-id="c0b06-105">This gate sequence is of fundamental significance to quantum computing because it creates a maximally entangled two-qubit state:</span></span>

<span data-ttu-id="c0b06-106">$ $ \mathrm{CNOT}_{01}(H\otimes 1) \ket{00} = \frac{1}{\sqrt{2}} \left (\ket{00} + \ket{11} \right), $ $</span><span class="sxs-lookup"><span data-stu-id="c0b06-106">$$\mathrm{CNOT}_{01}(H\otimes 1)\ket{00} = \frac{1}{\sqrt{2}} \left(\ket{00} + \ket{11} \right),$$</span></span>

<span data-ttu-id="c0b06-107">As operações com essa ou mais complexidade são onipresentes em algoritmos Quantum e correção de erro Quantum, portanto, deve ser um grande alívio de que há um método simples para sua visualização chamada de *diagrama de circuito Quantum*.</span><span class="sxs-lookup"><span data-stu-id="c0b06-107">Operations with this or greater complexity are ubiquitous in quantum algorithms and quantum error correction, so it should come as a great relief that there is a simple method for their visualization called a *quantum circuit diagram*.</span></span>
<span data-ttu-id="c0b06-108">O diagrama de circuito para preparar esse estado de Quantum de confusas máximo é:</span><span class="sxs-lookup"><span data-stu-id="c0b06-108">The circuit diagram for preparing this maximally entangled quantum state is:</span></span>

<!--- ![](.\media\1.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="c0b06-109">![diagrama de circuito para um estado confusas de dois qubits de duas pontas](~/media/1.svg)</span><span class="sxs-lookup"><span data-stu-id="c0b06-109">![Circuit diagram for a maximally entangled two-qubit state](~/media/1.svg)</span></span>

## <a name="quantum-circuit-diagram-conventions"></a><span data-ttu-id="c0b06-110">Convenções de diagrama de circuito Quantum</span><span class="sxs-lookup"><span data-stu-id="c0b06-110">Quantum circuit diagram conventions</span></span>
<span data-ttu-id="c0b06-111">Essa linguagem visual para operações Quantum pode ser mais prontamente fácil do que escrever sua matriz equivalente quando você entende as convenções para expressar um circuito Quantum.</span><span class="sxs-lookup"><span data-stu-id="c0b06-111">This visual language for quantum operations can be more readily digestible than writing down its equivalent matrix once you understand the conventions for expressing a quantum circuit.</span></span>
<span data-ttu-id="c0b06-112">Analisamos essas convenções abaixo.</span><span class="sxs-lookup"><span data-stu-id="c0b06-112">We review these conventions below.</span></span>

<span data-ttu-id="c0b06-113">Em um diagrama de circuito, cada linha sólida representa um qubit ou mais geralmente um registro de qubit.</span><span class="sxs-lookup"><span data-stu-id="c0b06-113">In a circuit diagram, each solid line depicts a qubit or more generally a qubit register.</span></span>
<span data-ttu-id="c0b06-114">Por convenção, a linha superior é o registro de qubit $0 $ e o resto é rotulado em sequência.</span><span class="sxs-lookup"><span data-stu-id="c0b06-114">By convention, the top line is qubit register $0$ and the remainder are labeled sequentially.</span></span> <span data-ttu-id="c0b06-115">O circuito de exemplo acima é representado como agindo em dois qubits (ou dois registros equivalentes que consistem em um qubit).</span><span class="sxs-lookup"><span data-stu-id="c0b06-115">The above example circuit is depicted as acting on two qubits (or equivalently two registers consisting of one qubit).</span></span>
<span data-ttu-id="c0b06-116">As Gates que atuam em um ou mais registros de qubit são indicadas como uma caixa.</span><span class="sxs-lookup"><span data-stu-id="c0b06-116">Gates acting on one or more qubit registers are denoted as a box.</span></span>
<span data-ttu-id="c0b06-117">Por exemplo, o símbolo</span><span class="sxs-lookup"><span data-stu-id="c0b06-117">For example, the symbol</span></span>

<!--- ![](.\media\2.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="c0b06-118">![símbolo de uma operação de Hadamard que atua em um registro de qubit único](~/media/2.svg)</span><span class="sxs-lookup"><span data-stu-id="c0b06-118">![Symbol for a Hadamard operation acting on a single-qubit register](~/media/2.svg)</span></span>

<span data-ttu-id="c0b06-119">é uma operação [Hadamard](xref:microsoft.quantum.intrinsic.h) que atua em um registro de qubit único.</span><span class="sxs-lookup"><span data-stu-id="c0b06-119">is a [Hadamard](xref:microsoft.quantum.intrinsic.h) operation acting on a single-qubit register.</span></span>

<span data-ttu-id="c0b06-120">As Gates da Quantum são ordenadas em ordem cronológica com a porta mais à esquerda como a portão aplicada pela primeira vez ao qubits.</span><span class="sxs-lookup"><span data-stu-id="c0b06-120">Quantum gates are ordered in chronological order with the left-most gate as the gate first applied to the qubits.</span></span>
<span data-ttu-id="c0b06-121">Em outras palavras, se você modelar os fios como tendo o estado Quantum, os fios trazem o estado da Quantum por meio de cada um dos Gates no diagrama da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="c0b06-121">In other words, if you picture the wires as holding the quantum state, the wires bring the quantum state through each of the gates in the diagram from left to right.</span></span>
<span data-ttu-id="c0b06-122">Isso é para dizer</span><span class="sxs-lookup"><span data-stu-id="c0b06-122">That is to say</span></span> 

<!--- ![](.\media\3.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="c0b06-123">![diagrama de Gates Quantum sendo aplicado da esquerda para a direita](~/media/3.svg)</span><span class="sxs-lookup"><span data-stu-id="c0b06-123">![Diagram of quantum gates being applied left-to-right](~/media/3.svg)</span></span>

<span data-ttu-id="c0b06-124">é a matriz unitário $CBA $.</span><span class="sxs-lookup"><span data-stu-id="c0b06-124">is the unitary matrix $CBA$.</span></span>
<span data-ttu-id="c0b06-125">A multiplicação de matriz obedece à Convenção oposta: a matriz mais à direita é aplicada primeiro.</span><span class="sxs-lookup"><span data-stu-id="c0b06-125">Matrix multiplication obeys the opposite convention: the right-most matrix is applied first.</span></span> <span data-ttu-id="c0b06-126">Em diagramas de circuito Quantum, no entanto, o portão mais à esquerda é aplicado primeiro.</span><span class="sxs-lookup"><span data-stu-id="c0b06-126">In quantum circuit diagrams, however, the left-most gate is applied first.</span></span>
<span data-ttu-id="c0b06-127">Essa diferença pode, às vezes, levar à confusão. portanto, é importante observar essa diferença significativa entre a notação linear algébricas e os diagramas de circuito Quantum.</span><span class="sxs-lookup"><span data-stu-id="c0b06-127">This difference can at times lead to confusion, so it is important to note this significant difference between the linear algebraic notation and quantum circuit diagrams.</span></span>

## <a name="inputs-and-outputs-of-quantum-circuits"></a><span data-ttu-id="c0b06-128">Entradas e saídas de circuitos Quantum</span><span class="sxs-lookup"><span data-stu-id="c0b06-128">Inputs and outputs of quantum circuits</span></span>
<span data-ttu-id="c0b06-129">Todos os exemplos anteriores que tinham tido exatamente o mesmo número de fios (qubits) de entrada para uma porta Quantum como o número de cabos do portão Quantum.</span><span class="sxs-lookup"><span data-stu-id="c0b06-129">All previous examples given have had precisely the same number of wires (qubits) input to a quantum gate as the number of wires out from the quantum gate.</span></span>
<span data-ttu-id="c0b06-130">A princípio, pode parecer razoável que os circuitos Quantum pudessem ter mais, ou menos, saídas do que as entradas em geral.</span><span class="sxs-lookup"><span data-stu-id="c0b06-130">It may at first seem reasonable that quantum circuits could have more, or fewer, outputs than inputs in general.</span></span>
<span data-ttu-id="c0b06-131">No entanto, isso é impossível, pois todas as operações de Quantum, salvar medida, são unitários e, portanto, reversível.</span><span class="sxs-lookup"><span data-stu-id="c0b06-131">This is impossible, however, because all quantum operations, save measurement, are unitary and hence reversible.</span></span>
<span data-ttu-id="c0b06-132">Se eles não tiverem o mesmo número de saídas que não seriam reversível e, portanto, não são unitários, o que é uma contradição.</span><span class="sxs-lookup"><span data-stu-id="c0b06-132">If they did not have the same number of outputs as inputs they would not be reversible and hence not unitary, which is a contradiction.</span></span>
<span data-ttu-id="c0b06-133">Por esse motivo, qualquer caixa desenhada em um diagrama de circuito deve ter precisamente o mesmo número de fios inserindo-o como sendo encerrado.</span><span class="sxs-lookup"><span data-stu-id="c0b06-133">For this reason any box drawn in a circuit diagram must have precisely the same number of wires entering it as exiting it.</span></span>

<span data-ttu-id="c0b06-134">Os diagramas de circuito qubit seguem convenções semelhantes para os qubit únicos.</span><span class="sxs-lookup"><span data-stu-id="c0b06-134">Multi-qubit circuit diagrams follow similar conventions to single-qubit ones.</span></span>
<span data-ttu-id="c0b06-135">Como um exemplo de esclarecimento, podemos definir uma operação qubit de dois unitários $B $ para ser $ (H S\otimes X) $ e expressar o circuito equivalentemente como</span><span class="sxs-lookup"><span data-stu-id="c0b06-135">As a clarifying example, we can define a two-qubit unitary operation $B$ to be $(H S\otimes X)$ and express the circuit equivalently as</span></span>

<!--- ![](.\media\4.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="c0b06-136">![diagrama de circuito de uma operação qubit de duas pontas](~/media/4.svg)</span><span class="sxs-lookup"><span data-stu-id="c0b06-136">![Circuit diagram of a two-qubit unitary operation](~/media/4.svg)</span></span>

<span data-ttu-id="c0b06-137">Também podemos exibir $B $ como tendo uma ação em um único registro de duas qubit em vez de registros de 2 1-qubit, dependendo do contexto no qual o circuito é usado.</span><span class="sxs-lookup"><span data-stu-id="c0b06-137">We can also view $B$ as having an action on a single two-qubit register rather than two one-qubit registers depending on the context in which the circuit is used.</span></span> <span data-ttu-id="c0b06-138">Talvez a propriedade mais útil desses diagramas de circuito abstrato seja que eles permitam que algoritmos de Quantum complicados sejam descritos em um alto nível sem precisar compilá-los em Gates fundamentais.</span><span class="sxs-lookup"><span data-stu-id="c0b06-138">Perhaps the most useful property of such abstract circuit diagrams is that they allow complicated quantum algorithms to be described at a high level without having to compile them down to fundamental gates.</span></span>
<span data-ttu-id="c0b06-139">Isso significa que você pode obter uma intuição sobre o fluxo de dados para um grande algoritmo Quantum sem a necessidade de entender todos os detalhes de como cada uma das sub-rotinas dentro do algoritmo funciona.</span><span class="sxs-lookup"><span data-stu-id="c0b06-139">This means that you can get an intuition about the data flow for a large quantum algorithm without needing to understand all the details of how each of the subroutines within the algorithm work.</span></span>

## <a name="controlled-gates"></a><span data-ttu-id="c0b06-140">Gates controlados</span><span class="sxs-lookup"><span data-stu-id="c0b06-140">Controlled gates</span></span>
<span data-ttu-id="c0b06-141">O outro constructo criado em diagramas de circuito Quantum qubit é Control.</span><span class="sxs-lookup"><span data-stu-id="c0b06-141">The other construct that is built into multi-qubit quantum circuit diagrams is control.</span></span>
<span data-ttu-id="c0b06-142">A ação de um portão controlado de Quantum singular, denotado $ \Lambda (G) $, em que um único valor de qubit controla o aplicativo de $G $, pode ser compreendido observando o exemplo a seguir de uma entrada de estado do produto $ \Lambda (G) (\alpha \ket{0} + \beta \ket{1}) \ket{\psi} = \alpha \ket{0} \ket{\psi} + \beta \ket{1} G\ket {\ psi} $</span><span class="sxs-lookup"><span data-stu-id="c0b06-142">The action of a quantum singly controlled gate, denoted $\Lambda(G)$, where a single qubit's value controls the application of $G$, can be understood by looking at the following example of a product state input $\Lambda(G) (\alpha \ket{0} + \beta \ket{1}) \ket{\psi} = \alpha \ket{0} \ket{\psi} + \beta \ket{1} G\ket{\psi}$.</span></span>
<span data-ttu-id="c0b06-143">Ou seja, a porta controlada se aplica $G $ ao registro que contém $ \psi $ If e somente se o qubit de controle usa o valor $1 $.</span><span class="sxs-lookup"><span data-stu-id="c0b06-143">That is to say, the controlled gate applies $G$ to the register containing $\psi$ if and only if the control qubit takes the value $1$.</span></span>
<span data-ttu-id="c0b06-144">Em geral, descrevemos essas operações controladas em diagramas de circuito como</span><span class="sxs-lookup"><span data-stu-id="c0b06-144">In general, we describe such controlled operations in circuit diagrams as</span></span>

<!--- ![](.\media\5.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="c0b06-145">![diagrama de circuito de um portão individualmente controlado](~/media/5.svg)</span><span class="sxs-lookup"><span data-stu-id="c0b06-145">![Circuit diagram of a singly controlled gate](~/media/5.svg)</span></span>

<span data-ttu-id="c0b06-146">Aqui, o círculo preto denota o bit quântico no qual o portão é controlado e uma transmissão vertical denota o unitário que é aplicado quando o qubit de controle usa o valor $1 $.</span><span class="sxs-lookup"><span data-stu-id="c0b06-146">Here the black circle denotes the quantum bit on which the gate is controlled and a vertical wire denotes the unitary that is applied when the control qubit takes the value $1$.</span></span>
<span data-ttu-id="c0b06-147">Para os casos especiais em que $G = X $ e $G = Z $ apresentamos a notação a seguir para descrever a versão controlada das Gates (Observe que a porta X controlada é a [porta do $CNOT $](xref:microsoft.quantum.intrinsic.cnot)):</span><span class="sxs-lookup"><span data-stu-id="c0b06-147">For the special cases where $G=X$ and $G=Z$ we introduce the following notation to describe the controlled version of the gates (note that the controlled-X gate is the [$CNOT$ gate](xref:microsoft.quantum.intrinsic.cnot)):</span></span>

<!--- ![](.\media\6.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="c0b06-148">diagrama de circuito de ![para casos especiais de Gates controlados](~/media/6.svg)</span><span class="sxs-lookup"><span data-stu-id="c0b06-148">![Circuit diagram for special cases of controlled gates](~/media/6.svg)</span></span>

<span data-ttu-id="c0b06-149">O Q # fornece métodos para gerar automaticamente a versão controlada de uma operação, o que evita que o programador tenha que codificar essas operações manualmente.</span><span class="sxs-lookup"><span data-stu-id="c0b06-149">Q# provides methods to automatically generate the controlled version of an operation, which saves the programmer from having to hand code these operations.</span></span> <span data-ttu-id="c0b06-150">Um exemplo disso é mostrado abaixo:</span><span class="sxs-lookup"><span data-stu-id="c0b06-150">An example of this is shown below:</span></span>

```qsharp
operation PrepareSuperposition(qubit : Qubit) : Unit
is Ctl { // Auto-generate the controlled specialization of the operation
    H(qubit);
}
```

## <a name="measurement-operator"></a><span data-ttu-id="c0b06-151">Operador de medida</span><span class="sxs-lookup"><span data-stu-id="c0b06-151">Measurement operator</span></span>
<span data-ttu-id="c0b06-152">A operação restante a ser visualizada em diagramas de circuito é medida.</span><span class="sxs-lookup"><span data-stu-id="c0b06-152">The remaining operation to visualize in circuit diagrams is measurement.</span></span>
<span data-ttu-id="c0b06-153">A medição usa um registro qubit, mede-o e gera o resultado como informações clássicas.</span><span class="sxs-lookup"><span data-stu-id="c0b06-153">Measurement takes a qubit register, measures it, and outputs the result as classical information.</span></span>
<span data-ttu-id="c0b06-154">Uma operação de medição é denotada por um símbolo de medidor e sempre usa como entrada um registro de qubit (indicado por uma linha sólida) e gera informações clássicas (indicadas por uma linha dupla).</span><span class="sxs-lookup"><span data-stu-id="c0b06-154">A measurement operation is denoted by a meter symbol and always takes as input a qubit register (denoted by a solid line) and outputs classical information (denoted by a double line).</span></span>
<span data-ttu-id="c0b06-155">Especificamente, esse subcircuito é semelhante a:</span><span class="sxs-lookup"><span data-stu-id="c0b06-155">Specifically, such a subcircuit looks like:</span></span>

<!--- ![](.\media\7.svg) ---->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="c0b06-156">![símbolo que representa uma operação de medida](~/media/7.svg)</span><span class="sxs-lookup"><span data-stu-id="c0b06-156">![Symbol representing a measurement operation](~/media/7.svg)</span></span>

<span data-ttu-id="c0b06-157">Q # implementa um [operador de medida](xref:microsoft.quantum.intrinsic.measure) para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="c0b06-157">Q# implements a [Measure operator](xref:microsoft.quantum.intrinsic.measure) for this purpose.</span></span>
<span data-ttu-id="c0b06-158">Consulte a [seção sobre medições](xref:microsoft.quantum.libraries.standard.prelude#measurements) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c0b06-158">See the [section on measurements](xref:microsoft.quantum.libraries.standard.prelude#measurements) for more information.</span></span>

<span data-ttu-id="c0b06-159">Da mesma forma, o subcircuito</span><span class="sxs-lookup"><span data-stu-id="c0b06-159">Similarly, the subcircuit</span></span>

<!--- ![](.\media\8.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="c0b06-160">![diagrama de circuito que representa uma operação controlada](~/media/8.svg)</span><span class="sxs-lookup"><span data-stu-id="c0b06-160">![Circuit diagram representing a controlled operation](~/media/8.svg)</span></span>

<span data-ttu-id="c0b06-161">fornece um portão controlado de forma clássica, em que $G $ é aplicado condicionalmente no bit de controle clássico sendo o valor de $1 $.</span><span class="sxs-lookup"><span data-stu-id="c0b06-161">gives a classically controlled gate, where $G$ is applied conditioned on the classical control bit being value $1$.</span></span>

## <a name="teleportation-circuit-diagram"></a><span data-ttu-id="c0b06-162">Diagrama de circuito de teleportação</span><span class="sxs-lookup"><span data-stu-id="c0b06-162">Teleportation circuit diagram</span></span>
<span data-ttu-id="c0b06-163">A [porta de transporte Quantum](xref:microsoft.quantum.techniques.puttingittogether) talvez seja o melhor algoritmo Quantum para ilustrar esses componentes.</span><span class="sxs-lookup"><span data-stu-id="c0b06-163">[Quantum teleportation](xref:microsoft.quantum.techniques.puttingittogether) is perhaps the best quantum algorithm for illustrating these components.</span></span>
<span data-ttu-id="c0b06-164">A teleportabilidade Quantum é um método para mover dados dentro de um computador Quantum (ou até mesmo entre computadores Quantum distantes em uma rede Quantum) por meio do uso de Entanglement e medição.</span><span class="sxs-lookup"><span data-stu-id="c0b06-164">Quantum teleportation is a method for moving data within a quantum computer (or even between distant quantum computers in a quantum network) through the use of entanglement and measurement.</span></span>
<span data-ttu-id="c0b06-165">Curiosamente, é realmente capaz de mover um estado Quantum, digamos o valor em um determinado qubit, de um qubit para outro, sem nem mesmo saber qual é o valor da qubit!</span><span class="sxs-lookup"><span data-stu-id="c0b06-165">Interestingly, it is actually capable of moving a quantum state, say the value in a given qubit, from one qubit to another, without even knowing what the qubit's value is!</span></span>
<span data-ttu-id="c0b06-166">Isso é necessário para que o protocolo funcione de acordo com as leis da mecânica quantum.</span><span class="sxs-lookup"><span data-stu-id="c0b06-166">This is necessary for the protocol to work according to the laws of quantum mechanics.</span></span>
<span data-ttu-id="c0b06-167">O circuito de teleportabilidade Quantum é fornecido abaixo; também fornecemos uma versão anotada do circuito para ilustrar como ler o circuito Quantum.</span><span class="sxs-lookup"><span data-stu-id="c0b06-167">The quantum teleportation circuit is given below; we also provide an annotated version of the circuit to illustrate how to read the quantum circuit.</span></span>

<!--- ![](.\media\tp2.svg){ width=50% } --->
<span data-ttu-id="c0b06-168">![circuito de teleportagem Quantum](~/media/tp2.svg)</span><span class="sxs-lookup"><span data-stu-id="c0b06-168">![Quantum teleportation circuit](~/media/tp2.svg)</span></span>
