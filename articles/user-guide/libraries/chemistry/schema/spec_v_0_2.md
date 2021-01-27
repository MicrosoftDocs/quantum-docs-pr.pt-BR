---
title: Especificação de esquema Broombridge (ver 0,2)
description: Detalha as especificações do esquema Broombridge quantum química v 0.2 para a biblioteca do Microsoft quantum química.
author: guanghaolow
ms.author: gulow
ms.date: 05/28/2019
ms.topic: conceptual
uid: microsoft.quantum.libraries.chemistry.schema.spec_v_0_2
no-loc:
- Q#
- $$v
ms.openlocfilehash: 8d26b56d88f365144510692466bfffc7feb71d88
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854057"
---
# <a name="broombridge-specification-v02"></a><span data-ttu-id="f12b3-103">Especificação Broombridge v 0.2</span><span class="sxs-lookup"><span data-stu-id="f12b3-103">Broombridge Specification v0.2</span></span> #

<span data-ttu-id="f12b3-104">As palavras-chave "deve", "não deve", "REQUIRED", "is", "maio" e "OPTIONAL" neste documento devem ser interpretadas conforme descrito em [RFC 2119](https://tools.ietf.org/html/rfc2119)(recomendável), "pode" e "opcional" neste documentos.</span><span class="sxs-lookup"><span data-stu-id="f12b3-104">The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](https://tools.ietf.org/html/rfc2119).</span></span>

<span data-ttu-id="f12b3-105">Qualquer barra lateral com os títulos "observação", "informações" ou "aviso" é informativa.</span><span class="sxs-lookup"><span data-stu-id="f12b3-105">Any sidebar with the headings "NOTE," "INFORMATION," or "WARNING" is informative.</span></span>

## <a name="introduction"></a><span data-ttu-id="f12b3-106">Introdução</span><span class="sxs-lookup"><span data-stu-id="f12b3-106">Introduction</span></span> ##

<span data-ttu-id="f12b3-107">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="f12b3-107">This section is informative.</span></span>

<span data-ttu-id="f12b3-108">Os documentos do Broombridge destinam-se a comunicar instâncias de problemas de simulação na química do Quantum para processamento usando simulação de Quantum e programação cadeias.</span><span class="sxs-lookup"><span data-stu-id="f12b3-108">Broombridge documents are intended to communicate instances of simulation problems in quantum chemistry for processing using quantum simulation and programming toolchains.</span></span>

## <a name="serialization"></a><span data-ttu-id="f12b3-109">Serialização</span><span class="sxs-lookup"><span data-stu-id="f12b3-109">Serialization</span></span> ##

<span data-ttu-id="f12b3-110">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="f12b3-110">This section is normative.</span></span>

<span data-ttu-id="f12b3-111">Um documento Broombridge deve ser serializado como um [documento YAML 1,2](http://yaml.org/spec/) que representa um objeto JSON, conforme descrito em [RFC 4627](https://tools.ietf.org/html/rfc4627) seção 2,2.</span><span class="sxs-lookup"><span data-stu-id="f12b3-111">A Broombridge document MUST be serialized as a [YAML 1.2 document](http://yaml.org/spec/) representing a JSON object as described in [RFC 4627](https://tools.ietf.org/html/rfc4627) section 2.2.</span></span>
<span data-ttu-id="f12b3-112">O objeto serializado para YAML deve ter uma propriedade `"$schema"` cujo valor é `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.2.schema.json"` e deve ser válido de acordo com as especificações do rascunho do esquema JSON-06 [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)].</span><span class="sxs-lookup"><span data-stu-id="f12b3-112">The object serialized to YAML MUST have a property `"$schema"` whose value is `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.2.schema.json"`, and MUST be valid according to the JSON Schema draft-06 specifications [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)].</span></span>

<span data-ttu-id="f12b3-113">Para o restante desta especificação, "o objeto Broombridge" fará referência ao objeto JSON desserializado de um documento Broombridge YAML.</span><span class="sxs-lookup"><span data-stu-id="f12b3-113">For the remainder of this specification, "the Broombridge object" will refer to the JSON object deserialized from a Broombridge YAML document.</span></span>

<span data-ttu-id="f12b3-114">A menos que indicado de outra forma explicitamente, os objetos não devem ter propriedades adicionais além daquelas especificadas explicitamente neste documento.</span><span class="sxs-lookup"><span data-stu-id="f12b3-114">Unless otherwise explicitly noted, objects MUST NOT have additional properties beyond those specified explicitly in this document.</span></span>

## <a name="additional-definitions"></a><span data-ttu-id="f12b3-115">Definições adicionais</span><span class="sxs-lookup"><span data-stu-id="f12b3-115">Additional Definitions</span></span> ##

<span data-ttu-id="f12b3-116">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="f12b3-116">This section is normative.</span></span>

### <a name="quantity-objects"></a><span data-ttu-id="f12b3-117">Quantidade de objetos</span><span class="sxs-lookup"><span data-stu-id="f12b3-117">Quantity Objects</span></span> ###

<span data-ttu-id="f12b3-118">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="f12b3-118">This section is normative.</span></span>

<span data-ttu-id="f12b3-119">Um _objeto Quantity_ é um objeto JSON e deve ter uma propriedade `units` cujo valor seja um dos valores permitidos listados na tabela 1.</span><span class="sxs-lookup"><span data-stu-id="f12b3-119">A _quantity object_ is a JSON object, and MUST have a property `units` whose value is one of the allowed values listed in Table 1.</span></span>

<span data-ttu-id="f12b3-120">Um objeto de quantidade é um _objeto de quantidade simples_ se tiver uma única propriedade, `value` além de sua `units` propriedade.</span><span class="sxs-lookup"><span data-stu-id="f12b3-120">A quantity object is a _simple quantity object_ if it has a single property `value` in addition to its `units` property.</span></span>
<span data-ttu-id="f12b3-121">O valor da `value` propriedade deve ser um número.</span><span class="sxs-lookup"><span data-stu-id="f12b3-121">The value of the `value` property MUST be a number.</span></span>

<span data-ttu-id="f12b3-122">Um objeto Quantity é um _objeto de quantidade vinculada_ se ele tiver as propriedades `lower` e, `upper` além de sua `units` propriedade.</span><span class="sxs-lookup"><span data-stu-id="f12b3-122">A quantity object is a _bounded quantity object_ if it has the properties `lower` and `upper` in addition to its `units` property.</span></span>
<span data-ttu-id="f12b3-123">Os valores das `lower` Propriedades e `upper` devem ser números.</span><span class="sxs-lookup"><span data-stu-id="f12b3-123">The values of the `lower` and `upper` properties MUST be numbers.</span></span>
<span data-ttu-id="f12b3-124">Um objeto de quantidade associada pode ter uma propriedade `value` cujo valor é um número.</span><span class="sxs-lookup"><span data-stu-id="f12b3-124">A bounded quantity object MAY have a property `value` whose value is a number.</span></span>

<span data-ttu-id="f12b3-125">Um objeto de quantidade é um _objeto de quantidade de matriz esparsa_ se ele tiver a propriedade `format` e uma propriedade além de `values` sua `units` propriedade.</span><span class="sxs-lookup"><span data-stu-id="f12b3-125">A quantity object is a _sparse array quantity object_ if it has the property `format` and a property `values` in addition to its `units` property.</span></span>
<span data-ttu-id="f12b3-126">O valor de `format` deve ser a cadeia de caracteres `sparse` .</span><span class="sxs-lookup"><span data-stu-id="f12b3-126">The value of `format` MUST be the string `sparse`.</span></span>
<span data-ttu-id="f12b3-127">O valor da `values` propriedade deve ser uma matriz.</span><span class="sxs-lookup"><span data-stu-id="f12b3-127">The value of the `values` property MUST be an array.</span></span>
<span data-ttu-id="f12b3-128">Cada elemento de `values` deve ser uma matriz que representa os índices e o valor da quantidade de matriz esparsa.</span><span class="sxs-lookup"><span data-stu-id="f12b3-128">Each element of `values` MUST be an array representing the indices and value of the sparse array quantity.</span></span>

<span data-ttu-id="f12b3-129">Os índices para cada elemento de um objeto de quantidade de matriz esparsa devem ser exclusivos em todo o objeto de quantidade de matriz esparsa.</span><span class="sxs-lookup"><span data-stu-id="f12b3-129">The indices for each element of a sparse array quantity object MUST be unique across the entire sparse array quantity object.</span></span>
<span data-ttu-id="f12b3-130">Se um índice estiver presente com um valor de `0` , um analisador deve tratar o objeto de quantidade de matriz esparsa de forma idêntica a um objeto de quantidade de matriz esparsa no qual esse índice não está presente.</span><span class="sxs-lookup"><span data-stu-id="f12b3-130">If an index is present with a value of `0`, a parser MUST treat the sparse array quantity object identically to a sparse array quantity object in which that index is not present at all.</span></span>


<span data-ttu-id="f12b3-131">Um objeto de quantidade deve ser</span><span class="sxs-lookup"><span data-stu-id="f12b3-131">A quantity object MUST either be</span></span>

- <span data-ttu-id="f12b3-132">um objeto de quantidade simples,</span><span class="sxs-lookup"><span data-stu-id="f12b3-132">a simple quantity object,</span></span>
- <span data-ttu-id="f12b3-133">um objeto de quantidade vinculada ou</span><span class="sxs-lookup"><span data-stu-id="f12b3-133">a bounded quantity object, or</span></span>
- <span data-ttu-id="f12b3-134">um objeto de quantidade de matriz esparsa.</span><span class="sxs-lookup"><span data-stu-id="f12b3-134">a sparse array quantity object.</span></span>


### <a name="examples"></a><span data-ttu-id="f12b3-135">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f12b3-135">Examples</span></span> ###

<span data-ttu-id="f12b3-136">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="f12b3-136">This section is informative.</span></span>

<span data-ttu-id="f12b3-137">Uma quantidade simples representando $1.9844146837 \, \mathrm{ha} $:</span><span class="sxs-lookup"><span data-stu-id="f12b3-137">A simple quantity representing $1.9844146837\,\mathrm{Ha}$:</span></span>

```yaml
coulomb_repulsion:
    value: 1.9844146837
    units: hartree
```

<span data-ttu-id="f12b3-138">Uma quantidade limitada que representa uma distribuição uniforme sobre o intervalo $ [-7,-6] \, \mathrm{ha} $:</span><span class="sxs-lookup"><span data-stu-id="f12b3-138">A bounded quantity representing a uniform distribution over the interval $[-7, -6]\,\mathrm{Ha}$:</span></span>

```yaml
fci_energy:
    upper: -6
    lower: -7
    units: hartree
```

<span data-ttu-id="f12b3-139">A seguir está uma quantidade de matriz esparsa com um elemento `[1, 2]` igual a `hello` e um elemento `[3, 4]` igual a `world` :</span><span class="sxs-lookup"><span data-stu-id="f12b3-139">The following is a sparse array quantity with an element `[1, 2]` equal to `hello` and an element `[3, 4]` equal to `world`:</span></span>

```yaml
sparse_example:
    format: sparse
    units: hartree
    values:
    - [1, 2, "hello"]
    - [3, 4, "world"]
```

## <a name="format-section"></a><span data-ttu-id="f12b3-140">Seção de formato</span><span class="sxs-lookup"><span data-stu-id="f12b3-140">Format Section</span></span> ##

<span data-ttu-id="f12b3-141">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="f12b3-141">This section is normative.</span></span>

<span data-ttu-id="f12b3-142">O objeto Broombridge deve ter uma propriedade `format` cujo valor é um objeto JSON com uma propriedade chamada `version` .</span><span class="sxs-lookup"><span data-stu-id="f12b3-142">The Broombridge object MUST have a property `format` whose value is a JSON object with one property called `version`.</span></span>
<span data-ttu-id="f12b3-143">A `version` propriedade deve ter o valor `"0.2"` .</span><span class="sxs-lookup"><span data-stu-id="f12b3-143">The `version` property MUST have the value `"0.2"`.</span></span>

### <a name="example"></a><span data-ttu-id="f12b3-144">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f12b3-144">Example</span></span> ###

<span data-ttu-id="f12b3-145">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="f12b3-145">This section is informative.</span></span>

```yaml
format:                        # required
    version: "0.2"             # must match exactly
```

## <a name="problem-description-section"></a><span data-ttu-id="f12b3-146">Seção Descrição do problema</span><span class="sxs-lookup"><span data-stu-id="f12b3-146">Problem Description Section</span></span> ##

<span data-ttu-id="f12b3-147">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="f12b3-147">This section is normative.</span></span>

<span data-ttu-id="f12b3-148">O objeto Broombridge deve ter uma propriedade `problem_description` cujo valor é uma matriz JSON.</span><span class="sxs-lookup"><span data-stu-id="f12b3-148">The Broombridge object MUST have a property `problem_description` whose value is a JSON array.</span></span>
<span data-ttu-id="f12b3-149">Cada item no valor da `problem_description` propriedade deve ser um objeto JSON que descreve um conjunto de integrais, conforme descrito no restante desta seção.</span><span class="sxs-lookup"><span data-stu-id="f12b3-149">Each item in the value of the `problem_description` property MUST be a JSON object describing one set of integrals, as described in the remainder of this section.</span></span>
<span data-ttu-id="f12b3-150">No restante desta seção, o termo "objeto de descrição do problema" fará referência a um item no valor da `problem_description` Propriedade do objeto Broombridge.</span><span class="sxs-lookup"><span data-stu-id="f12b3-150">In the remainder of this section, the term "problem description object" will refer to an item in the value of the `problem_description` property of the Broombridge object.</span></span>

<span data-ttu-id="f12b3-151">Cada objeto de descrição do problema deve ter uma propriedade `metadata` cujo valor é um objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="f12b3-151">Each problem description object MUST have a property `metadata` whose value is a JSON object.</span></span>
<span data-ttu-id="f12b3-152">O valor de `metadata` pode ser o objeto JSON vazio (ou seja, `{}` ) ou pode conter propriedades adicionais definidas pelo implementador.</span><span class="sxs-lookup"><span data-stu-id="f12b3-152">The value of `metadata` MAY be the empty JSON object (that is, `{}`), or MAY contain additional properties defined by the implementor.</span></span>

### <a name="hamiltonian-section"></a><span data-ttu-id="f12b3-153">Seção Hamiltonian</span><span class="sxs-lookup"><span data-stu-id="f12b3-153">Hamiltonian Section</span></span> ###

#### <a name="overview"></a><span data-ttu-id="f12b3-154">Visão geral</span><span class="sxs-lookup"><span data-stu-id="f12b3-154">Overview</span></span> ####

<span data-ttu-id="f12b3-155">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="f12b3-155">This section is informative.</span></span>

<span data-ttu-id="f12b3-156">A `hamiltonian` propriedade de cada objeto de descrição do problema descreve o Hamiltonian para um problema de química do Quantum específico, listando seus termos de um e dois corpo como matrizes esparsas de números reais.</span><span class="sxs-lookup"><span data-stu-id="f12b3-156">The `hamiltonian` property of each problem description object describes the Hamiltonian for a particular quantum chemistry problem by listing out its one- and two-body terms as sparse arrays of real numbers.</span></span>
<span data-ttu-id="f12b3-157">Os operadores de Hamiltonian descritos por cada objeto de descrição de problema assumem o formulário</span><span class="sxs-lookup"><span data-stu-id="f12b3-157">The Hamiltonian operators described by each problem description object take the form</span></span>

<span data-ttu-id="f12b3-158">$ $ H = \sum \_ \{ i, j \} \sum \_ {\sigma\in \\ {\uparrow, \downarrow \\ }} H \_ \{ IJ \} a ^ \{ \dagger \} \_ {i, \sigma} a \_ {j, \sigma} + \frac {1} {2} \sum \_ \{ i, j, k, l \} \sum \_ {\sigma, \rho\in \\ {\uparrow, \downarrow \\ }} H \_ {ijkl} a ^ \dagger \_ {i, \sigma} a ^ \dagger \_ {k, \rho} a \_ {l, \rho} a \_ {j, \sigma}, $ $</span><span class="sxs-lookup"><span data-stu-id="f12b3-158">$$ H = \sum\_\{i,j\}\sum\_{\sigma\in\\{\uparrow,\downarrow\\}} h\_\{ij\} a^\{\dagger\}\_{i,\sigma} a\_{j,\sigma} + \frac{1}{2}\sum\_\{i,j,k,l\}\sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}} h\_{ijkl} a^\dagger\_{i,\sigma} a^\dagger\_{k,\rho} a\_{l,\rho} a\_{j,\sigma}, $$</span></span>

<span data-ttu-id="f12b3-159">Aqui $h _ {ijkl} = (IJ | KL) $ na Convenção Mulliken.</span><span class="sxs-lookup"><span data-stu-id="f12b3-159">here $h_{ijkl}= (ij|kl)$ in Mulliken convention.</span></span>

<span data-ttu-id="f12b3-160">Para maior clareza, o termo One-at é</span><span class="sxs-lookup"><span data-stu-id="f12b3-160">For clarity, the one-electron term is</span></span>

<span data-ttu-id="f12b3-161">$ $ h_ {IJ} = \int {\mathrm d} x \psi ^ \* \_ i (x) \left (\frac {1} {2} \nabla ^ 2 + \sum \_ {A} \frac{Z \_ a} {| x-x \_ a |}  \right) \psi \_ j (x), $ $</span><span class="sxs-lookup"><span data-stu-id="f12b3-161">$$ h_{ij} = \int {\mathrm d}x \psi^\*\_i(x) \left(\frac{1}{2}\nabla^2 + \sum\_{A}\frac{Z\_A}{|x-x\_A|}  \right) \psi\_j(x), $$</span></span>

<span data-ttu-id="f12b3-162">e o termo de duas-bits é</span><span class="sxs-lookup"><span data-stu-id="f12b3-162">and the two-electron term is</span></span>

<span data-ttu-id="f12b3-163">$ $ h \_ \{ ijkl \} = \iint \{ \mathrm d \} x ^ 2 \psi ^ \{ \* \} \_ i (x \_ 1) \psi \_ j (x \_ 1) \frac \{ 1 \} \{ \| x \_ 1-x \_ 2 \| \} \psi \_ k ^ \{ \* \} (x \_ 2) \psi \_ l (x \_ 2).</span><span class="sxs-lookup"><span data-stu-id="f12b3-163">$$ h\_\{ijkl\} = \iint \{\mathrm d\}x^2 \psi^\{\*\}\_i(x\_1)\psi\_j(x\_1) \frac\{1\}\{\|x\_1 -x\_2\|\}\psi\_k^\{\*\}(x\_2) \psi\_l(x\_2).</span></span>
$$

<span data-ttu-id="f12b3-164">Conforme observado em nossa descrição da [ `basis_set` Propriedade](#basis-set-object) de cada elemento da `integral_sets` propriedade, supomos que as funções de base usadas sejam de valor real.</span><span class="sxs-lookup"><span data-stu-id="f12b3-164">As noted in our description of the [`basis_set` property](#basis-set-object) of each element of the `integral_sets` property, we further explicitly assume that the basis functions used are real-valued.</span></span>
<span data-ttu-id="f12b3-165">Isso nos permite usar os seguintes Symmetries entre os termos para compactar a representação do Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="f12b3-165">This allows us to use the following symmetries between the terms to compress the representation of the Hamiltonian.</span></span>

<span data-ttu-id="f12b3-166">$ $ h_ {ijkl} = h_ {Ijlk} = h_ {jikl} = h_ {jilk} = h_ {klij} = h_ {klji} = h_ {lkij} = h_ {LKJI}.</span><span class="sxs-lookup"><span data-stu-id="f12b3-166">$$ h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkij}=h_{lkji}.</span></span>
$$


#### <a name="contents"></a><span data-ttu-id="f12b3-167">Sumário</span><span class="sxs-lookup"><span data-stu-id="f12b3-167">Contents</span></span> ####

<span data-ttu-id="f12b3-168">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="f12b3-168">This section is normative.</span></span>

<span data-ttu-id="f12b3-169">Cada objeto de descrição do problema deve ter uma propriedade `hamiltonian` cujo valor é um objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="f12b3-169">Each problem description object MUST have a property `hamiltonian` whose value is a JSON object.</span></span>
<span data-ttu-id="f12b3-170">O valor da `hamiltonian` propriedade é conhecido como um objeto Hamiltonian e deve ter as propriedades e, `one_electron_integrals` `two_electron_integrals` conforme descrito no restante desta seção.</span><span class="sxs-lookup"><span data-stu-id="f12b3-170">The value of the `hamiltonian` property is known as a Hamiltonian object, and MUST have the properties `one_electron_integrals` and `two_electron_integrals` as described in the remainder of this section.</span></span>

<span data-ttu-id="f12b3-171">Cada objeto de descrição do problema deve ter uma propriedade `coulomb_repulsion` cujo valor é um objeto de quantidade simples.</span><span class="sxs-lookup"><span data-stu-id="f12b3-171">Each problem description object MUST have a property `coulomb_repulsion` whose value is a simple quantity object.</span></span>
<span data-ttu-id="f12b3-172">Cada objeto de descrição do problema deve ter uma propriedade `energy_offet` cujo valor é um objeto de quantidade simples.</span><span class="sxs-lookup"><span data-stu-id="f12b3-172">Each problem description object MUST have a property `energy_offet` whose value is a simple quantity object.</span></span>
> <span data-ttu-id="f12b3-173">ANOTAÇÕES Os valores de `coulomb_repulsion` e `energy_offet` adicionados em conjunto capturam o termo de identidade do Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="f12b3-173">[NOTE] The values of `coulomb_repulsion` and `energy_offet` added together capture the identity term of the Hamiltonian.</span></span>

##### <a name="one-electron-integrals-object"></a><span data-ttu-id="f12b3-174">Objeto de One-Electron integrais</span><span class="sxs-lookup"><span data-stu-id="f12b3-174">One-Electron Integrals Object</span></span> #####

<span data-ttu-id="f12b3-175">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="f12b3-175">This section is normative.</span></span>

<span data-ttu-id="f12b3-176">A `one_electron_integrals` Propriedade do objeto HAMILTONIAN deve ser uma quantidade de matriz esparsa cujos índices são dois inteiros e cujos valores são números.</span><span class="sxs-lookup"><span data-stu-id="f12b3-176">The `one_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity whose indices are two integers and whose values are numbers.</span></span>
<span data-ttu-id="f12b3-177">Cada termo deve ter índices `[i, j]` onde `i >= j` .</span><span class="sxs-lookup"><span data-stu-id="f12b3-177">Every term MUST have indices `[i, j]` where `i >= j`.</span></span>

> <span data-ttu-id="f12b3-178">ANOTAÇÕES Isso reflete a simetria de que $h _ {IJ} = h_ {ji} $, que é uma conseqüência do fato de que o Hamiltonian é Hermitian.</span><span class="sxs-lookup"><span data-stu-id="f12b3-178">[NOTE] This reflects the symmetry that $h_{ij} = h_{ji}$ which is a consequence of the fact that the Hamiltonian is Hermitian.</span></span>


###### <a name="example"></a><span data-ttu-id="f12b3-179">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f12b3-179">Example</span></span> ######

<span data-ttu-id="f12b3-180">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="f12b3-180">This section is informative.</span></span>

<span data-ttu-id="f12b3-181">A quantidade de matriz esparsa a seguir representa o Hamiltonian $ $ H = \left (-5,0 (a ^ \{ \dagger \} \_ {1, \uparrow} a \_ {1, \uparrow} + a ^ \{ \dagger \} \_ {1, \downarrow} a \_ {1, \downarrow}) + 0,17 (a ^ \{ \dagger \} \_ {2, \uparrow} a \_ {1, \uparrow} + a ^ \{ \dagger \} \_ {1, \uparrow} a \_ {2, \uparrow} + a ^ \{ \dagger \} \_ {2, \downarrow} a \_ {1, \downarrow} + a ^ \{ \dagger \} \_ {1, \downarrow} a \_ {2, \downarrow}) \right) \\ , \mathrm{ha}.</span><span class="sxs-lookup"><span data-stu-id="f12b3-181">The following sparse array quantity represents the Hamiltonian $$ H = \left(-5.0  (a^\{\dagger\}\_{1,\uparrow} a\_{1,\uparrow}+a^\{\dagger\}\_{1,\downarrow} a\_{1,\downarrow})+ 0.17 (a^\{\dagger\}\_{2,\uparrow} a\_{1,\uparrow}+ a^\{\dagger\}\_{1,\uparrow} a\_{2,\uparrow}+a^\{\dagger\}\_{2,\downarrow} a\_{1,\downarrow}+ a^\{\dagger\}\_{1,\downarrow} a\_{2,\downarrow})\right)\\,\mathrm{Ha}.</span></span>
$$

```yaml
one_electron_integrals:     # required
    units: hartree          # required
    format: sparse          # required
    values:                 # required
        # i j f(i,j)
        - [1, 1, -5.0]
        - [2, 1,  0.17]
```
> [!NOTE]
> <span data-ttu-id="f12b3-182">Broombridge usa indexação com base em 1.</span><span class="sxs-lookup"><span data-stu-id="f12b3-182">Broombridge uses 1-based indexing.</span></span>


##### <a name="two-electron-integrals-object"></a><span data-ttu-id="f12b3-183">Objeto de Two-Electron integrais</span><span class="sxs-lookup"><span data-stu-id="f12b3-183">Two-Electron Integrals Object</span></span> #####

<span data-ttu-id="f12b3-184">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="f12b3-184">This section is normative.</span></span>

<span data-ttu-id="f12b3-185">A `two_electron_integrals` Propriedade do objeto HAMILTONIAN deve ser uma quantidade de matriz esparsa com uma propriedade adicional chamada `index_convention` .</span><span class="sxs-lookup"><span data-stu-id="f12b3-185">The `two_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity with one additional property called `index_convention`.</span></span>
<span data-ttu-id="f12b3-186">Cada elemento do valor de `two_electron_integrals` deve ter quatro índices.</span><span class="sxs-lookup"><span data-stu-id="f12b3-186">Each element of the value of `two_electron_integrals` MUST have four indices.</span></span>

<span data-ttu-id="f12b3-187">Cada `two_electron_integrals` propriedade deve ter uma `index_convention` propriedade.</span><span class="sxs-lookup"><span data-stu-id="f12b3-187">Each `two_electron_integrals` property MUST have a `index_convention` property.</span></span>
<span data-ttu-id="f12b3-188">O valor da `index_convention` propriedade deve ser um dos valores permitidos listados na tabela 1.</span><span class="sxs-lookup"><span data-stu-id="f12b3-188">The value of the `index_convention` property MUST be one of the allowed values listed in Table 1.</span></span>
<span data-ttu-id="f12b3-189">Se o valor de `index_convention` for `mulliken` , para cada elemento da quantidade de `two_electron_integrals` matriz esparsa, um analisador que carrega um documento Broombridge deve criar uma instância de um termo Hamiltonian igual ao operador de dois bits $h _ {i, j, k, l} a ^ \ dagger_i um ^ \ dagger_j a_k A_L $, em que $i $, $j $, $k $ e $l $ devem ser inteiros de valor pelo menos 1 e em que $h _ {i, j, k, l} $ é o elemento `[i, j, k, l, h(i, j, k, l)]` da quantidade de matriz esparsa.</span><span class="sxs-lookup"><span data-stu-id="f12b3-189">If the value of `index_convention` is `mulliken`, then for each element of the `two_electron_integrals` sparse array quantity, a parser loading a Broombridge document MUST instantiate a Hamiltonian term equal to the two-electron operator $h_{i, j, k, l} a^\dagger_i a^\dagger_j a_k a_l$, where $i$, $j$, $k$, and $l$ MUST be integers of value at least 1, and where $h_{i, j, k, l}$ is the element `[i, j, k, l, h(i, j, k, l)]` of the sparse array quantity.</span></span>

###### <a name="symmetries"></a><span data-ttu-id="f12b3-190">Symmetries</span><span class="sxs-lookup"><span data-stu-id="f12b3-190">Symmetries</span></span> ######

<span data-ttu-id="f12b3-191">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="f12b3-191">This section is normative.</span></span>

<span data-ttu-id="f12b3-192">Se a `index_convention` propriedade de um `two_electron_integrals` objeto for igual a `mulliken` , se um elemento com índices `[i, j, k, l]` estiver presente, os seguintes índices não deverão estar presentes, a menos que sejam iguais a `[i, j, k, l]` :</span><span class="sxs-lookup"><span data-stu-id="f12b3-192">If the `index_convention` property of a `two_electron_integrals` object is equal to `mulliken`, then if an element with indices `[i, j, k, l]` is present, the following indices MUST NOT be present unless they are equal to `[i, j, k, l]`:</span></span>

- `[i, j, l, k]`
- `[j, i, k, l]`
- `[j, i, l, k]`
- `[k, l, i, j]`
- `[k, l, j, i]`
- `[l, k, j, i]`

> [!NOTE]
> <span data-ttu-id="f12b3-193">Como a `index_convention` propriedade é um objeto de quantidade esparsa, nenhum índice pode ser repetido em elementos diferentes.</span><span class="sxs-lookup"><span data-stu-id="f12b3-193">Because the `index_convention` property is a sparse quantity object, no indices may be repeated on different elements.</span></span>
> <span data-ttu-id="f12b3-194">Em particular, se um elemento com índices `[i, j, k, l]` estiver presente, nenhum outro elemento poderá ter esses índices.</span><span class="sxs-lookup"><span data-stu-id="f12b3-194">In particular, if an element with indices `[i, j, k, l]` is present, no other element may have those indices.</span></span>


<!-- h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkji}. -->

###### <a name="example"></a><span data-ttu-id="f12b3-195">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f12b3-195">Example</span></span> #######

<span data-ttu-id="f12b3-196">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="f12b3-196">This section is informative.</span></span>

<span data-ttu-id="f12b3-197">O objeto a seguir especifica o Hamiltonian</span><span class="sxs-lookup"><span data-stu-id="f12b3-197">The following object specifies the Hamiltonian</span></span>

<span data-ttu-id="f12b3-198">$ $ H = \frac12 \sum \_ {\sigma, \rho\in \\ {\uparrow, \downarrow \\ }} \Biggr (1,6 a ^ {\dagger} \_ {1, \sigma} a ^ {\dagger} \_ {1, \rho} a \_ {1, \rho} a \_ {1, \sigma}-0,1 a ^ {\dagger} \_ {6, \sigma} a ^ {\dagger} { \_ 1, \rho} a \_ {3, \rho} a \_ {2, \sigma}-0,1 a ^ {\dagger} \_ {6, \sigma} a ^ {\dagger} \_ {1, \rho} a \_ {2, \rho} a \_ {3, \sigma}-0,1 a ^ {\dagger} \_ {1, \sigma} a ^ {\dagger} \_ {6, \rho} a \_ {3, \rho} a \_ {2, \sigma}-0,1 a ^ {\dagger} \_ {1, \sigma} a ^ {\dagger} \_ {6, \rho} a \_ {2, \rho} a \_ {3, \sigma} $ $ $ $-0,1 a ^ {\dagger} \_ {3, \sigma} a ^ {\dagger} \_ {2, \rho} a \_ {6, \rho} a \_ {1, \sigma}-0,1 a ^ {\dagger} \_ {3, \sigma} a ^ {\dagger} \_ {2, \rho} a \_ {1, \rho} a \_ {6, \sigma}-0,1 a ^ {\dagger} \_ {2, \sigma} a ^ {\dagger} \_ {3 , \rho} a \_ {6, \rho} a \_ {1, \sigma}-0,1 a ^ {\dagger} \_ {2, \sigma} a ^ {\dagger} \_ {3, \rho} a \_ {1, \Rho} a \_ {6, \sigma}\Biggr) \\ , \textrm{ha}.</span><span class="sxs-lookup"><span data-stu-id="f12b3-198">$$ H = \frac12 \sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}}\Biggr( 1.6 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{1,\rho} a\_{1,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{2,\rho} a\_{3,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{2,\rho} a\_{3,\sigma} $$ $$- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{1,\rho} a\_{6,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{1,\rho} a\_{6,\sigma}\Biggr)\\,\textrm{Ha}.</span></span>
$$

```yaml
two_electron_integrals:
    index_convention: mulliken
    units: hartree
    format: sparse
    values:
        - [1, 1, 1, 1,  1.6]
        - [6, 1, 3, 2, -0.1]
```

### <a name="initial-state-section"></a><span data-ttu-id="f12b3-199">Seção de estado inicial</span><span class="sxs-lookup"><span data-stu-id="f12b3-199">Initial State Section</span></span> ###

<span data-ttu-id="f12b3-200">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="f12b3-200">This section is normative.</span></span>

<span data-ttu-id="f12b3-201">O `initial_state_suggestion` objeto cujo valor é uma matriz JSON especifica os Estados de Quantum inicial de interesse para o Hamiltonian especificado.</span><span class="sxs-lookup"><span data-stu-id="f12b3-201">The `initial_state_suggestion` object whose value is a JSON array specifies initial quantum states of interest to the specified Hamiltonian.</span></span> <span data-ttu-id="f12b3-202">Cada item no valor da `initial_state_suggestion` propriedade deve ser um objeto JSON que descreve um estado Quantum, conforme descrito no restante desta seção.</span><span class="sxs-lookup"><span data-stu-id="f12b3-202">Each item in the value of the `initial_state_suggestion` property MUST be a JSON object describing one quantum state, as described in the remainder of this section.</span></span>
<span data-ttu-id="f12b3-203">No restante desta seção, o termo "objeto de estado" fará referência a um item no valor da `initial_state_suggestion` Propriedade do objeto Broombridge.</span><span class="sxs-lookup"><span data-stu-id="f12b3-203">In the remainder of this section, the term "state object" will refer to an item in the value of the `initial_state_suggestion` property of the Broombridge object.</span></span>

#### <a name="state-object"></a><span data-ttu-id="f12b3-204">Objeto de estado</span><span class="sxs-lookup"><span data-stu-id="f12b3-204">State object</span></span> ####

<span data-ttu-id="f12b3-205">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="f12b3-205">This section is normative.</span></span>

<span data-ttu-id="f12b3-206">Cada objeto de Estado deve ter uma `label` propriedade que contém uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f12b3-206">Each state object MUST have a `label` property containing a string.</span></span> <span data-ttu-id="f12b3-207">Cada objeto de Estado deve ter uma `method` propriedade.</span><span class="sxs-lookup"><span data-stu-id="f12b3-207">Each state object MUST have a `method` property.</span></span> <span data-ttu-id="f12b3-208">O valor da `method` propriedade deve ser um dos valores permitidos listados na tabela 3.</span><span class="sxs-lookup"><span data-stu-id="f12b3-208">The value of the `method` property MUST be one of the allowed values listed in Table 3.</span></span>
<span data-ttu-id="f12b3-209">Cada objeto de estado pode ter uma propriedade `energy` cujo valor deve ser um objeto de quantidade simples.</span><span class="sxs-lookup"><span data-stu-id="f12b3-209">Each state object MAY have a property `energy` whose value MUST be a simple quantity object.</span></span>

<span data-ttu-id="f12b3-210">Se o valor da `method` propriedade for `sparse_multi_configurational` , o objeto de estado deverá ter uma `superposition` propriedade que contém uma matriz de Estados de base e suas amplitudes não normalizadas.</span><span class="sxs-lookup"><span data-stu-id="f12b3-210">If the value of the `method` property is `sparse_multi_configurational`, the state object MUST have a `superposition` property containing an array of basis states and their unnormalized amplitudes.</span></span>

<span data-ttu-id="f12b3-211">Por exemplo, os Estados iniciais $ $ \ket{G0} = \ket{G1} = \ket{G2} = (a ^ {\dagger} \_ {1, \uparrow}a ^ {\dagger} \_ {2, \uparrow}a ^ {\dagger} \_ {2, \downarrow}) \ket {0} $ $ $ $ \ket{E} = \frac{0.1 (a ^ {\dagger} \_ {1, \uparrow}a ^ {\dagger} \_ {2, \uparrow}a ^ {\dagger} \_ {2, \downarrow}) + 0.2 (um ^ {\dagger} \_ {1, \uparrow}a ^ {\dagger} \_ {3, \uparrow}a ^ {\dagger} \_ {2, \downarrow})} {\sqrt{| 0,1 | ^ 2 + | 0.2 | ^ 2}} \ket {0} , $ $, em que $ \ket{E} $ tem energia $0.987 \textrm{ha} $, são representados por</span><span class="sxs-lookup"><span data-stu-id="f12b3-211">For example, the initial states $$ \ket{G0}=\ket{G1}=\ket{G2}=(a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})\ket{0} $$ $$ \ket{E}=\frac{0.1 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})+0.2 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{3,\uparrow}a^{\dagger}\_{2,\downarrow})}{\sqrt{|0.1|^2+|0.2|^2}}\ket{0}, $$ where $\ket{E}$ has energy $0.987 \textrm{Ha}$, are represented by</span></span>
```yaml
initial_state_suggestions: # optional. If not provided, spin-orbitals will be filled to minimize one-body diagonal term energies.
  - label: "|G0>"
    method: sparse_multi_configurational
    superposition:
      - [1.0, "(1a)+","(2a)+","(2b)+","|vacuum>"]
  - label: "|G1>"
    method: sparse_multi_configurational
    superposition:
      - [-1.0, "(2a)+","(1a)+","(2b)+","|vacuum>"]
  - label: "|G2>"
    method: sparse_multi_configurational
    superposition:
      - [1.0, "(3a)","(1a)+","(2a)+","(3a)+","(2b)+","|vacuum>"]
  - label: "|E>"
    energy: {units: hartree, value: 0.987}
    method: sparse_multi_configurational
    superposition:
      - [0.1, "(1a)+","(2a)+","(2b)+","|vacuum>"]
      - [0.2, "(1a)+","(3a)+","(2b)+","|vacuum>"]
```

<span data-ttu-id="f12b3-212">Se o valor da `method` propriedade for `unitary_coupled_cluster` , o objeto de estado deverá ter uma `cluster_operator` propriedade cujo valor é um objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="f12b3-212">If the value of the `method` property is `unitary_coupled_cluster`, the state object MUST have a `cluster_operator` property whose value is a JSON object.</span></span>
<span data-ttu-id="f12b3-213">O objeto JSON deve ter uma `reference_state` propriedade cujo valor é um estado base.</span><span class="sxs-lookup"><span data-stu-id="f12b3-213">The JSON object MUST have a `reference_state` property whose value is a basis state.</span></span>
<span data-ttu-id="f12b3-214">O objeto JSON pode ter uma `one_body_amplitudes` propriedade cujo valor é uma matriz de operadores de cluster de um corpo e suas amplitudes.</span><span class="sxs-lookup"><span data-stu-id="f12b3-214">The JSON object MAY have a `one_body_amplitudes` property whose value is an array of one-body cluster operators and their amplitudes.</span></span>
<span data-ttu-id="f12b3-215">O objeto JSON pode ter uma `two_body_amplitudes` propriedade cujo valor é uma matriz de operadores de cluster de dois corpo e suas amplitudes.</span><span class="sxs-lookup"><span data-stu-id="f12b3-215">The JSON object MAY have a `two_body_amplitudes` property whose value is an array of two-body cluster operators and their amplitudes.</span></span>
<span data-ttu-id="f12b3-216">que contém uma matriz de Estados de base e suas amplitudes não normalizadas.</span><span class="sxs-lookup"><span data-stu-id="f12b3-216">containing an array of basis states and their unnormalized amplitudes.</span></span>

<span data-ttu-id="f12b3-217">Por exemplo, o estado $ $ \ket{\Text{Reference}} = (um ^ {\dagger} \_ {1, \uparrow}a ^ {\dagger} \_ {2, \uparrow}a ^ {\dagger} \_ {2, \downarrow}) \ket {0} , $ $</span><span class="sxs-lookup"><span data-stu-id="f12b3-217">For example, the state $$ \ket{\text{reference}}=(a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})\ket{0}, $$</span></span>

<span data-ttu-id="f12b3-218">$ $ \ket{\text{UCCSD}} = e ^ {T-T ^ \dagger}\ket{\Text{Reference}}, $ $</span><span class="sxs-lookup"><span data-stu-id="f12b3-218">$$ \ket{\text{UCCSD}}=e^{T-T^\dagger}\ket{\text{reference}}, $$</span></span>

<span data-ttu-id="f12b3-219">$ $ T = 0,1 a ^ {\dagger} \_ {3, \uparrow}a \_ {2, \downarrow} + 0,2 a ^ {\dagger} \_ {2, \uparrow}a \_ {2, \downarrow}-0,3 a ^ {\dagger} \_ {1, \uparrow}a ^ {\dagger} \_ {3, \downarrow}a { \_ 3, \uparrow}a \_ {2, \downarrow} $ $ é representado por</span><span class="sxs-lookup"><span data-stu-id="f12b3-219">$$ T = 0.1 a^{\dagger}\_{3,\uparrow}a\_{2,\downarrow} + 0.2 a^{\dagger}\_{2,\uparrow}a\_{2,\downarrow} - 0.3 a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{3,\downarrow}a\_{3,\uparrow}a\_{2,\downarrow} $$ is represented by</span></span>
```yaml
initial_state_suggestions: # optional. If not provided, spin-orbitals will be filled to minimize one-body diagonal term energies.
  - label: "UCCSD"
    method: unitary_coupled_cluster
    cluster_operator: # Initial state that cluster operator is applied to.
        reference_state: 
          [1.0, "(1a)+", "(2a)+", "(2b)+", '|vacuum>']
        one_body_amplitudes: # A one-body cluster term is t^{q}_{p} a^\dag_p a_q   
            - [0.1, "(3a)+", "(2b)"]
            - [-0.2, "(2a)+", "(2b)"]
        two_body_amplitudes: # A two-body unitary cluster term is t^{rs}_{pq} a^\dag_p a^\dag_q a_r a_s
            - [-0.3, "(1a)+", "(3b)+", "(3a)", "(2b)"]
```

#### <a name="basis-set-object"></a><span data-ttu-id="f12b3-220">Objeto de conjunto base</span><span class="sxs-lookup"><span data-stu-id="f12b3-220">Basis Set Object</span></span> ####

<span data-ttu-id="f12b3-221">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="f12b3-221">This section is normative.</span></span>

<span data-ttu-id="f12b3-222">Cada objeto de descrição do problema pode ter uma `basis_set` propriedade.</span><span class="sxs-lookup"><span data-stu-id="f12b3-222">Each problem description object MAY have a `basis_set` property.</span></span>
<span data-ttu-id="f12b3-223">Se houver, o valor da `basis_set` Propriedade deverá ser um objeto com duas propriedades `type` e `name` .</span><span class="sxs-lookup"><span data-stu-id="f12b3-223">If present, the value of the `basis_set` property MUST be an object with two properties, `type` and `name`.</span></span>

<span data-ttu-id="f12b3-224">As funções base identificadas pelo valor da `basis_set` Propriedade devem ser de valor real.</span><span class="sxs-lookup"><span data-stu-id="f12b3-224">The basis functions identified by the value of the `basis_set` property MUST be real-valued.</span></span>

> [!NOTE]
> <span data-ttu-id="f12b3-225">A suposição de que todas as funções de base tenham valor real pode ser reduzida em versões futuras desta especificação.</span><span class="sxs-lookup"><span data-stu-id="f12b3-225">The assumption that all basis functions are real-valued may be relaxed in future versions of this specification.</span></span>

## <a name="tables-and-lists"></a><span data-ttu-id="f12b3-226">Tabelas e listas</span><span class="sxs-lookup"><span data-stu-id="f12b3-226">Tables and Lists</span></span> ##

### <a name="table-1-allowed-physical-units"></a><span data-ttu-id="f12b3-227">Tabela 1.</span><span class="sxs-lookup"><span data-stu-id="f12b3-227">Table 1.</span></span> <span data-ttu-id="f12b3-228">Unidades físicas permitidas</span><span class="sxs-lookup"><span data-stu-id="f12b3-228">Allowed Physical Units</span></span> ###

<span data-ttu-id="f12b3-229">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="f12b3-229">This section is normative.</span></span>

<span data-ttu-id="f12b3-230">Qualquer cadeia de caracteres especificando uma unidade deve ser uma das seguintes:</span><span class="sxs-lookup"><span data-stu-id="f12b3-230">Any string specifying a unit MUST be one of the following:</span></span>

- `hartree`
- `ev`

<span data-ttu-id="f12b3-231">Analisadores e produtores devem tratar os seguintes objetos de quantidade simples como equivalentes:</span><span class="sxs-lookup"><span data-stu-id="f12b3-231">Parsers and producers MUST treat the following simple quantity objects as equivalent:</span></span>

```yaml
- {"units": "hartree", "value": 1}
- {"units": "ev", "value": 27.2113831301723}
```

### <a name="table-2-allowed-index-conventions"></a><span data-ttu-id="f12b3-232">Tabela 2.</span><span class="sxs-lookup"><span data-stu-id="f12b3-232">Table 2.</span></span> <span data-ttu-id="f12b3-233">Convenções de índice permitidas</span><span class="sxs-lookup"><span data-stu-id="f12b3-233">Allowed Index Conventions</span></span> ###

<span data-ttu-id="f12b3-234">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="f12b3-234">This section is normative.</span></span>

<span data-ttu-id="f12b3-235">Qualquer cadeia de caracteres especificando uma Convenção de índice deve ser uma das seguintes:</span><span class="sxs-lookup"><span data-stu-id="f12b3-235">Any string specifying an index convention MUST be one of the following:</span></span>

- `mulliken`

<span data-ttu-id="f12b3-236">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="f12b3-236">This section is informative.</span></span>

<span data-ttu-id="f12b3-237">As convenções de índice adicionais podem ser introduzidas em versões futuras desta especificação.</span><span class="sxs-lookup"><span data-stu-id="f12b3-237">Additional index conventions may be introduced in future versions of this specification.</span></span>

#### <a name="interpretation-of-index-conventions"></a><span data-ttu-id="f12b3-238">Interpretação de convenções de índice</span><span class="sxs-lookup"><span data-stu-id="f12b3-238">Interpretation of Index Conventions</span></span> ####

<span data-ttu-id="f12b3-239">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="f12b3-239">This section is informative.</span></span>

### <a name="table-3-allowed-state-methods"></a><span data-ttu-id="f12b3-240">Tabela 3.</span><span class="sxs-lookup"><span data-stu-id="f12b3-240">Table 3.</span></span> <span data-ttu-id="f12b3-241">Métodos de estado permitidos</span><span class="sxs-lookup"><span data-stu-id="f12b3-241">Allowed State methods</span></span> ###

<span data-ttu-id="f12b3-242">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="f12b3-242">This section is normative.</span></span>

<span data-ttu-id="f12b3-243">Qualquer cadeia de caracteres especificando um método de Estado deve ser uma das seguintes:</span><span class="sxs-lookup"><span data-stu-id="f12b3-243">Any string specifying a state method MUST be one of the following:</span></span>

- `sparse_multi_configurational`
- `unitary_coupled_cluster`

<span data-ttu-id="f12b3-244">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="f12b3-244">This section is informative.</span></span>

<span data-ttu-id="f12b3-245">Métodos de estado adicionais podem ser introduzidos em versões futuras desta especificação.</span><span class="sxs-lookup"><span data-stu-id="f12b3-245">Additional state methods may be introduced in future versions of this specification.</span></span>
