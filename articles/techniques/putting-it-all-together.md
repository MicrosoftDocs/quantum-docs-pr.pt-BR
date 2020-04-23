---
title: Q# técnicas - Juntando tudo
description: Passe por um programa básico q# que demonstre teletransporte quântico.
uid: microsoft.quantum.techniques.puttingittogether
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 4bd91699017e4c1acd9f4449b8a65e39bd07878e
ms.sourcegitcommit: b6b8459eb654040f1e19f66411b29fc9e48e95c9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2020
ms.locfileid: "82030558"
---
# <a name="putting-it-all-together-teleportation"></a><span data-ttu-id="aa27d-103">Colocando tudo junto: teletransporte</span><span class="sxs-lookup"><span data-stu-id="aa27d-103">Putting It All Together: Teleportation</span></span> #
<span data-ttu-id="aa27d-104">Voltemos ao exemplo do circuito de teletransporte definido em [Circuitos Quânticos.](xref:microsoft.quantum.concepts.circuits)</span><span class="sxs-lookup"><span data-stu-id="aa27d-104">Let's return to the example of the teleportation circuit defined in [Quantum Circuits](xref:microsoft.quantum.concepts.circuits).</span></span> <span data-ttu-id="aa27d-105">Vamos usar isso para ilustrar os conceitos que aprendemos até agora.</span><span class="sxs-lookup"><span data-stu-id="aa27d-105">We're going to use this to illustrate the concepts we've learned so far.</span></span> <span data-ttu-id="aa27d-106">Uma explicação do teletransporte quântico é fornecida abaixo para aqueles que não estão familiarizados com a teoria, seguido por um passo a passo da implementação do código em Q#.</span><span class="sxs-lookup"><span data-stu-id="aa27d-106">An explanation of quantum teleportation is provided below for those who are unfamiliar with the theory, followed by a walkthrough of the code implementation in Q#.</span></span> 

## <a name="quantum-teleportation-theory"></a><span data-ttu-id="aa27d-107">Teletransporte Quântico: Teoria</span><span class="sxs-lookup"><span data-stu-id="aa27d-107">Quantum Teleportation: Theory</span></span>
<span data-ttu-id="aa27d-108">Teletransporte quântico é uma técnica para enviar um estado quântico desconhecido (que vamos nos referir como a '__mensagem__') de um qubit em um local para um qubit em outro local (vamos nos referir a esses qubits como '__aqui__' e '__lá__', respectivamente).</span><span class="sxs-lookup"><span data-stu-id="aa27d-108">Quantum teleportation is a technique for sending an unknown quantum state (which we'll refer to as the '__message__') from a qubit in one location to a qubit in another location (we'll refer to these qubits as '__here__' and '__there__', respectively).</span></span> <span data-ttu-id="aa27d-109">Podemos representar nossa __mensagem__ como um vetor usando a notação Dirac:</span><span class="sxs-lookup"><span data-stu-id="aa27d-109">We can represent our __message__ as a vector using Dirac notation:</span></span> 

<span data-ttu-id="aa27d-110">$$ \ket{\psi} = \alfa\ket{0} +{1} \beta\ket $$</span><span class="sxs-lookup"><span data-stu-id="aa27d-110">$$ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $$</span></span>

<span data-ttu-id="aa27d-111">O estado do qubit de __mensagem__ é desconhecido para nós, pois não sabemos os valores de $\alpha$ e $\beta$.</span><span class="sxs-lookup"><span data-stu-id="aa27d-111">The __message__ qubit's state is unknown to us as we do not know the values of $\alpha$ and $\beta$.</span></span>

### <a name="step-1-create-an-entangled-state"></a><span data-ttu-id="aa27d-112">Passo 1: Criar um estado emaranhado</span><span class="sxs-lookup"><span data-stu-id="aa27d-112">Step 1: Create an entangled state</span></span>
<span data-ttu-id="aa27d-113">Para enviar a __mensagem__ precisamos que o qubit __aqui__ fique emaranhado com o qubit __lá.__</span><span class="sxs-lookup"><span data-stu-id="aa27d-113">In order to send the __message__ we need for the qubit __here__ to be entangled with the qubit __there__.</span></span> <span data-ttu-id="aa27d-114">Isso é conseguido aplicando um portão Hadamard, seguido por um portão CNOT.</span><span class="sxs-lookup"><span data-stu-id="aa27d-114">This is achieved by applying a Hadamard gate, followed by a CNOT gate.</span></span> <span data-ttu-id="aa27d-115">Vamos ver a matemática por trás dessas operações do portal.</span><span class="sxs-lookup"><span data-stu-id="aa27d-115">Let's look at the math behind these gate operations.</span></span>

<span data-ttu-id="aa27d-116">Vamos começar com os qubits __aqui__ e __ali__ ambos no estado de $ket{0}$ .</span><span class="sxs-lookup"><span data-stu-id="aa27d-116">We will begin with the qubits __here__ and __there__ both in the $\ket{0}$ state.</span></span> <span data-ttu-id="aa27d-117">Depois de envolver esses qubits, eles estão no estado:</span><span class="sxs-lookup"><span data-stu-id="aa27d-117">After entangling these qubits, they are in the state:</span></span>

<span data-ttu-id="aa27d-118">$${1}\ket{\\phi^}= \frac {\sqrt{2}{00} }(\ket + \ket{11}) $$</span><span class="sxs-lookup"><span data-stu-id="aa27d-118">$$ \ket{\phi^+} = \frac{1}{\sqrt{2}}(\ket{00} + \ket{11}) $$</span></span>

### <a name="step-2-send-the-message"></a><span data-ttu-id="aa27d-119">Passo 2: Envie a mensagem</span><span class="sxs-lookup"><span data-stu-id="aa27d-119">Step 2: Send the message</span></span>
<span data-ttu-id="aa27d-120">Para enviar a __mensagem__ primeiro aplicamos um portão CNOT com o qubit de __mensagem__ e __aqui__ qubit como entradas (o qubit da __mensagem__ é o controle e o qubit __aqui__ é o qubit de destino, neste caso).</span><span class="sxs-lookup"><span data-stu-id="aa27d-120">To send the __message__ we first apply a CNOT gate with the __message__ qubit and __here__ qubit as inputs (the __message__ qubit being the control and the __here__ qubit being the target qubit, in this instance).</span></span> <span data-ttu-id="aa27d-121">Este estado de entrada pode ser escrito:</span><span class="sxs-lookup"><span data-stu-id="aa27d-121">This input state can be written:</span></span>

<span data-ttu-id="aa27d-122">$$ \ket{\psi}\ket{\phi^}={0} (\alfa\ket + \beta\ket{1})(\frac{1}{2}{\sqrt }(\ket{00} + \ket{11})) $$</span><span class="sxs-lookup"><span data-stu-id="aa27d-122">$$ \ket{\psi}\ket{\phi^+} = (\alpha\ket{0} + \beta\ket{1})(\frac{1}{\sqrt{2}}(\ket{00} + \ket{11})) $$</span></span>

<span data-ttu-id="aa27d-123">Isso se expande para:</span><span class="sxs-lookup"><span data-stu-id="aa27d-123">This expands to:</span></span>

<span data-ttu-id="aa27d-124">$$ \ket{\psi}\ket{\phi^}={2}\frac{\alpha}{\\sqrt{000} }\ket + \frac{\alpha}\\sqrt{2}}\ket{011} + \frac{\beta}{\sqrt{2}}\ket{100} + \frac{\beta}{\\\\\sqrt }\\\sqrt{2}}\ket{111} $$</span><span class="sxs-lookup"><span data-stu-id="aa27d-124">$$ \ket{\psi}\ket{\phi^+} = \frac{\alpha}{\sqrt{2}}\ket{000} + \frac{\alpha}{\sqrt{2}}\ket{011} + \frac{\beta}{\sqrt{2}}\ket{100} + \frac{\beta}{\sqrt{2}}\ket{111} $$</span></span>

<span data-ttu-id="aa27d-125">Como lembrete, o portão CNOT vira o qubit de destino quando o qubit de controle é 1.</span><span class="sxs-lookup"><span data-stu-id="aa27d-125">As a reminder, the CNOT gate flips the target qubit when the control qubit is 1.</span></span> <span data-ttu-id="aa27d-126">Assim, por exemplo, uma entrada{000}de $\ket $ não resultará em nenhuma alteração, pois o primeiro qubit (o controle) é 0.</span><span class="sxs-lookup"><span data-stu-id="aa27d-126">So for example, an input of $\ket{000}$ will result in no change as the first qubit (the control) is 0.</span></span> <span data-ttu-id="aa27d-127">No entanto, pegue um caso em que o primeiro qubit é 1 - por exemplo, uma entrada de $\ket{100}$.</span><span class="sxs-lookup"><span data-stu-id="aa27d-127">However, take a case where the first qubit is 1 - for example an input of $\ket{100}$.</span></span> <span data-ttu-id="aa27d-128">Neste caso, a saída é{110}$\ket $ como o segundo qubit (o alvo) é virado pelo portão CNOT.</span><span class="sxs-lookup"><span data-stu-id="aa27d-128">In this instance, the output is $\ket{110}$ as the second qubit (the target) is flipped by the CNOT gate.</span></span>

<span data-ttu-id="aa27d-129">Vamos agora considerar nossa saída uma vez que o portão CNOT tenha agido em nossa entrada acima.</span><span class="sxs-lookup"><span data-stu-id="aa27d-129">Let's now consider our output once the CNOT gate has acted on our input above.</span></span> <span data-ttu-id="aa27d-130">O resultado é:</span><span class="sxs-lookup"><span data-stu-id="aa27d-130">The result is:</span></span>

<span data-ttu-id="aa27d-131">{2}$$ \frac{\alpha}{\sqrt }\ket{000} + \frac{\alpha}\\sqrt{2}}\ket{011} + \frac{\beta}{\sqrt{2}}\ket{110} + \frac{\beta}\\sqrt{2}}\ket{101} $$</span><span class="sxs-lookup"><span data-stu-id="aa27d-131">$$ \frac{\alpha}{\sqrt{2}}\ket{000} + \frac{\alpha}{\sqrt{2}}\ket{011} + \frac{\beta}{\sqrt{2}}\ket{110} + \frac{\beta}{\sqrt{2}}\ket{101} $$</span></span>

<span data-ttu-id="aa27d-132">O próximo passo para enviar a __mensagem__ é aplicar um portão Hadamard ao qubit da __mensagem__ (esse é o primeiro qubit de cada termo).</span><span class="sxs-lookup"><span data-stu-id="aa27d-132">The next step to send the __message__ is to apply a Hadamard gate to the __message__ qubit (that's the first qubit of each term).</span></span> 

<span data-ttu-id="aa27d-133">Como lembrete, o portão Hadamard faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="aa27d-133">As a reminder, the Hadamard gate does the following:</span></span>

<span data-ttu-id="aa27d-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa27d-134">Input</span></span> | <span data-ttu-id="aa27d-135">Saída</span><span class="sxs-lookup"><span data-stu-id="aa27d-135">Output</span></span>
---------------------------| ---------------------------------------------------------------
<span data-ttu-id="aa27d-136">$\ket{0}$</span><span class="sxs-lookup"><span data-stu-id="aa27d-136">$\ket{0}$</span></span>  | <span data-ttu-id="aa27d-137">$\frac{1}{\sqrt{2}}(\ket{0} {1}+ \ket )$</span><span class="sxs-lookup"><span data-stu-id="aa27d-137">$\frac{1}{\sqrt{2}}(\ket{0} + \ket{1})$</span></span>
<span data-ttu-id="aa27d-138">$\ket{1}$</span><span class="sxs-lookup"><span data-stu-id="aa27d-138">$\ket{1}$</span></span>  | <span data-ttu-id="aa27d-139">$\frac{1}{\sqrt{2}}(\ket{0} {1}- \ket )$</span><span class="sxs-lookup"><span data-stu-id="aa27d-139">$\frac{1}{\sqrt{2}}(\ket{0} - \ket{1})$</span></span>

<span data-ttu-id="aa27d-140">Se aplicarmos o portão Hadamard ao primeiro qubit de cada termo de nossa produção acima, obtemos o seguinte resultado:</span><span class="sxs-lookup"><span data-stu-id="aa27d-140">If we apply the Hadamard gate to the first qubit of each term of our output above, we get the following result:</span></span>

<span data-ttu-id="aa27d-141">$$ \frac{\alpha}{\sqrt{2}}(\frac{1}{\sqrt{2}{0} }(\ket + \ket{1}))\ket{00} {2}+ \frac{\alfa}\\sqrt }(\frac{1}{\sqrt{11} {2}{1}{2}{0} {1}{10} {2}{1}{2}{0} {1}{01} {2}}(\ket{0} + \ket))\ket{1}+ \frac{\beta}{\\sqrt }(\frac {\sqrt }(\ket) \ket ))\ket + \frac{\beta}{\sqrt }(\frac {\sqrt }(\ket - \ket ))\ket $$</span><span class="sxs-lookup"><span data-stu-id="aa27d-141">$$ \frac{\alpha}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} + \ket{1}))\ket{00} + \frac{\alpha}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} + \ket{1}))\ket{11} + \frac{\beta}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} - \ket{1}))\ket{10} + \frac{\beta}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} - \ket{1}))\ket{01} $$</span></span>

<span data-ttu-id="aa27d-142">Observe que cada termo tem{1}dois fatores{2}$\frac {\sqrt }$$ .</span><span class="sxs-lookup"><span data-stu-id="aa27d-142">Note that each term has two $\frac{1}{\sqrt{2}}$ factors.</span></span> <span data-ttu-id="aa27d-143">Podemos multiplicar estes dando o seguinte resultado:</span><span class="sxs-lookup"><span data-stu-id="aa27d-143">We can multiply these out giving the following result:</span></span>

<span data-ttu-id="aa27d-144">$${2}\frac{\alfa} (\ket{0} {1}+ \ket )\ket{00} +{2}\frac{\alfa} (\ket{0} +{1}\ket )\ket{0} {1}{10} {2}{0} {1}{01} {11} + \frac{\beta}{2}(\ket - \ket )\ket + \frac{\beta} (\ket - \ket )\ket $$</span><span class="sxs-lookup"><span data-stu-id="aa27d-144">$$ \frac{\alpha}{2}(\ket{0} + \ket{1})\ket{00} + \frac{\alpha}{2}(\ket{0} + \ket{1})\ket{11} + \frac{\beta}{2}(\ket{0} - \ket{1})\ket{10} + \frac{\beta}{2}(\ket{0} - \ket{1})\ket{01} $$</span></span>

<span data-ttu-id="aa27d-145">O fator $\frac{1}{2}$ é comum a cada termo, então agora podemos levá-lo fora dos suportes:</span><span class="sxs-lookup"><span data-stu-id="aa27d-145">The  $\frac{1}{2}$ factor is common to each term so we can now take it outside the brackets:</span></span>

<span data-ttu-id="aa27d-146">{1}{2}$$ \frac \big[\alfa(\ket{0} {1}+ \ket )\ket{00} {0} + \alfa(\ket +{1}\ket{0} ){1}\ket{11} + \beta(\ket){1}\ket{10} + \beta(\ket-{0} \ket ) \ket \ket{01}\grande] $$</span><span class="sxs-lookup"><span data-stu-id="aa27d-146">$$ \frac{1}{2}\big[\alpha(\ket{0} + \ket{1})\ket{00} + \alpha(\ket{0} + \ket{1})\ket{11} + \beta(\ket{0} - \ket{1})\ket{10} + \beta(\ket{0} - \ket{1})\ket{01}\big] $$</span></span>

<span data-ttu-id="aa27d-147">Podemos então multiplicar os suportes para cada termo dando:</span><span class="sxs-lookup"><span data-stu-id="aa27d-147">We can then multiply out the brackets for each term giving:</span></span>

<span data-ttu-id="aa27d-148">$${1}{2}\frac \grande[\alfa\ket{000} +{100} \alfa\ket{011} + \alfa\ket +{111} \alfa\ket + \beta\ket{001} {101}{010} - \beta\ket{110} + \beta\ket - \beta\ket \grande] $$ $</span><span class="sxs-lookup"><span data-stu-id="aa27d-148">$$ \frac{1}{2}\big[\alpha\ket{000} + \alpha\ket{100} + \alpha\ket{011} + \alpha\ket{111} + \beta\ket{010} - \beta\ket{110} + \beta\ket{001} - \beta\ket{101}\big] $$</span></span>

### <a name="step-3-measure-the-result"></a><span data-ttu-id="aa27d-149">Passo 3: Meça o resultado</span><span class="sxs-lookup"><span data-stu-id="aa27d-149">Step 3: Measure the result</span></span>

<span data-ttu-id="aa27d-150">Devido a __aqui__ e __ali__ estar emaranhado, qualquer medida __aqui__ afetará o estado de __lá.__</span><span class="sxs-lookup"><span data-stu-id="aa27d-150">Due to __here__ and __there__ being entangled, any measurement on __here__ will affect the state of __there__.</span></span> <span data-ttu-id="aa27d-151">Se medirmos o primeiro e o segundo qubit __(mensagem__ e __aqui)__ podemos saber em que estado __há,__ devido a essa propriedade de emaranhamento.</span><span class="sxs-lookup"><span data-stu-id="aa27d-151">If we measure the first and second qubit (__message__ and __here__) we can learn what state __there__ is in, due to this property of entanglement.</span></span> 

* <span data-ttu-id="aa27d-152">Se medirmos e conseguirmos um resultado 00, a superposição entra em colapso, deixando apenas termos consistentes com este resultado.</span><span class="sxs-lookup"><span data-stu-id="aa27d-152">If we measure and get a result 00, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="aa27d-153">Isso é $\alpha\ket{000} +\beta\ket{001}$.</span><span class="sxs-lookup"><span data-stu-id="aa27d-153">That's $\alpha\ket{000} +\beta\ket{001}$.</span></span> <span data-ttu-id="aa27d-154">Isso pode ser refatorado{00}para $\ket (\alpha\ket{0} +\beta\ket{1})$.</span><span class="sxs-lookup"><span data-stu-id="aa27d-154">This can be refactored to $\ket{00}(\alpha\ket{0} +\beta\ket{1})$.</span></span> <span data-ttu-id="aa27d-155">Portanto, se medirmos o primeiro e o segundo qubit a ser 00, sabemos que o{0} terceiro qubit,{1} __lá,__ está no estado $(\alfa\ket +\beta\ket )$.</span><span class="sxs-lookup"><span data-stu-id="aa27d-155">Therefore if we measure the first and second qubit to be 00, we know that the third qubit, __there__, is in the state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>
* <span data-ttu-id="aa27d-156">Se medirmos e conseguirmos um resultado 01, a superposição entra em colapso, deixando apenas termos consistentes com este resultado.</span><span class="sxs-lookup"><span data-stu-id="aa27d-156">If we measure and get a result 01, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="aa27d-157">Isso é $\alpha\ket{011} +\beta\ket{010}$.</span><span class="sxs-lookup"><span data-stu-id="aa27d-157">That's $\alpha\ket{011} +\beta\ket{010}$.</span></span> <span data-ttu-id="aa27d-158">Isso pode ser refatorado{01}para $\ket (\alpha\ket{1} +\beta\ket{0})$.</span><span class="sxs-lookup"><span data-stu-id="aa27d-158">This can be refactored to $\ket{01}(\alpha\ket{1} +\beta\ket{0})$.</span></span> <span data-ttu-id="aa27d-159">Portanto, se medirmos o primeiro e segundo qubit a ser 01, sabemos que o terceiro{1} qubit, __lá,__ está no estado $(\alfa\ket +\beta\ket{0})$.</span><span class="sxs-lookup"><span data-stu-id="aa27d-159">Therefore if we measure the first and second qubit to be 01, we know that the third qubit, __there__, is in the state $(\alpha\ket{1} +\beta\ket{0})$.</span></span>
* <span data-ttu-id="aa27d-160">Se medirmos e conseguirmos um resultado 10, a superposição entra em colapso, deixando apenas termos consistentes com este resultado.</span><span class="sxs-lookup"><span data-stu-id="aa27d-160">If we measure and get a result 10, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="aa27d-161">Isso é $\alpha\ket{100} -\beta\ket{101}$.</span><span class="sxs-lookup"><span data-stu-id="aa27d-161">That's $\alpha\ket{100} -\beta\ket{101}$.</span></span> <span data-ttu-id="aa27d-162">Isso pode ser refatorado{10}para $\ket (\alfa\ket{0} -\beta\ket{1})$.</span><span class="sxs-lookup"><span data-stu-id="aa27d-162">This can be refactored to $\ket{10}(\alpha\ket{0} -\beta\ket{1})$.</span></span> <span data-ttu-id="aa27d-163">Portanto, se medirmos o primeiro e o segundo qubit para ser 10, sabemos que o{0} terceiro qubit,{1} __lá,__ está no estado $(\alfa\ket -\beta\ket )$.</span><span class="sxs-lookup"><span data-stu-id="aa27d-163">Therefore if we measure the first and second qubit to be 10, we know that the third qubit, __there__, is in the state $(\alpha\ket{0} -\beta\ket{1})$.</span></span>
* <span data-ttu-id="aa27d-164">Se medirmos e conseguirmos um resultado 11, a superposição entra em colapso, deixando apenas termos consistentes com este resultado.</span><span class="sxs-lookup"><span data-stu-id="aa27d-164">If we measure and get a result 11, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="aa27d-165">Isso é $\alpha\ket{111} -\beta\ket{110}$.</span><span class="sxs-lookup"><span data-stu-id="aa27d-165">That's $\alpha\ket{111} -\beta\ket{110}$.</span></span> <span data-ttu-id="aa27d-166">Isso pode ser refatorado{11}para $\ket (\alfa\ket{1} -\beta\ket{0})$.</span><span class="sxs-lookup"><span data-stu-id="aa27d-166">This can be refactored to $\ket{11}(\alpha\ket{1} -\beta\ket{0})$.</span></span> <span data-ttu-id="aa27d-167">Portanto, se medirmos o primeiro e o segundo qubit para ser 11, sabemos que o{1} terceiro qubit,{0} __lá,__ está no estado $(\alfa\ket -\beta\ket )$.</span><span class="sxs-lookup"><span data-stu-id="aa27d-167">Therefore if we measure the first and second qubit to be 11, we know that the third qubit, __there__, is in the state $(\alpha\ket{1} -\beta\ket{0})$.</span></span>

### <a name="step-4-interpret-the-result"></a><span data-ttu-id="aa27d-168">Passo 4: Interprete o resultado</span><span class="sxs-lookup"><span data-stu-id="aa27d-168">Step 4: Interpret the result</span></span>

<span data-ttu-id="aa27d-169">Como lembrete, a __mensagem__ original que queríamos enviar era:</span><span class="sxs-lookup"><span data-stu-id="aa27d-169">As a reminder, the original __message__ we wished to send was:</span></span>

<span data-ttu-id="aa27d-170">$$ \ket{\psi} = \alfa\ket{0} +{1} \beta\ket $$</span><span class="sxs-lookup"><span data-stu-id="aa27d-170">$$ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $$</span></span>

<span data-ttu-id="aa27d-171">Precisamos colocar o qubit __lá__ neste estado, para que o estado recebido seja o que se pretendia.</span><span class="sxs-lookup"><span data-stu-id="aa27d-171">We need to get the __there__ qubit into this state, so that the received state is the one that was intended.</span></span> 

* <span data-ttu-id="aa27d-172">Se medimos e obtivemos um resultado de 00, então o terceiro qubit,{0} __lá,__ está no estado $(\alfa\ket +\beta\ket{1})$.</span><span class="sxs-lookup"><span data-stu-id="aa27d-172">If we measured and got a result of 00, then the third qubit, __there__, is in the state $(\alpha\ket{0} +\beta\ket{1})$.</span></span> <span data-ttu-id="aa27d-173">Como esta é a __mensagem pretendida,__ nenhuma alteração é necessária.</span><span class="sxs-lookup"><span data-stu-id="aa27d-173">As this is the intended __message__, no alteration is required.</span></span>
* <span data-ttu-id="aa27d-174">Se medimos e obtivemos um resultado de 01, então o terceiro qubit,{1} __lá,__ está no estado $(\alfa\ket +\beta\ket{0})$.</span><span class="sxs-lookup"><span data-stu-id="aa27d-174">If we measured and got a result of 01, then the third qubit, __there__, is in the state $(\alpha\ket{1} +\beta\ket{0})$.</span></span> <span data-ttu-id="aa27d-175">Isso difere da __mensagem__pretendida, no entanto, aplicar um portão{0} NOT nos dá{1}o estado desejado $(\alpha\ket +\beta\ket )$.</span><span class="sxs-lookup"><span data-stu-id="aa27d-175">This differs from the intended __message__, however applying a NOT gate gives us the desired state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>
* <span data-ttu-id="aa27d-176">Se medimos e obtivemos um resultado de 10, então o terceiro qubit,{0} __lá,__ está no estado $(\alfa\ket -\beta\ket{1})$.</span><span class="sxs-lookup"><span data-stu-id="aa27d-176">If we measured and got a result of 10, then the third qubit, __there__, is in the state $(\alpha\ket{0} -\beta\ket{1})$.</span></span> <span data-ttu-id="aa27d-177">Isso difere da __mensagem__pretendida, no entanto, a aplicação de{0} um portão Z{1}nos dá o estado desejado $(\alpha\ket +\beta\ket )$.</span><span class="sxs-lookup"><span data-stu-id="aa27d-177">This differs from the intended __message__, however applying a Z gate gives us the desired state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>
* <span data-ttu-id="aa27d-178">Se medimos e obtivemos um resultado de 11, então o terceiro qubit,{1} __lá,__ está no estado $(\alfa\ket -\beta\ket{0})$.</span><span class="sxs-lookup"><span data-stu-id="aa27d-178">If we measured and got a result of 11, then the third qubit, __there__, is in the state $(\alpha\ket{1} -\beta\ket{0})$.</span></span> <span data-ttu-id="aa27d-179">Isso difere da __mensagem__pretendida, no entanto, aplicar um portão NOT seguido de{0} um portão{1}Z nos dá o estado desejado $(\alfa\ket +\beta\ket )$.</span><span class="sxs-lookup"><span data-stu-id="aa27d-179">This differs from the intended __message__, however applying a NOT gate followed by a Z gate gives us the desired state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>

<span data-ttu-id="aa27d-180">Resumindo, se medirmos e o primeiro qubit for 1, um portão Z é aplicado.</span><span class="sxs-lookup"><span data-stu-id="aa27d-180">To summarize, if we measure and the first qubit is 1, a Z gate is applied.</span></span> <span data-ttu-id="aa27d-181">Se medirmos e o segundo qubit for 1, um portão NOT será aplicado.</span><span class="sxs-lookup"><span data-stu-id="aa27d-181">If we measure and the second qubit is 1, a NOT gate is applied.</span></span>

### <a name="summary"></a><span data-ttu-id="aa27d-182">Resumo</span><span class="sxs-lookup"><span data-stu-id="aa27d-182">Summary</span></span>
<span data-ttu-id="aa27d-183">Mostrado abaixo é um circuito quântico de livro-texto que implementa o teletransporte.</span><span class="sxs-lookup"><span data-stu-id="aa27d-183">Shown below is a text-book quantum circuit that implements the teleportation.</span></span> <span data-ttu-id="aa27d-184">Movendo-se da esquerda para a direita você pode ver:</span><span class="sxs-lookup"><span data-stu-id="aa27d-184">Moving from left to right you can see:</span></span>
- <span data-ttu-id="aa27d-185">Passo 1: Enroscando __aqui__ e __ali__ aplicando um portão Hadamard e portão CNOT.</span><span class="sxs-lookup"><span data-stu-id="aa27d-185">Step 1: Entangling __here__ and __there__ by applying a Hadamard gate and CNOT gate.</span></span>
- <span data-ttu-id="aa27d-186">Passo 2: Enviar a __mensagem__ usando um portão CNOT e um portão Hadamard.</span><span class="sxs-lookup"><span data-stu-id="aa27d-186">Step 2: Sending the __message__ using a CNOT gate and a Hadamard gate.</span></span>
- <span data-ttu-id="aa27d-187">Passo 3: Fazer uma medição do primeiro e segundo qubits, __mensagem__ e __aqui__.</span><span class="sxs-lookup"><span data-stu-id="aa27d-187">Step 3: Taking a measurement of the first and second qubits, __message__ and __here__.</span></span>
- <span data-ttu-id="aa27d-188">Passo 4: Aplicando um portão NOT ou um portão Z, dependendo do resultado da medição na etapa 3.</span><span class="sxs-lookup"><span data-stu-id="aa27d-188">Step 4: Applying a NOT gate or a Z gate, depending on the result of the measurement in step 3.</span></span>

!['Teleporte(msg : Qubit, lá : Qubit) : Unidade'](~/media/teleportation.svg)

## <a name="quantum-teleportation-code"></a><span data-ttu-id="aa27d-190">Teletransporte Quântico: Código</span><span class="sxs-lookup"><span data-stu-id="aa27d-190">Quantum Teleportation: Code</span></span>

<span data-ttu-id="aa27d-191">Temos nosso circuito para teletransporte quântico:</span><span class="sxs-lookup"><span data-stu-id="aa27d-191">We have our circuit for quantum teleportation:</span></span>

!['Teleporte(msg : Qubit, lá : Qubit) : Unidade'](~/media/teleportation.svg)

<span data-ttu-id="aa27d-193">Agora podemos traduzir cada um dos passos deste circuito quântico em Q#.</span><span class="sxs-lookup"><span data-stu-id="aa27d-193">We can now translate each of the steps in this quantum circuit into Q#.</span></span>

### <a name="step-0-definition"></a><span data-ttu-id="aa27d-194">Passo 0: Definição</span><span class="sxs-lookup"><span data-stu-id="aa27d-194">Step 0: Definition</span></span>
<span data-ttu-id="aa27d-195">Quando realizamos o teletransporte, devemos saber a __mensagem__ que desejamos enviar, e para onde desejamos enviá-la __(lá).__</span><span class="sxs-lookup"><span data-stu-id="aa27d-195">When we perform teleportation, we must know the __message__ we wish to send, and where we wish to send it (__there__).</span></span> <span data-ttu-id="aa27d-196">Por essa razão, começamos definindo uma nova operação de Teleporte `msg` que `there`recebe dois qubits como argumentos, e :</span><span class="sxs-lookup"><span data-stu-id="aa27d-196">For this reason, we begin by defining a new Teleport operation that is given two qubits as arguments, `msg` and `there`:</span></span>

```qsharp
operation Teleport(msg : Qubit, there : Qubit) : Unit {
```

<span data-ttu-id="aa27d-197">Também precisamos alocar um `here` qubit que `using` oalcancemos com um bloco:</span><span class="sxs-lookup"><span data-stu-id="aa27d-197">We also need to allocate a qubit `here` which we achieve with a `using` block:</span></span>

```qsharp
    using (here = Qubit()) {
```

### <a name="step-1-create-an-entangled-state"></a><span data-ttu-id="aa27d-198">Passo 1: Criar um estado emaranhado</span><span class="sxs-lookup"><span data-stu-id="aa27d-198">Step 1: Create an entangled state</span></span>
<span data-ttu-id="aa27d-199">Podemos então criar o par `here` `there` emaranhado entre @"microsoft.quantum.intrinsic.h" @"microsoft.quantum.intrinsic.cnot" e usando as operações e:</span><span class="sxs-lookup"><span data-stu-id="aa27d-199">We can then create the entangled pair between `here` and `there` by using the @"microsoft.quantum.intrinsic.h" and @"microsoft.quantum.intrinsic.cnot" operations:</span></span>

```qsharp
        H(here);
        CNOT(here, there);
```

### <a name="step-2-send-the-message"></a><span data-ttu-id="aa27d-200">Passo 2: Envie a mensagem</span><span class="sxs-lookup"><span data-stu-id="aa27d-200">Step 2: Send the message</span></span>
<span data-ttu-id="aa27d-201">Em seguida, usamos os próximos $\operatorname{CNOT}$ e $H$ gates para mover nosso qubit de mensagem:</span><span class="sxs-lookup"><span data-stu-id="aa27d-201">We then use the next $\operatorname{CNOT}$ and $H$ gates to move our message qubit:</span></span>

```qsharp
        CNOT(msg, here);
        H(msg);
```

### <a name="step-3--4-measuring-and-interpreting-the-result"></a><span data-ttu-id="aa27d-202">Passo 3 & 4: Medir e interpretar o resultado</span><span class="sxs-lookup"><span data-stu-id="aa27d-202">Step 3 & 4: Measuring and interpreting the result</span></span>
<span data-ttu-id="aa27d-203">Por fim, @"microsoft.quantum.intrinsic.m" utilizamos para realizar as medições e realizar as operações `if` de portão necessárias para obter o estado desejado, conforme denotado pelas declarações:</span><span class="sxs-lookup"><span data-stu-id="aa27d-203">Finally, we use @"microsoft.quantum.intrinsic.m" to perform the measurements and perform the necessary gate operations to get the desired state, as denoted by `if` statements:</span></span>

```qsharp
        // Measure out the entanglement
        if (M(msg) == One)  { Z(there); }
        if (M(here) == One) { X(there); }
```

### <a name="step-5-restarting-the-qubit-register"></a><span data-ttu-id="aa27d-204">Passo 5: Reiniciar o registro de qubit</span><span class="sxs-lookup"><span data-stu-id="aa27d-204">Step 5: Restarting the qubit register</span></span>

<span data-ttu-id="aa27d-205">No final de cada operação Q# precisamos deixar os qubits{0}no estado $\ket $.</span><span class="sxs-lookup"><span data-stu-id="aa27d-205">At the end of every Q# operation we need to let the qubits in the state $\ket{0}$.</span></span> <span data-ttu-id="aa27d-206">Podemos usar @"microsoft.quantum.intrinsic.reset" para reiniciar todos os qubits para o estado zero e isso vai terminar nossa operação.</span><span class="sxs-lookup"><span data-stu-id="aa27d-206">We can use @"microsoft.quantum.intrinsic.reset" to restart all the qubits to the zero state and this will finish our operation.</span></span>

```qsharp
        Reset(msg);
        Reset(here);
        Reset(there);
    }
}
```


