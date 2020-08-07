---
title: Especificação de esquema Broombridge (ver 0,1)
description: Detalha as especificações do esquema Broombridge quantum química v 0.1 para a biblioteca do Microsoft quantum química.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/17/2018
ms.topic: article
uid: microsoft.quantum.libraries.chemistry.schema.spec_v_0_1
no-loc:
- Q#
- $$v
ms.openlocfilehash: abbc63b8801c774e6ba06cff99b7382d64424b2c
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869130"
---
# <a name="broombridge-specification-v01"></a><span data-ttu-id="1df68-103">Especificação de Broombridge v 0,1</span><span class="sxs-lookup"><span data-stu-id="1df68-103">Broombridge Specification v0.1</span></span> #

<span data-ttu-id="1df68-104">As palavras-chave "deve", "não deve", "REQUIRED", "is", "maio" e "OPTIONAL" neste documento devem ser interpretadas conforme descrito em [RFC 2119](https://tools.ietf.org/html/rfc2119)(recomendável), "pode" e "opcional" neste documentos.</span><span class="sxs-lookup"><span data-stu-id="1df68-104">The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](https://tools.ietf.org/html/rfc2119).</span></span>

<span data-ttu-id="1df68-105">Qualquer barra lateral com os títulos "observação", "informações" ou "aviso" é informativa.</span><span class="sxs-lookup"><span data-stu-id="1df68-105">Any sidebar with the headings "NOTE," "INFORMATION," or "WARNING" is informative.</span></span>

## <a name="introduction"></a><span data-ttu-id="1df68-106">Introdução</span><span class="sxs-lookup"><span data-stu-id="1df68-106">Introduction</span></span> ##

<span data-ttu-id="1df68-107">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="1df68-107">This section is informative.</span></span>

<span data-ttu-id="1df68-108">Os documentos do Broombridge destinam-se a comunicar instâncias de problemas de simulação na química do Quantum para processamento usando simulação de Quantum e programação cadeias.</span><span class="sxs-lookup"><span data-stu-id="1df68-108">Broombridge documents are intended to communicate instances of simulation problems in quantum chemistry for processing using quantum simulation and programming toolchains.</span></span>

## <a name="serialization"></a><span data-ttu-id="1df68-109">Serialização</span><span class="sxs-lookup"><span data-stu-id="1df68-109">Serialization</span></span> ##

<span data-ttu-id="1df68-110">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="1df68-110">This section is normative.</span></span>

<span data-ttu-id="1df68-111">Um documento Broombridge deve ser serializado como um [documento YAML 1,2](http://yaml.org/spec/) que representa um objeto JSON, conforme descrito em [RFC 4627](https://tools.ietf.org/html/rfc4627) seção 2,2.</span><span class="sxs-lookup"><span data-stu-id="1df68-111">A Broombridge document MUST be serialized as a [YAML 1.2 document](http://yaml.org/spec/) representing a JSON object as described in [RFC 4627](https://tools.ietf.org/html/rfc4627) section 2.2.</span></span>
<span data-ttu-id="1df68-112">O objeto serializado para YAML deve ter uma propriedade `"$schema"` cujo valor é `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.1.schema.json"` e deve ser válido de acordo com as especificações do rascunho do esquema JSON-06 [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)].</span><span class="sxs-lookup"><span data-stu-id="1df68-112">The object serialized to YAML MUST have a property `"$schema"` whose value is `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.1.schema.json"`, and MUST be valid according to the JSON Schema draft-06 specifications [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)].</span></span>

<span data-ttu-id="1df68-113">Para o restante desta especificação, "o objeto Broombridge" fará referência ao objeto JSON desserializado de um documento Broombridge YAML.</span><span class="sxs-lookup"><span data-stu-id="1df68-113">For the remainder of this specification, "the Broombridge object" will refer to the JSON object deserialized from a Broombridge YAML document.</span></span>

<span data-ttu-id="1df68-114">A menos que indicado de outra forma explicitamente, os objetos não devem ter propriedades adicionais além daquelas especificadas explicitamente neste documento.</span><span class="sxs-lookup"><span data-stu-id="1df68-114">Unless otherwise explicitly noted, objects MUST NOT have additional properties beyond those specified explicitly in this document.</span></span>

## <a name="additional-definitions"></a><span data-ttu-id="1df68-115">Definições adicionais</span><span class="sxs-lookup"><span data-stu-id="1df68-115">Additional Definitions</span></span> ##

<span data-ttu-id="1df68-116">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="1df68-116">This section is normative.</span></span>

### <a name="quantity-objects"></a><span data-ttu-id="1df68-117">Quantidade de objetos</span><span class="sxs-lookup"><span data-stu-id="1df68-117">Quantity Objects</span></span> ###

<span data-ttu-id="1df68-118">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="1df68-118">This section is normative.</span></span>

<span data-ttu-id="1df68-119">Um _objeto Quantity_ é um objeto JSON e deve ter uma propriedade `units` cujo valor seja um dos valores permitidos listados na tabela 1.</span><span class="sxs-lookup"><span data-stu-id="1df68-119">A _quantity object_ is a JSON object, and MUST have a property `units` whose value is one of the allowed values listed in Table 1.</span></span>

<span data-ttu-id="1df68-120">Um objeto de quantidade é um _objeto de quantidade simples_ se tiver uma única propriedade, `value` além de sua `units` propriedade.</span><span class="sxs-lookup"><span data-stu-id="1df68-120">A quantity object is a _simple quantity object_ if it has a single property `value` in addition to its `units` property.</span></span>
<span data-ttu-id="1df68-121">O valor da `value` propriedade deve ser um número.</span><span class="sxs-lookup"><span data-stu-id="1df68-121">The value of the `value` property MUST be a number.</span></span>

<span data-ttu-id="1df68-122">Um objeto Quantity é um _objeto de quantidade vinculada_ se ele tiver as propriedades `lower` e, `upper` além de sua `units` propriedade.</span><span class="sxs-lookup"><span data-stu-id="1df68-122">A quantity object is a _bounded quantity object_ if it has the properties `lower` and `upper` in addition to its `units` property.</span></span>
<span data-ttu-id="1df68-123">Os valores das `lower` Propriedades e `upper` devem ser números.</span><span class="sxs-lookup"><span data-stu-id="1df68-123">The values of the `lower` and `upper` properties MUST be numbers.</span></span>
<span data-ttu-id="1df68-124">Um objeto de quantidade associada pode ter uma propriedade `value` cujo valor é um número.</span><span class="sxs-lookup"><span data-stu-id="1df68-124">A bounded quantity object MAY have a property `value` whose value is a number.</span></span>

<span data-ttu-id="1df68-125">Um objeto de quantidade é um _objeto de quantidade de matriz esparsa_ se ele tiver a propriedade `format` e uma propriedade além de `values` sua `units` propriedade.</span><span class="sxs-lookup"><span data-stu-id="1df68-125">A quantity object is a _sparse array quantity object_ if it has the property `format` and a property `values` in addition to its `units` property.</span></span>
<span data-ttu-id="1df68-126">O valor de `format` deve ser a cadeia de caracteres `sparse` .</span><span class="sxs-lookup"><span data-stu-id="1df68-126">The value of `format` MUST be the string `sparse`.</span></span>
<span data-ttu-id="1df68-127">O valor da `values` propriedade deve ser uma matriz.</span><span class="sxs-lookup"><span data-stu-id="1df68-127">The value of the `values` property MUST be an array.</span></span>
<span data-ttu-id="1df68-128">Cada elemento de `values` deve ser uma matriz que representa os índices e o valor da quantidade de matriz esparsa.</span><span class="sxs-lookup"><span data-stu-id="1df68-128">Each element of `values` MUST be an array representing the indices and value of the sparse array quantity.</span></span>

<span data-ttu-id="1df68-129">Os índices para cada elemento de um objeto de quantidade de matriz esparsa devem ser exclusivos em todo o objeto de quantidade de matriz esparsa.</span><span class="sxs-lookup"><span data-stu-id="1df68-129">The indices for each element of a sparse array quantity object MUST be unique across the entire sparse array quantity object.</span></span>
<span data-ttu-id="1df68-130">Se um índice estiver presente com um valor de `0` , um analisador deve tratar o objeto de quantidade de matriz esparsa de forma idêntica a um objeto de quantidade de matriz esparsa no qual esse índice não está presente.</span><span class="sxs-lookup"><span data-stu-id="1df68-130">If an index is present with a value of `0`, a parser MUST treat the sparse array quantity object identically to a sparse array quantity object in which that index is not present at all.</span></span>


<span data-ttu-id="1df68-131">Um objeto de quantidade deve ser</span><span class="sxs-lookup"><span data-stu-id="1df68-131">A quantity object MUST either be</span></span>

- <span data-ttu-id="1df68-132">um objeto de quantidade simples,</span><span class="sxs-lookup"><span data-stu-id="1df68-132">a simple quantity object,</span></span>
- <span data-ttu-id="1df68-133">um objeto de quantidade vinculada ou</span><span class="sxs-lookup"><span data-stu-id="1df68-133">a bounded quantity object, or</span></span>
- <span data-ttu-id="1df68-134">um objeto de quantidade de matriz esparsa.</span><span class="sxs-lookup"><span data-stu-id="1df68-134">a sparse array quantity object.</span></span>


### <a name="examples"></a><span data-ttu-id="1df68-135">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1df68-135">Examples</span></span> ###

<span data-ttu-id="1df68-136">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="1df68-136">This section is informative.</span></span>

<span data-ttu-id="1df68-137">Uma quantidade simples representando $1.9844146837 \, \mathrm{ha} $:</span><span class="sxs-lookup"><span data-stu-id="1df68-137">A simple quantity representing $1.9844146837\,\mathrm{Ha}$:</span></span>

```yaml
coulomb_repulsion:
    value: 1.9844146837
    units: hartree
```

<span data-ttu-id="1df68-138">Uma quantidade limitada que representa uma distribuição uniforme sobre o intervalo $ [-7,-6] \, \mathrm{ha} $:</span><span class="sxs-lookup"><span data-stu-id="1df68-138">A bounded quantity representing a uniform distribution over the interval $[-7, -6]\,\mathrm{Ha}$:</span></span>

```yaml
fci_energy:
    upper: -6
    lower: -7
    units: hartree
```

<span data-ttu-id="1df68-139">A seguir está uma quantidade de matriz esparsa com um elemento `[1, 2]` igual a `hello` e um elemento `[3, 4]` igual a `world` :</span><span class="sxs-lookup"><span data-stu-id="1df68-139">The following is a sparse array quantity with an element `[1, 2]` equal to `hello` and an element `[3, 4]` equal to `world`:</span></span>

```yaml
sparse_example:
    format: sparse
    units: hartree
    values:
    - [1, 2, "hello"]
    - [3, 4, "world"]
```

## <a name="format-section"></a><span data-ttu-id="1df68-140">Seção de formato</span><span class="sxs-lookup"><span data-stu-id="1df68-140">Format Section</span></span> ##

<span data-ttu-id="1df68-141">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="1df68-141">This section is normative.</span></span>

<span data-ttu-id="1df68-142">O objeto Broombridge deve ter uma propriedade `format` cujo valor é um objeto JSON com uma propriedade chamada `version` .</span><span class="sxs-lookup"><span data-stu-id="1df68-142">The Broombridge object MUST have a property `format` whose value is a JSON object with one property called `version`.</span></span>
<span data-ttu-id="1df68-143">A `version` propriedade deve ter o valor `"0.1"` .</span><span class="sxs-lookup"><span data-stu-id="1df68-143">The `version` property MUST have the value `"0.1"`.</span></span>

### <a name="example"></a><span data-ttu-id="1df68-144">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1df68-144">Example</span></span> ###

<span data-ttu-id="1df68-145">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="1df68-145">This section is informative.</span></span>

```yaml
format:                        # required
    version: "0.1"             # must match exactly
```

## <a name="integral-sets-section"></a><span data-ttu-id="1df68-146">Seção de conjuntos integrais</span><span class="sxs-lookup"><span data-stu-id="1df68-146">Integral Sets Section</span></span> ##

<span data-ttu-id="1df68-147">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="1df68-147">This section is normative.</span></span>

<span data-ttu-id="1df68-148">O objeto Broombridge deve ter uma propriedade `integral_sets` cujo valor é uma matriz JSON.</span><span class="sxs-lookup"><span data-stu-id="1df68-148">The Broombridge object MUST have a property `integral_sets` whose value is a JSON array.</span></span>
<span data-ttu-id="1df68-149">Cada item no valor da `integral_sets` propriedade deve ser um objeto JSON que descreve um conjunto de integrais, conforme descrito no restante desta seção.</span><span class="sxs-lookup"><span data-stu-id="1df68-149">Each item in the value of the `integral_sets` property MUST be a JSON object describing one set of integrals, as described in the remainder of this section.</span></span>
<span data-ttu-id="1df68-150">No restante desta seção, o termo "objeto de conjunto integral" fará referência a um item no valor da `integral_sets` Propriedade do objeto Broombridge.</span><span class="sxs-lookup"><span data-stu-id="1df68-150">In the remainder of this section, the term "integral set object" will refer to an item in the value of the `integral_sets` property of the Broombridge object.</span></span>

<span data-ttu-id="1df68-151">Cada objeto de conjunto integral deve ter uma propriedade `metadata` cujo valor é um objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="1df68-151">Each integral set object MUST have a property `metadata` whose value is a JSON object.</span></span>
<span data-ttu-id="1df68-152">O valor de `metadata` pode ser o objeto JSON vazio (ou seja, `{}` ) ou pode conter propriedades adicionais definidas pelo implementador.</span><span class="sxs-lookup"><span data-stu-id="1df68-152">The value of `metadata` MAY be the empty JSON object (that is, `{}`), or MAY contain additional properties defined by the implementor.</span></span>

### <a name="hamiltonian-section"></a><span data-ttu-id="1df68-153">Seção Hamiltonian</span><span class="sxs-lookup"><span data-stu-id="1df68-153">Hamiltonian Section</span></span> ###

#### <a name="overview"></a><span data-ttu-id="1df68-154">Visão geral</span><span class="sxs-lookup"><span data-stu-id="1df68-154">Overview</span></span> ####

<span data-ttu-id="1df68-155">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="1df68-155">This section is informative.</span></span>

<span data-ttu-id="1df68-156">A `hamiltonian` propriedade de cada objeto de conjunto inteiro descreve o Hamiltonian para um problema de química do Quantum específico, listando seus termos de um e dois corpo como matrizes esparsas de números reais.</span><span class="sxs-lookup"><span data-stu-id="1df68-156">The `hamiltonian` property of each integral set object describes the Hamiltonian for a particular quantum chemistry problem by listing out its one- and two-body terms as sparse arrays of real numbers.</span></span>
<span data-ttu-id="1df68-157">Os operadores Hamiltonian descritos por cada objeto de conjunto integral assumem o formulário</span><span class="sxs-lookup"><span data-stu-id="1df68-157">The Hamiltonian operators described by each integral set object take the form</span></span>

<span data-ttu-id="1df68-158">$ $ H = \sum \_ \{ i, j \} \sum \_ {\sigma\in \\ {\uparrow, \downarrow \\ }} H \_ \{ IJ \} a ^ \{ \dagger \} \_ {i, \sigma} a \_ {j, \sigma} + \frac {1} {2} \sum \_ \{ i, j, k, l \} \sum \_ {\sigma, \rho\in \\ {\uparrow, \downarrow \\ }} H \_ {ijkl} a ^ \dagger \_ {i, \sigma} a ^ \dagger \_ {k, \rho} a \_ {l, \rho} a \_ {j, \sigma}, $ $</span><span class="sxs-lookup"><span data-stu-id="1df68-158">$$ H = \sum\_\{i,j\}\sum\_{\sigma\in\\{\uparrow,\downarrow\\}} h\_\{ij\} a^\{\dagger\}\_{i,\sigma} a\_{j,\sigma} + \frac{1}{2}\sum\_\{i,j,k,l\}\sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}} h\_{ijkl} a^\dagger\_{i,\sigma} a^\dagger\_{k,\rho} a\_{l,\rho} a\_{j,\sigma}, $$</span></span>

<span data-ttu-id="1df68-159">Aqui $h _ {ijkl} = (IJ | KL) $ na Convenção Mulliken.</span><span class="sxs-lookup"><span data-stu-id="1df68-159">here $h_{ijkl}= (ij|kl)$ in Mulliken convention.</span></span>

<span data-ttu-id="1df68-160">Para maior clareza, o termo One-at é</span><span class="sxs-lookup"><span data-stu-id="1df68-160">For clarity, the one-electron term is</span></span>

<span data-ttu-id="1df68-161">$ $ h_ {IJ} = \int {\mathrm d} x \psi ^ \* \_ i (x) \left (\frac {1} {2} \nabla ^ 2 + \sum \_ {A} \frac{Z \_ a} {| x-x \_ a |}  \right) \psi \_ j (x), $ $</span><span class="sxs-lookup"><span data-stu-id="1df68-161">$$ h_{ij} = \int {\mathrm d}x \psi^\*\_i(x) \left(\frac{1}{2}\nabla^2 + \sum\_{A}\frac{Z\_A}{|x-x\_A|}  \right) \psi\_j(x), $$</span></span>

<span data-ttu-id="1df68-162">e o termo de duas-bits é</span><span class="sxs-lookup"><span data-stu-id="1df68-162">and the two-electron term is</span></span>

<span data-ttu-id="1df68-163">$ $ h \_ \{ ijkl \} = \iint \{ \mathrm d \} x ^ 2 \psi ^ \{ \* \} \_ i (x \_ 1) \psi \_ j (x \_ 1) \frac \{ 1 \} \{ \| x \_ 1-x \_ 2 \| \} \psi \_ k ^ \{ \* \} (x \_ 2) \psi \_ l (x \_ 2).</span><span class="sxs-lookup"><span data-stu-id="1df68-163">$$ h\_\{ijkl\} = \iint \{\mathrm d\}x^2 \psi^\{\*\}\_i(x\_1)\psi\_j(x\_1) \frac\{1\}\{\|x\_1 -x\_2\|\}\psi\_k^\{\*\}(x\_2) \psi\_l(x\_2).</span></span>
$$

<span data-ttu-id="1df68-164">Conforme observado em nossa descrição da [ `basis_set` Propriedade](#basis-set-object) de cada elemento da `integral_sets` propriedade, supomos que as funções de base usadas sejam de valor real.</span><span class="sxs-lookup"><span data-stu-id="1df68-164">As noted in our description of the [`basis_set` property](#basis-set-object) of each element of the `integral_sets` property, we further explicitly assume that the basis functions used are real-valued.</span></span>
<span data-ttu-id="1df68-165">Isso nos permite usar os seguintes Symmetries entre os termos para compactar a representação do Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="1df68-165">This allows us to use the following symmetries between the terms to compress the representation of the Hamiltonian.</span></span>

<span data-ttu-id="1df68-166">$ $ h_ {ijkl} = h_ {Ijlk} = h_ {jikl} = h_ {jilk} = h_ {klij} = h_ {klji} = h_ {lkij} = h_ {LKJI}.</span><span class="sxs-lookup"><span data-stu-id="1df68-166">$$ h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkij}=h_{lkji}.</span></span>
$$


#### <a name="contents"></a><span data-ttu-id="1df68-167">Sumário</span><span class="sxs-lookup"><span data-stu-id="1df68-167">Contents</span></span> ####

<span data-ttu-id="1df68-168">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="1df68-168">This section is normative.</span></span>

<span data-ttu-id="1df68-169">Cada conjunto integral deve ter uma propriedade `hamiltonian` cujo valor é um objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="1df68-169">Each integral set MUST have a property `hamiltonian` whose value is a JSON object.</span></span>
<span data-ttu-id="1df68-170">O valor da `hamiltonian` propriedade é conhecido como um objeto Hamiltonian e deve ter as propriedades e, `one_electron_integrals` `two_electron_integrals` conforme descrito no restante desta seção.</span><span class="sxs-lookup"><span data-stu-id="1df68-170">The value of the `hamiltonian` property is known as a Hamiltonian object, and MUST have the properties `one_electron_integrals` and `two_electron_integrals` as described in the remainder of this section.</span></span>
<span data-ttu-id="1df68-171">Um objeto Hamiltonian também pode ter uma propriedade `particle_hole_representation` .</span><span class="sxs-lookup"><span data-stu-id="1df68-171">A Hamiltonian object MAY also have a property `particle_hole_representation`.</span></span>
<span data-ttu-id="1df68-172">Se presente, o valor de `particle_hole_representation` deve seguir o formato descrito no restante desta seção.</span><span class="sxs-lookup"><span data-stu-id="1df68-172">If present, the value of `particle_hole_representation` MUST follow the format described in the remainder of this section.</span></span>

##### <a name="one-electron-integrals-object"></a><span data-ttu-id="1df68-173">Objeto de integral de um único-</span><span class="sxs-lookup"><span data-stu-id="1df68-173">One-Electron Integrals Object</span></span> #####

<span data-ttu-id="1df68-174">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="1df68-174">This section is normative.</span></span>

<span data-ttu-id="1df68-175">A `one_electron_integrals` Propriedade do objeto HAMILTONIAN deve ser uma quantidade de matriz esparsa cujos índices são dois inteiros e cujos valores são números.</span><span class="sxs-lookup"><span data-stu-id="1df68-175">The `one_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity whose indices are two integers and whose values are numbers.</span></span>
<span data-ttu-id="1df68-176">Cada termo deve ter índices `[i, j]` onde `i >= j` .</span><span class="sxs-lookup"><span data-stu-id="1df68-176">Every term MUST have indices `[i, j]` where `i >= j`.</span></span>

> <span data-ttu-id="1df68-177">ANOTAÇÕES Isso reflete a simetria de que $h _ {IJ} = h_ {ji} $, que é uma conseqüência do fato de que o Hamiltonian é Hermitian.</span><span class="sxs-lookup"><span data-stu-id="1df68-177">[NOTE] This reflects the symmetry that $h_{ij} = h_{ji}$ which is a consequence of the fact that the Hamiltonian is Hermitian.</span></span>


###### <a name="example"></a><span data-ttu-id="1df68-178">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1df68-178">Example</span></span> ######

<span data-ttu-id="1df68-179">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="1df68-179">This section is informative.</span></span>

<span data-ttu-id="1df68-180">A quantidade de matriz esparsa a seguir representa o Hamiltonian $ $ H = \left (-5,0 (a ^ \{ \dagger \} \_ {1, \uparrow} a \_ {1, \uparrow} + a ^ \{ \dagger \} \_ {1, \downarrow} a \_ {1, \downarrow}) + 0,17 (a ^ \{ \dagger \} \_ {2, \uparrow} a \_ {1, \uparrow} + a ^ \{ \dagger \} \_ {1, \uparrow} a \_ {2, \uparrow} + a ^ \{ \dagger \} \_ {2, \downarrow} a \_ {1, \downarrow} + a ^ \{ \dagger \} \_ {1, \downarrow} a \_ {2, \downarrow}) \right) \\ , \mathrm{ha}.</span><span class="sxs-lookup"><span data-stu-id="1df68-180">The following sparse array quantity represents the Hamiltonian $$ H = \left(-5.0  (a^\{\dagger\}\_{1,\uparrow} a\_{1,\uparrow}+a^\{\dagger\}\_{1,\downarrow} a\_{1,\downarrow})+ 0.17 (a^\{\dagger\}\_{2,\uparrow} a\_{1,\uparrow}+ a^\{\dagger\}\_{1,\uparrow} a\_{2,\uparrow}+a^\{\dagger\}\_{2,\downarrow} a\_{1,\downarrow}+ a^\{\dagger\}\_{1,\downarrow} a\_{2,\downarrow})\right)\\,\mathrm{Ha}.</span></span>
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
> <span data-ttu-id="1df68-181">Broombridge usa indexação com base em 1.</span><span class="sxs-lookup"><span data-stu-id="1df68-181">Broombridge uses 1-based indexing.</span></span>


##### <a name="two-electron-integrals-object"></a><span data-ttu-id="1df68-182">Objeto de integral de dois bits</span><span class="sxs-lookup"><span data-stu-id="1df68-182">Two-Electron Integrals Object</span></span> #####

<span data-ttu-id="1df68-183">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="1df68-183">This section is normative.</span></span>

<span data-ttu-id="1df68-184">A `two_electron_integrals` Propriedade do objeto HAMILTONIAN deve ser uma quantidade de matriz esparsa com uma propriedade adicional chamada `index_convention` .</span><span class="sxs-lookup"><span data-stu-id="1df68-184">The `two_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity with one additional property called `index_convention`.</span></span>
<span data-ttu-id="1df68-185">Cada elemento do valor de `two_electron_integrals` deve ter quatro índices.</span><span class="sxs-lookup"><span data-stu-id="1df68-185">Each element of the value of `two_electron_integrals` MUST have four indices.</span></span>

<span data-ttu-id="1df68-186">Cada `two_electron_integrals` propriedade deve ter uma `index_convention` propriedade.</span><span class="sxs-lookup"><span data-stu-id="1df68-186">Each `two_electron_integrals` property MUST have a `index_convention` property.</span></span>
<span data-ttu-id="1df68-187">O valor da `index_convention` propriedade deve ser um dos valores permitidos listados na tabela 1.</span><span class="sxs-lookup"><span data-stu-id="1df68-187">The value of the `index_convention` property MUST be one of the allowed values listed in Table 1.</span></span>
<span data-ttu-id="1df68-188">Se o valor de `index_convention` for `mulliken` , para cada elemento da quantidade de `two_electron_integrals` matriz esparsa, um analisador que carrega um documento Broombridge deve criar uma instância de um termo Hamiltonian igual ao operador de dois bits $h _ {i, j, k, l} a ^ \ dagger_i um ^ \ dagger_j a_k A_L $, em que $i $, $j $, $k $ e $l $ devem ser inteiros no intervalo inclusivo de 1 até o número de elétrons especificado pela `n_electrons` Propriedade do objeto de conjunto integral e em que $h _ {i, j, k, l} $ é o elemento `[i, j, k, l, h(i, j, k, l)]` da quantidade de matriz esparsa.</span><span class="sxs-lookup"><span data-stu-id="1df68-188">If the value of `index_convention` is `mulliken`, then for each element of the `two_electron_integrals` sparse array quantity, a parser loading a Broombridge document MUST instantiate a Hamiltonian term equal to the two-electron operator $h_{i, j, k, l} a^\dagger_i a^\dagger_j a_k a_l$, where $i$, $j$, $k$, and $l$ MUST be integers in the inclusive range from 1 to the number of electrons specified by the `n_electrons` property of the integral set object, and where $h_{i, j, k, l}$ is the element `[i, j, k, l, h(i, j, k, l)]` of the sparse array quantity.</span></span>

###### <a name="symmetries"></a><span data-ttu-id="1df68-189">Symmetries</span><span class="sxs-lookup"><span data-stu-id="1df68-189">Symmetries</span></span> ######

<span data-ttu-id="1df68-190">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="1df68-190">This section is normative.</span></span>

<span data-ttu-id="1df68-191">Se a `index_convention` propriedade de um `two_electron_integrals` objeto for igual a `mulliken` , se um elemento com índices `[i, j, k, l]` estiver presente, os seguintes índices não deverão estar presentes, a menos que sejam iguais a `[i, j, k, l]` :</span><span class="sxs-lookup"><span data-stu-id="1df68-191">If the `index_convention` property of a `two_electron_integrals` object is equal to `mulliken`, then if an element with indices `[i, j, k, l]` is present, the following indices MUST NOT be present unless they are equal to `[i, j, k, l]`:</span></span>

- `[i, j, l, k]`
- `[j, i, k, l]`
- `[j, i, l, k]`
- `[k, l, i, j]`
- `[k, l, j, i]`
- `[l, k, j, i]`

> [!NOTE]
> <span data-ttu-id="1df68-192">Como a `index_convention` propriedade é um objeto de quantidade esparsa, nenhum índice pode ser repetido em elementos diferentes.</span><span class="sxs-lookup"><span data-stu-id="1df68-192">Because the `index_convention` property is a sparse quantity object, no indices may be repeated on different elements.</span></span>
> <span data-ttu-id="1df68-193">Em particular, se um elemento com índices `[i, j, k, l]` estiver presente, nenhum outro elemento poderá ter esses índices.</span><span class="sxs-lookup"><span data-stu-id="1df68-193">In particular, if an element with indices `[i, j, k, l]` is present, no other element may have those indices.</span></span>


<!-- h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkji}. -->

###### <a name="example"></a><span data-ttu-id="1df68-194">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1df68-194">Example</span></span> #######

<span data-ttu-id="1df68-195">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="1df68-195">This section is informative.</span></span>

<span data-ttu-id="1df68-196">O objeto a seguir especifica o Hamiltonian</span><span class="sxs-lookup"><span data-stu-id="1df68-196">The following object specifies the Hamiltonian</span></span>

<span data-ttu-id="1df68-197">$ $ H = \frac12 \sum \_ {\sigma, \rho\in \\ {\uparrow, \downarrow \\ }} \Biggr (1,6 a ^ {\dagger} \_ {1, \sigma} a ^ {\dagger} \_ {1, \rho} a \_ {1, \rho} a \_ {1, \sigma}-0,1 a ^ {\dagger} \_ {6, \sigma} a ^ {\dagger} { \_ 1, \rho} a \_ {3, \rho} a \_ {2, \sigma}-0,1 a ^ {\dagger} \_ {6, \sigma} a ^ {\dagger} \_ {1, \rho} a \_ {2, \rho} a \_ {3, \sigma}-0,1 a ^ {\dagger} \_ {1, \sigma} a ^ {\dagger} \_ {6, \rho} a \_ {3, \rho} a \_ {2, \sigma}-0,1 a ^ {\dagger} \_ {1, \sigma} a ^ {\dagger} \_ {6, \rho} a \_ {2, \rho} a \_ {3, \sigma} $ $ $ $-0,1 a ^ {\dagger} \_ {3, \sigma} a ^ {\dagger} \_ {2, \rho} a \_ {6, \rho} a \_ {1, \sigma}-0,1 a ^ {\dagger} \_ {3, \sigma} a ^ {\dagger} \_ {2, \rho} a \_ {1, \rho} a \_ {6, \sigma}-0,1 a ^ {\dagger} \_ {2, \sigma} a ^ {\dagger} \_ {3 , \rho} a \_ {6, \rho} a \_ {1, \sigma}-0,1 a ^ {\dagger} \_ {2, \sigma} a ^ {\dagger} \_ {3, \rho} a \_ {1, \Rho} a \_ {6, \sigma}\Biggr) \\ , \textrm{ha}.</span><span class="sxs-lookup"><span data-stu-id="1df68-197">$$ H = \frac12 \sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}}\Biggr( 1.6 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{1,\rho} a\_{1,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{2,\rho} a\_{3,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{2,\rho} a\_{3,\sigma} $$ $$- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{1,\rho} a\_{6,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{1,\rho} a\_{6,\sigma}\Biggr)\\,\textrm{Ha}.</span></span>
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

##### <a name="particlehole-representation-object"></a><span data-ttu-id="1df68-198">Partícula – objeto de representação de orifício</span><span class="sxs-lookup"><span data-stu-id="1df68-198">Particle–Hole Representation Object</span></span> #####

<span data-ttu-id="1df68-199">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="1df68-199">This section is normative.</span></span>

<span data-ttu-id="1df68-200">O objeto partícula – representação de orifício especifica que os integrais armazenados são definidos com relação à representação de orifícios de partículas, em que os operadores de criação e Annihilation descrevem excitations fora do estado de referência usado, como um estado Hartree – Fock.</span><span class="sxs-lookup"><span data-stu-id="1df68-200">The particle–hole representation object specifies that the integrals stored are defined with respect to particle hole representation wherein the creation and annihilation operators describe excitations away from the reference state used, such as a Hartree–Fock state.</span></span>
<span data-ttu-id="1df68-201">O objeto é opcional.</span><span class="sxs-lookup"><span data-stu-id="1df68-201">The object is OPTIONAL.</span></span>
<span data-ttu-id="1df68-202">Se o objeto não for especificado, o Hamiltonian será interpretado como não fornecido na representação de orifício de partículas.</span><span class="sxs-lookup"><span data-stu-id="1df68-202">If the object is not specified then the Hamiltonian is to be interpreted as not given in particle-hole representation.</span></span>
<span data-ttu-id="1df68-203">Se presente, o valor de `particle_hole_representation` deve ser um objeto de quantidade de matriz esparsa cujos índices são quatro inteiros e cujos valores são um número e uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1df68-203">If present, the value of `particle_hole_representation` MUST be a sparse array quantity object whose indices are four integers, and whose values are a number and a string.</span></span>
<span data-ttu-id="1df68-204">A parte da cadeia de caracteres do valor de cada elemento deve conter somente os caracteres `'+'` e `'-'` que especifica se um determinado fator é um operador de criação ou Annihilation na partícula – a representação de orifício.</span><span class="sxs-lookup"><span data-stu-id="1df68-204">The string portion of the value of each element MUST contain only the characters `'+'` and `'-'` which specifies whether a given factor in the term is a creation or annihilation operator in the particle–hole representation.</span></span>  <span data-ttu-id="1df68-205">Por exemplo `"-+++"` , coresponde a um orifício que está sendo criado no site $i $ e as partículas que estão sendo criadas nos sites $j, k $ e $l $.</span><span class="sxs-lookup"><span data-stu-id="1df68-205">For example `"-+++"` coresponds to a hole being created at site $i$ and particles being created at sites $j,k$ and $l$.</span></span>

> [!NOTE]
> <span data-ttu-id="1df68-206">Como o valor de `particle_hole_representation` é um objeto de quantidade de matriz esparsa, `unit` as `format` Propriedades e devem ser especificadas.</span><span class="sxs-lookup"><span data-stu-id="1df68-206">As the value of the `particle_hole_representation` is a sparse array quantity object, the `unit` and `format` properties must be specified.</span></span>
> <span data-ttu-id="1df68-207">As unidades aceitáveis incluem listadas na tabela 1.</span><span class="sxs-lookup"><span data-stu-id="1df68-207">Acceptable units include are listed in Table 1.</span></span>
> <span data-ttu-id="1df68-208">A `format` propriedade é necessária e indica se os coeficientes Hamiltonian são especificados como uma matriz densa ou esparsa.</span><span class="sxs-lookup"><span data-stu-id="1df68-208">The `format` property is required, and indicates whether the Hamiltonian coefficients are specified as a dense or sparse array.</span></span>
> <span data-ttu-id="1df68-209">Na versão atual, somente as matrizes esparsas têm suporte, com a interpretação de que todos os elementos não especificados são $0 $, mas as versões futuras podem adicionar suporte para valores adicionais da `format` propriedade.</span><span class="sxs-lookup"><span data-stu-id="1df68-209">In the current version, only sparse arrays are supported, with interpretation that all unspecified elements are $0$, but future versions may add support for additional values of the `format` property.</span></span>

### <a name="initial-state-section"></a><span data-ttu-id="1df68-210">Seção de estado inicial</span><span class="sxs-lookup"><span data-stu-id="1df68-210">Initial State Section</span></span> ###

<span data-ttu-id="1df68-211">O objeto initial_state_suggestion especifica os Estados de Quantum inicial de interesse para o Hamiltonian especificado.</span><span class="sxs-lookup"><span data-stu-id="1df68-211">The initial_state_suggestion object specifies initial quantum states of interest to the specified Hamiltonian.</span></span> <span data-ttu-id="1df68-212">Esse objeto deve ser uma matriz de `state` objetos JSON.</span><span class="sxs-lookup"><span data-stu-id="1df68-212">This object must be an array of JSON `state` objects.</span></span>

#### <a name="state-object"></a><span data-ttu-id="1df68-213">Objeto de estado</span><span class="sxs-lookup"><span data-stu-id="1df68-213">State object</span></span> ####

<span data-ttu-id="1df68-214">Cada Estado representa uma superposição de órbitas ocupados.</span><span class="sxs-lookup"><span data-stu-id="1df68-214">Each states represents a superposition of occupied orbitals.</span></span> <span data-ttu-id="1df68-215">Cada objeto de Estado deve ter uma `label` propriedade que contém uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1df68-215">Each state object MUST have a `label` property containing a string.</span></span> <span data-ttu-id="1df68-216">Cada objeto de Estado deve ter uma `superposition` propriedade que contenha uma matriz de Estados de base e suas amplitudes não normalizadas.</span><span class="sxs-lookup"><span data-stu-id="1df68-216">Each state object MUST have a `superposition` property containing an array of basis states and their unnormalized amplitudes.</span></span>

<span data-ttu-id="1df68-217">Por exemplo, os Estados iniciais $ $ \ket{G0} = \ket{G1} = \ket{G2} = (a ^ {\dagger} \_ {1, \uparrow}a ^ {\dagger} \_ {2, \uparrow}a ^ {\dagger} \_ {2, \downarrow}) \ket {0} $ $ $ $ \ket{E} = \frac{0.1 (a ^ {\dagger} \_ {1, \uparrow}a ^ {\dagger} \_ {2, \uparrow}a ^ {\dagger} \_ {2, \downarrow}) + 0.2 (um ^ {\dagger} \_ {1, \uparrow}a ^ {\dagger} \_ {3, \uparrow}a ^ {\dagger} \_ {2, \downarrow})} {\sqrt{| 0,1 | ^ 2 + | 0.2 | ^ 2}} \ket {0} $ $ são representados por</span><span class="sxs-lookup"><span data-stu-id="1df68-217">For example, the initial states $$ \ket{G0}=\ket{G1}=\ket{G2}=(a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})\ket{0} $$ $$ \ket{E}=\frac{0.1 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})+0.2 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{3,\uparrow}a^{\dagger}\_{2,\downarrow})}{\sqrt{|0.1|^2+|0.2|^2}}\ket{0} $$ are represented by</span></span>
```yaml
initial_state_suggestions: # optional. If not provided, spin-orbitals will be filled to minimize one-body diagonal term energies.
    - state:
        label: "|G0>"
        superposition:
            - [1.0, "(1a)+","(2a)+","(2b)+","|vacuum>"]
    - state:
        label: "|G1>"
        superposition:
            - [-1.0, "(2a)+","(1a)+","(2b)+","|vacuum>"]
    - state:
        label: "|G2>"
        superposition:
            - [1.0, "(3a)","(1a)+","(2a)+","(3a)+","(2b)+","|vacuum>"]
    - state:
        label: "|E>"
        superposition:
            - [0.1, "(1a)+","(2a)+","(2b)+","|vacuum>"]
            - [0.2, "(1a)+","(3a)+","(2b)+","|vacuum>"]
```

#### <a name="basis-set-object"></a><span data-ttu-id="1df68-218">Objeto de conjunto base</span><span class="sxs-lookup"><span data-stu-id="1df68-218">Basis Set Object</span></span> ####

<span data-ttu-id="1df68-219">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="1df68-219">This section is normative.</span></span>

<span data-ttu-id="1df68-220">Cada objeto de conjunto integral pode ter uma `basis_set` propriedade.</span><span class="sxs-lookup"><span data-stu-id="1df68-220">Each integral set object MAY have a `basis_set` property.</span></span>
<span data-ttu-id="1df68-221">Se houver, o valor da `basis_set` Propriedade deverá ser um objeto com duas propriedades `type` e `name` .</span><span class="sxs-lookup"><span data-stu-id="1df68-221">If present, the value of the `basis_set` property MUST be an object with two properties, `type` and `name`.</span></span>

<span data-ttu-id="1df68-222">As funções base identificadas pelo valor da `basis_set` Propriedade devem ser de valor real.</span><span class="sxs-lookup"><span data-stu-id="1df68-222">The basis functions identified by the value of the `basis_set` property MUST be real-valued.</span></span>

> [!NOTE]
> <span data-ttu-id="1df68-223">A suposição de que todas as funções de base tenham valor real pode ser reduzida em versões futuras desta especificação.</span><span class="sxs-lookup"><span data-stu-id="1df68-223">The assumption that all basis functions are real-valued may be relaxed in future versions of this specification.</span></span>

## <a name="tables-and-lists"></a><span data-ttu-id="1df68-224">Tabelas e listas</span><span class="sxs-lookup"><span data-stu-id="1df68-224">Tables and Lists</span></span> ##

### <a name="table-1-allowed-physical-units"></a><span data-ttu-id="1df68-225">Tabela 1.</span><span class="sxs-lookup"><span data-stu-id="1df68-225">Table 1.</span></span> <span data-ttu-id="1df68-226">Unidades físicas permitidas</span><span class="sxs-lookup"><span data-stu-id="1df68-226">Allowed Physical Units</span></span> ###

<span data-ttu-id="1df68-227">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="1df68-227">This section is normative.</span></span>

<span data-ttu-id="1df68-228">Qualquer cadeia de caracteres especificando uma unidade deve ser uma das seguintes:</span><span class="sxs-lookup"><span data-stu-id="1df68-228">Any string specifying a unit MUST be one of the following:</span></span>

- `hartree`
- `ev`

<span data-ttu-id="1df68-229">Analisadores e produtores devem tratar os seguintes objetos de quantidade simples como equivalentes:</span><span class="sxs-lookup"><span data-stu-id="1df68-229">Parsers and producers MUST treat the following simple quantity objects as equivalent:</span></span>

```yaml
- {"units": "hartree", "value": 1}
- {"units": "ev", "value": 27.2113831301723}
```

### <a name="table-2-allowed-index-conventions"></a><span data-ttu-id="1df68-230">Tabela 2.</span><span class="sxs-lookup"><span data-stu-id="1df68-230">Table 2.</span></span> <span data-ttu-id="1df68-231">Convenções de índice permitidas</span><span class="sxs-lookup"><span data-stu-id="1df68-231">Allowed Index Conventions</span></span> ###

<span data-ttu-id="1df68-232">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="1df68-232">This section is normative.</span></span>

<span data-ttu-id="1df68-233">Qualquer cadeia de caracteres especificando uma Convenção de índice deve ser uma das seguintes:</span><span class="sxs-lookup"><span data-stu-id="1df68-233">Any string specifying an index convention MUST be one of the following:</span></span>

- `mulliken`

<span data-ttu-id="1df68-234">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="1df68-234">This section is informative.</span></span>

<span data-ttu-id="1df68-235">As convenções de índice adicionais podem ser introduzidas em versões futuras desta especificação.</span><span class="sxs-lookup"><span data-stu-id="1df68-235">Additional index conventions may be introduced in future versions of this specification.</span></span>

#### <a name="interpretation-of-index-conventions"></a><span data-ttu-id="1df68-236">Interpretação de convenções de índice</span><span class="sxs-lookup"><span data-stu-id="1df68-236">Interpretation of Index Conventions</span></span> ####

<span data-ttu-id="1df68-237">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="1df68-237">This section is informative.</span></span>
