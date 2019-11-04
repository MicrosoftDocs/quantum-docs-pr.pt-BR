---
title: Especificação de esquema Broombridge
author: guanghaolow
ms.author: gulow@microsoft.com
ms.date: 05/28/2019
ms.topic: article
uid: microsoft.quantum.libraries.chemistry.schema.spec_v_0_2
ms.openlocfilehash: 2f4be96bc6f1e8e6fe21b93bc0d9ab2aa367fd53
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/29/2019
ms.locfileid: "73185300"
---
# <a name="broombridge-specification-v02"></a><span data-ttu-id="7873d-102">Especificação Broombridge v 0.2</span><span class="sxs-lookup"><span data-stu-id="7873d-102">Broombridge Specification v0.2</span></span> #

<span data-ttu-id="7873d-103">As palavras-chave "deve", "não deve", "REQUIRED", "is", "maio" e "OPTIONAL" neste documento devem ser interpretadas conforme descrito em [RFC 2119](https://tools.ietf.org/html/rfc2119)(recomendável), "pode" e "opcional" neste documentos.</span><span class="sxs-lookup"><span data-stu-id="7873d-103">The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](https://tools.ietf.org/html/rfc2119).</span></span>

<span data-ttu-id="7873d-104">Qualquer barra lateral com os títulos "observação", "informações" ou "aviso" é informativa.</span><span class="sxs-lookup"><span data-stu-id="7873d-104">Any sidebar with the headings "NOTE," "INFORMATION," or "WARNING" is informative.</span></span>

## <a name="introduction"></a><span data-ttu-id="7873d-105">Introdução</span><span class="sxs-lookup"><span data-stu-id="7873d-105">Introduction</span></span> ##

<span data-ttu-id="7873d-106">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="7873d-106">This section is informative.</span></span>

<span data-ttu-id="7873d-107">Os documentos do Broombridge destinam-se a comunicar instâncias de problemas de simulação na química do Quantum para processamento usando simulação de Quantum e programação cadeias.</span><span class="sxs-lookup"><span data-stu-id="7873d-107">Broombridge documents are intended to communicate instances of simulation problems in quantum chemistry for processing using quantum simulation and programming toolchains.</span></span>

## <a name="serialization"></a><span data-ttu-id="7873d-108">Serialização</span><span class="sxs-lookup"><span data-stu-id="7873d-108">Serialization</span></span> ##

<span data-ttu-id="7873d-109">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="7873d-109">This section is normative.</span></span>

<span data-ttu-id="7873d-110">Um documento Broombridge deve ser serializado como um [documento YAML 1,2](http://yaml.org/spec/) que representa um objeto JSON, conforme descrito em [RFC 4627](https://tools.ietf.org/html/rfc4627) seção 2,2.</span><span class="sxs-lookup"><span data-stu-id="7873d-110">A Broombridge document MUST be serialized as a [YAML 1.2 document](http://yaml.org/spec/) representing a JSON object as described in [RFC 4627](https://tools.ietf.org/html/rfc4627) section 2.2.</span></span>
<span data-ttu-id="7873d-111">O objeto serializado para YAML deve ter uma propriedade `"$schema"` cujo valor é `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.2.schema.json"`e deve ser válido de acordo com as especificações de rascunho do esquema JSON-06 [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)].</span><span class="sxs-lookup"><span data-stu-id="7873d-111">The object serialized to YAML MUST have a property `"$schema"` whose value is `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.2.schema.json"`, and MUST be valid according to the JSON Schema draft-06 specifications [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)].</span></span>

<span data-ttu-id="7873d-112">Para o restante desta especificação, "o objeto Broombridge" fará referência ao objeto JSON desserializado de um documento Broombridge YAML.</span><span class="sxs-lookup"><span data-stu-id="7873d-112">For the remainder of this specification, "the Broombridge object" will refer to the JSON object deserialized from a Broombridge YAML document.</span></span>

<span data-ttu-id="7873d-113">A menos que indicado de outra forma explicitamente, os objetos não devem ter propriedades adicionais além daquelas especificadas explicitamente neste documento.</span><span class="sxs-lookup"><span data-stu-id="7873d-113">Unless otherwise explicitly noted, objects MUST NOT have additional properties beyond those specified explicitly in this document.</span></span>

## <a name="additional-definitions"></a><span data-ttu-id="7873d-114">Definições Adicionais</span><span class="sxs-lookup"><span data-stu-id="7873d-114">Additional Definitions</span></span> ##

<span data-ttu-id="7873d-115">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="7873d-115">This section is normative.</span></span>

### <a name="quantity-objects"></a><span data-ttu-id="7873d-116">Quantidade de objetos</span><span class="sxs-lookup"><span data-stu-id="7873d-116">Quantity Objects</span></span> ###

<span data-ttu-id="7873d-117">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="7873d-117">This section is normative.</span></span>

<span data-ttu-id="7873d-118">Um _objeto Quantity_ é um objeto JSON e deve ter uma propriedade `units` cujo valor é um dos valores permitidos listados na tabela 1.</span><span class="sxs-lookup"><span data-stu-id="7873d-118">A _quantity object_ is a JSON object, and MUST have a property `units` whose value is one of the allowed values listed in Table 1.</span></span>

<span data-ttu-id="7873d-119">Um objeto de quantidade é um _objeto de quantidade simples_ se tiver uma única propriedade `value` além de sua propriedade `units`.</span><span class="sxs-lookup"><span data-stu-id="7873d-119">A quantity object is a _simple quantity object_ if it has a single property `value` in addition to its `units` property.</span></span>
<span data-ttu-id="7873d-120">O valor da propriedade `value` deve ser um número.</span><span class="sxs-lookup"><span data-stu-id="7873d-120">The value of the `value` property MUST be a number.</span></span>

<span data-ttu-id="7873d-121">Um objeto Quantity é um _objeto de quantidade vinculada_ se tiver as propriedades `lower` e `upper` além de sua propriedade `units`.</span><span class="sxs-lookup"><span data-stu-id="7873d-121">A quantity object is a _bounded quantity object_ if it has the properties `lower` and `upper` in addition to its `units` property.</span></span>
<span data-ttu-id="7873d-122">Os valores das propriedades `lower` e `upper` devem ser números.</span><span class="sxs-lookup"><span data-stu-id="7873d-122">The values of the `lower` and `upper` properties MUST be numbers.</span></span>
<span data-ttu-id="7873d-123">Um objeto de quantidade associada pode ter uma propriedade `value` cujo valor é um número.</span><span class="sxs-lookup"><span data-stu-id="7873d-123">A bounded quantity object MAY have a property `value` whose value is a number.</span></span>

<span data-ttu-id="7873d-124">Um objeto Quantity é um _objeto de quantidade de matriz esparsa_ se tiver a propriedade `format` e uma propriedade `values` além de sua propriedade `units`.</span><span class="sxs-lookup"><span data-stu-id="7873d-124">A quantity object is a _sparse array quantity object_ if it has the property `format` and a property `values` in addition to its `units` property.</span></span>
<span data-ttu-id="7873d-125">O valor de `format` deve ser a cadeia de caracteres `sparse`.</span><span class="sxs-lookup"><span data-stu-id="7873d-125">The value of `format` MUST be the string `sparse`.</span></span>
<span data-ttu-id="7873d-126">O valor da propriedade `values` deve ser uma matriz.</span><span class="sxs-lookup"><span data-stu-id="7873d-126">The value of the `values` property MUST be an array.</span></span>
<span data-ttu-id="7873d-127">Cada elemento de `values` deve ser uma matriz que representa os índices e o valor da quantidade de matriz esparsa.</span><span class="sxs-lookup"><span data-stu-id="7873d-127">Each element of `values` MUST be an array representing the indices and value of the sparse array quantity.</span></span>

<span data-ttu-id="7873d-128">Os índices para cada elemento de um objeto de quantidade de matriz esparsa devem ser exclusivos em todo o objeto de quantidade de matriz esparsa.</span><span class="sxs-lookup"><span data-stu-id="7873d-128">The indices for each element of a sparse array quantity object MUST be unique across the entire sparse array quantity object.</span></span>
<span data-ttu-id="7873d-129">Se um índice estiver presente com um valor de `0`, um analisador deverá tratar o objeto de quantidade de matriz esparsa de forma idêntica a um objeto de quantidade de matriz esparsa no qual esse índice não está presente.</span><span class="sxs-lookup"><span data-stu-id="7873d-129">If an index is present with a value of `0`, a parser MUST treat the sparse array quantity object identically to a sparse array quantity object in which that index is not present at all.</span></span>


<span data-ttu-id="7873d-130">Um objeto de quantidade deve ser</span><span class="sxs-lookup"><span data-stu-id="7873d-130">A quantity object MUST either be</span></span>

- <span data-ttu-id="7873d-131">um objeto de quantidade simples,</span><span class="sxs-lookup"><span data-stu-id="7873d-131">a simple quantity object,</span></span>
- <span data-ttu-id="7873d-132">um objeto de quantidade vinculada ou</span><span class="sxs-lookup"><span data-stu-id="7873d-132">a bounded quantity object, or</span></span>
- <span data-ttu-id="7873d-133">um objeto de quantidade de matriz esparsa.</span><span class="sxs-lookup"><span data-stu-id="7873d-133">a sparse array quantity object.</span></span>


### <a name="examples"></a><span data-ttu-id="7873d-134">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7873d-134">Examples</span></span> ###

<span data-ttu-id="7873d-135">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="7873d-135">This section is informative.</span></span>

<span data-ttu-id="7873d-136">Uma quantidade simples representando $1.9844146837\,\mathrm{Ha} $:</span><span class="sxs-lookup"><span data-stu-id="7873d-136">A simple quantity representing $1.9844146837\,\mathrm{Ha}$:</span></span>

```yaml
coulomb_repulsion:
    value: 1.9844146837
    units: hartree
```

<span data-ttu-id="7873d-137">Uma quantidade limitada que representa uma distribuição uniforme sobre o intervalo $ [-7,-6]\,\mathrm{Ha} $:</span><span class="sxs-lookup"><span data-stu-id="7873d-137">A bounded quantity representing a uniform distribution over the interval $[-7, -6]\,\mathrm{Ha}$:</span></span>

```yaml
fci_energy:
    upper: -6
    lower: -7
    units: hartree
```

<span data-ttu-id="7873d-138">A seguir está uma quantidade de matriz esparsa com um elemento `[1, 2]` igual a `hello` e um elemento `[3, 4]` igual a `world`:</span><span class="sxs-lookup"><span data-stu-id="7873d-138">The following is a sparse array quantity with an element `[1, 2]` equal to `hello` and an element `[3, 4]` equal to `world`:</span></span>

```yaml
sparse_example:
    format: sparse
    units: hartree
    values:
    - [1, 2, "hello"]
    - [3, 4, "world"]
```

## <a name="format-section"></a><span data-ttu-id="7873d-139">Seção de formato</span><span class="sxs-lookup"><span data-stu-id="7873d-139">Format Section</span></span> ##

<span data-ttu-id="7873d-140">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="7873d-140">This section is normative.</span></span>

<span data-ttu-id="7873d-141">O objeto Broombridge deve ter uma propriedade `format` cujo valor é um objeto JSON com uma propriedade chamada `version`.</span><span class="sxs-lookup"><span data-stu-id="7873d-141">The Broombridge object MUST have a property `format` whose value is a JSON object with one property called `version`.</span></span>
<span data-ttu-id="7873d-142">A propriedade `version` deve ter o valor `"0.2"`.</span><span class="sxs-lookup"><span data-stu-id="7873d-142">The `version` property MUST have the value `"0.2"`.</span></span>

### <a name="example"></a><span data-ttu-id="7873d-143">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7873d-143">Example</span></span> ###

<span data-ttu-id="7873d-144">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="7873d-144">This section is informative.</span></span>

```yaml
format:                        # required
    version: "0.2"             # must match exactly
```

## <a name="problem-description-section"></a><span data-ttu-id="7873d-145">Seção Descrição do problema</span><span class="sxs-lookup"><span data-stu-id="7873d-145">Problem Description Section</span></span> ##

<span data-ttu-id="7873d-146">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="7873d-146">This section is normative.</span></span>

<span data-ttu-id="7873d-147">O objeto Broombridge deve ter uma propriedade `problem_description` cujo valor é uma matriz JSON.</span><span class="sxs-lookup"><span data-stu-id="7873d-147">The Broombridge object MUST have a property `problem_description` whose value is a JSON array.</span></span>
<span data-ttu-id="7873d-148">Cada item no valor da propriedade `problem_description` deve ser um objeto JSON que descreve um conjunto de integrais, conforme descrito no restante desta seção.</span><span class="sxs-lookup"><span data-stu-id="7873d-148">Each item in the value of the `problem_description` property MUST be a JSON object describing one set of integrals, as described in the remainder of this section.</span></span>
<span data-ttu-id="7873d-149">No restante desta seção, o termo "objeto de descrição do problema" fará referência a um item no valor da propriedade `problem_description` do objeto Broombridge.</span><span class="sxs-lookup"><span data-stu-id="7873d-149">In the remainder of this section, the term "problem description object" will refer to an item in the value of the `problem_description` property of the Broombridge object.</span></span>

<span data-ttu-id="7873d-150">Cada objeto de descrição do problema deve ter uma propriedade `metadata` cujo valor é um objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="7873d-150">Each problem description object MUST have a property `metadata` whose value is a JSON object.</span></span>
<span data-ttu-id="7873d-151">O valor de `metadata` pode ser o objeto JSON vazio (ou seja, `{}`) ou pode conter propriedades adicionais definidas pelo implementador.</span><span class="sxs-lookup"><span data-stu-id="7873d-151">The value of `metadata` MAY be the empty JSON object (that is, `{}`), or MAY contain additional properties defined by the implementor.</span></span>

### <a name="hamiltonian-section"></a><span data-ttu-id="7873d-152">Seção Hamiltonian</span><span class="sxs-lookup"><span data-stu-id="7873d-152">Hamiltonian Section</span></span> ###

#### <a name="overview"></a><span data-ttu-id="7873d-153">Visão Geral</span><span class="sxs-lookup"><span data-stu-id="7873d-153">Overview</span></span> ####

<span data-ttu-id="7873d-154">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="7873d-154">This section is informative.</span></span>

<span data-ttu-id="7873d-155">A propriedade `hamiltonian` de cada objeto de descrição do problema descreve o Hamiltonian para um problema de química do Quantum específico, listando seus termos de um e dois corpo como matrizes esparsas de números reais.</span><span class="sxs-lookup"><span data-stu-id="7873d-155">The `hamiltonian` property of each problem description object describes the Hamiltonian for a particular quantum chemistry problem by listing out its one- and two-body terms as sparse arrays of real numbers.</span></span>
<span data-ttu-id="7873d-156">Os operadores de Hamiltonian descritos por cada objeto de descrição de problema assumem o formulário</span><span class="sxs-lookup"><span data-stu-id="7873d-156">The Hamiltonian operators described by each problem description object take the form</span></span>

<span data-ttu-id="7873d-157">$ $ H = \sum\_\{i, j\}\sum\_{\sigma\in\\{\uparrow, \downarrow\\}} H\_\{IJ\} a ^\{\dagger\}\_{i , \sigma} a\_{j, \sigma} + \frac{1}{2}\sum\_\{i, j, k, l\}\sum\_{\sigma, \rho\in\\{\uparrow, \downarrow\\}} h\_{ijkl} a ^ \dagger\_{i , \sigma} a ^ \dagger\_{k, \rho} a\_{l, \rho} a\_{j, \sigma}, $ $</span><span class="sxs-lookup"><span data-stu-id="7873d-157">$$ H = \sum\_\{i,j\}\sum\_{\sigma\in\\{\uparrow,\downarrow\\}} h\_\{ij\} a^\{\dagger\}\_{i,\sigma} a\_{j,\sigma} + \frac{1}{2}\sum\_\{i,j,k,l\}\sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}} h\_{ijkl} a^\dagger\_{i,\sigma} a^\dagger\_{k,\rho} a\_{l,\rho} a\_{j,\sigma}, $$</span></span>

<span data-ttu-id="7873d-158">Aqui $h _ {ijkl} = (IJ | KL) $ na Convenção Mulliken.</span><span class="sxs-lookup"><span data-stu-id="7873d-158">here $h_{ijkl}= (ij|kl)$ in Mulliken convention.</span></span>

<span data-ttu-id="7873d-159">Para maior clareza, o termo One-at é</span><span class="sxs-lookup"><span data-stu-id="7873d-159">For clarity, the one-electron term is</span></span>

<span data-ttu-id="7873d-160">$ $ h_ {IJ} = \int {\mathrm d} x \psi ^ \*\_i (x) \left (\frac{1}{2}\nabla ^ 2 + \sum\_{A} \frac{Z\_A} {| x-x\_A |}  \right) \psi\_j (x), $ $</span><span class="sxs-lookup"><span data-stu-id="7873d-160">$$ h_{ij} = \int {\mathrm d}x \psi^\*\_i(x) \left(\frac{1}{2}\nabla^2 + \sum\_{A}\frac{Z\_A}{|x-x\_A|}  \right) \psi\_j(x), $$</span></span>

<span data-ttu-id="7873d-161">e o termo de duas-bits é</span><span class="sxs-lookup"><span data-stu-id="7873d-161">and the two-electron term is</span></span>

<span data-ttu-id="7873d-162">$ $ h\_\{ijkl\} = \iint \{\mathrm d\}x ^ 2 \psi ^\{\*\}\_i (x\_1) \psi\_j (x\_1) \frac\{1\}\{\|x\_1-x\_2\|\}\psi\_k ^\{\*\}(x\_2) \psi\_l (x\_2).</span><span class="sxs-lookup"><span data-stu-id="7873d-162">$$ h\_\{ijkl\} = \iint \{\mathrm d\}x^2 \psi^\{\*\}\_i(x\_1)\psi\_j(x\_1) \frac\{1\}\{\|x\_1 -x\_2\|\}\psi\_k^\{\*\}(x\_2) \psi\_l(x\_2).</span></span>
$$

<span data-ttu-id="7873d-163">Conforme observado em nossa descrição da [propriedade`basis_set`](#basis-set-object) de cada elemento da propriedade `integral_sets`, declaromos mais explicitamente que as funções de base usadas são de valor real.</span><span class="sxs-lookup"><span data-stu-id="7873d-163">As noted in our description of the [`basis_set` property](#basis-set-object) of each element of the `integral_sets` property, we further explicitly assume that the basis functions used are real-valued.</span></span>
<span data-ttu-id="7873d-164">Isso nos permite usar os seguintes Symmetries entre os termos para compactar a representação do Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="7873d-164">This allows us to use the following symmetries between the terms to compress the representation of the Hamiltonian.</span></span>

<span data-ttu-id="7873d-165">$ $ h_ {ijkl} = h_ {Ijlk} = h_ {jikl} = h_ {jilk} = h_ {klij} = h_ {klji} = h_ {lkij} = h_ {LKJI}.</span><span class="sxs-lookup"><span data-stu-id="7873d-165">$$ h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkij}=h_{lkji}.</span></span>
$$


#### <a name="contents"></a><span data-ttu-id="7873d-166">Conteúdo</span><span class="sxs-lookup"><span data-stu-id="7873d-166">Contents</span></span> ####

<span data-ttu-id="7873d-167">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="7873d-167">This section is normative.</span></span>

<span data-ttu-id="7873d-168">Cada objeto de descrição do problema deve ter uma propriedade `hamiltonian` cujo valor é um objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="7873d-168">Each problem description object MUST have a property `hamiltonian` whose value is a JSON object.</span></span>
<span data-ttu-id="7873d-169">O valor da propriedade `hamiltonian` é conhecido como um objeto Hamiltonian e deve ter as propriedades `one_electron_integrals` e `two_electron_integrals` conforme descrito no restante desta seção.</span><span class="sxs-lookup"><span data-stu-id="7873d-169">The value of the `hamiltonian` property is known as a Hamiltonian object, and MUST have the properties `one_electron_integrals` and `two_electron_integrals` as described in the remainder of this section.</span></span>

<span data-ttu-id="7873d-170">Cada objeto de descrição do problema deve ter uma propriedade `coulomb_repulsion` cujo valor é um objeto de quantidade simples.</span><span class="sxs-lookup"><span data-stu-id="7873d-170">Each problem description object MUST have a property `coulomb_repulsion` whose value is a simple quantity object.</span></span>
<span data-ttu-id="7873d-171">Cada objeto de descrição do problema deve ter uma propriedade `energy_offet` cujo valor é um objeto de quantidade simples.</span><span class="sxs-lookup"><span data-stu-id="7873d-171">Each problem description object MUST have a property `energy_offet` whose value is a simple quantity object.</span></span>
> <span data-ttu-id="7873d-172">ANOTAÇÕES Os valores de `coulomb_repulsion` e `energy_offet` adicionados juntos capturam o termo de identidade do Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="7873d-172">[NOTE] The values of `coulomb_repulsion` and `energy_offet` added together capture the identity term of the Hamiltonian.</span></span>

##### <a name="one-electron-integrals-object"></a><span data-ttu-id="7873d-173">Objeto de integral de um único-</span><span class="sxs-lookup"><span data-stu-id="7873d-173">One-Electron Integrals Object</span></span> #####

<span data-ttu-id="7873d-174">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="7873d-174">This section is normative.</span></span>

<span data-ttu-id="7873d-175">A propriedade `one_electron_integrals` do objeto Hamiltonian deve ser uma quantidade de matriz esparsa cujos índices são dois inteiros e cujos valores são números.</span><span class="sxs-lookup"><span data-stu-id="7873d-175">The `one_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity whose indices are two integers and whose values are numbers.</span></span>
<span data-ttu-id="7873d-176">Cada termo deve ter índices `[i, j]` onde `i >= j`.</span><span class="sxs-lookup"><span data-stu-id="7873d-176">Every term MUST have indices `[i, j]` where `i >= j`.</span></span>

> <span data-ttu-id="7873d-177">ANOTAÇÕES Isso reflete a simetria de que $h _ {IJ} = h_ {ji} $, que é uma conseqüência do fato de que o Hamiltonian é Hermitian.</span><span class="sxs-lookup"><span data-stu-id="7873d-177">[NOTE] This reflects the symmetry that $h_{ij} = h_{ji}$ which is a consequence of the fact that the Hamiltonian is Hermitian.</span></span>


###### <a name="example"></a><span data-ttu-id="7873d-178">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7873d-178">Example</span></span> ######

<span data-ttu-id="7873d-179">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="7873d-179">This section is informative.</span></span>

<span data-ttu-id="7873d-180">A quantidade de matriz esparsa a seguir representa o Hamiltonian $ $ H = \left (-5,0 (a ^\{\dagger\}\_{1, \uparrow} a\_{1, \uparrow} + a ^\{\dagger\}\_{1, \downarrow} a\_{1 , \downarrow}) + 0,17 (^\{\dagger\}\_{2, \uparrow} a\_{1, \uparrow} + a ^\{\dagger\}\_{1, \uparrow} a\_{2, \uparrow} + a ^\{\dagger\}\_{2 , \downarrow} a\_{1, \downarrow} + a ^\{\dagger\}\_{1, \downarrow} a\_{2, \downarrow}) \right)\\, \mathrm{Ha}.</span><span class="sxs-lookup"><span data-stu-id="7873d-180">The following sparse array quantity represents the Hamiltonian $$ H = \left(-5.0  (a^\{\dagger\}\_{1,\uparrow} a\_{1,\uparrow}+a^\{\dagger\}\_{1,\downarrow} a\_{1,\downarrow})+ 0.17 (a^\{\dagger\}\_{2,\uparrow} a\_{1,\uparrow}+ a^\{\dagger\}\_{1,\uparrow} a\_{2,\uparrow}+a^\{\dagger\}\_{2,\downarrow} a\_{1,\downarrow}+ a^\{\dagger\}\_{1,\downarrow} a\_{2,\downarrow})\right)\\,\mathrm{Ha}.</span></span>
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
> <span data-ttu-id="7873d-181">Broombridge usa indexação com base em 1.</span><span class="sxs-lookup"><span data-stu-id="7873d-181">Broombridge uses 1-based indexing.</span></span>


##### <a name="two-electron-integrals-object"></a><span data-ttu-id="7873d-182">Objeto de integral de dois bits</span><span class="sxs-lookup"><span data-stu-id="7873d-182">Two-Electron Integrals Object</span></span> #####

<span data-ttu-id="7873d-183">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="7873d-183">This section is normative.</span></span>

<span data-ttu-id="7873d-184">A propriedade `two_electron_integrals` do objeto Hamiltonian deve ser uma quantidade de matriz esparsa com uma propriedade adicional chamada `index_convention`.</span><span class="sxs-lookup"><span data-stu-id="7873d-184">The `two_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity with one additional property called `index_convention`.</span></span>
<span data-ttu-id="7873d-185">Cada elemento do valor de `two_electron_integrals` deve ter quatro índices.</span><span class="sxs-lookup"><span data-stu-id="7873d-185">Each element of the value of `two_electron_integrals` MUST have four indices.</span></span>

<span data-ttu-id="7873d-186">Cada propriedade de `two_electron_integrals` deve ter uma propriedade `index_convention`.</span><span class="sxs-lookup"><span data-stu-id="7873d-186">Each `two_electron_integrals` property MUST have a `index_convention` property.</span></span>
<span data-ttu-id="7873d-187">O valor da propriedade `index_convention` deve ser um dos valores permitidos listados na tabela 1.</span><span class="sxs-lookup"><span data-stu-id="7873d-187">The value of the `index_convention` property MUST be one of the allowed values listed in Table 1.</span></span>
<span data-ttu-id="7873d-188">Se o valor de `index_convention` for `mulliken`, para cada elemento da quantidade de matriz esparsa de `two_electron_integrals`, um analisador que carrega um documento Broombridge deve criar uma instância de um termo Hamiltonian igual ao operador de dois bits $h _ {i, j, k, l} a ^ \dagger_i a ^ \dagger_j a_k A_L $ , em que $i $, $j $, $k $ e $l $ devem ser inteiros de valor pelo menos 1 e em que $h _ {i, j, k, l} $ é o elemento `[i, j, k, l, h(i, j, k, l)]` da quantidade de matriz esparsa.</span><span class="sxs-lookup"><span data-stu-id="7873d-188">If the value of `index_convention` is `mulliken`, then for each element of the `two_electron_integrals` sparse array quantity, a parser loading a Broombridge document MUST instantiate a Hamiltonian term equal to the two-electron operator $h_{i, j, k, l} a^\dagger_i a^\dagger_j a_k a_l$, where $i$, $j$, $k$, and $l$ MUST be integers of value at least 1, and where $h_{i, j, k, l}$ is the element `[i, j, k, l, h(i, j, k, l)]` of the sparse array quantity.</span></span>

###### <a name="symmetries"></a><span data-ttu-id="7873d-189">Symmetries</span><span class="sxs-lookup"><span data-stu-id="7873d-189">Symmetries</span></span> ######

<span data-ttu-id="7873d-190">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="7873d-190">This section is normative.</span></span>

<span data-ttu-id="7873d-191">Se a propriedade `index_convention` de um objeto `two_electron_integrals` for igual a `mulliken`, se um elemento com índices `[i, j, k, l]` estiver presente, os índices a seguir não deverão estar presentes, a menos que sejam iguais a `[i, j, k, l]`:</span><span class="sxs-lookup"><span data-stu-id="7873d-191">If the `index_convention` property of a `two_electron_integrals` object is equal to `mulliken`, then if an element with indices `[i, j, k, l]` is present, the following indices MUST NOT be present unless they are equal to `[i, j, k, l]`:</span></span>

- `[i, j, l, k]`
- `[j, i, k, l]`
- `[j, i, l, k]`
- `[k, l, i, j]`
- `[k, l, j, i]`
- `[l, k, j, i]`

> [!NOTE]
> <span data-ttu-id="7873d-192">Como a propriedade `index_convention` é um objeto de quantidade esparsa, nenhum índice pode ser repetido em elementos diferentes.</span><span class="sxs-lookup"><span data-stu-id="7873d-192">Because the `index_convention` property is a sparse quantity object, no indices may be repeated on different elements.</span></span>
> <span data-ttu-id="7873d-193">Em particular, se um elemento com índices `[i, j, k, l]` estiver presente, nenhum outro elemento poderá ter esses índices.</span><span class="sxs-lookup"><span data-stu-id="7873d-193">In particular, if an element with indices `[i, j, k, l]` is present, no other element may have those indices.</span></span>


<!-- h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkji}. -->

###### <a name="example"></a><span data-ttu-id="7873d-194">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7873d-194">Example</span></span> #######

<span data-ttu-id="7873d-195">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="7873d-195">This section is informative.</span></span>

<span data-ttu-id="7873d-196">O objeto a seguir especifica o Hamiltonian</span><span class="sxs-lookup"><span data-stu-id="7873d-196">The following object specifies the Hamiltonian</span></span>

<span data-ttu-id="7873d-197">$ $ H = \frac12 \sum\_{\sigma, \rho\in\\{\uparrow, \downarrow\\}} \Biggr (1,6 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_{1, \rho} a\_{1, \rho} a\_{1, \sigma}-0,1 a ^ {\dagger}\_{6 , \sigma} a ^ {\dagger}\_{1, \rho} a\_{3, \rho} a\_{2, \sigma}-0,1 a ^ {\dagger}\_{6, \sigma} a ^ {\dagger}\_{1, \rho} a\_{2, \rho} a\_{3 , \sigma}-0,1 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_{6, \rho} a\_{3, \rho} a\_{2, \sigma}-0,1 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_{6, \rho} a\_{2 , \rho} a\_{3, \sigma} $ $ $ $-0,1 a ^ {\dagger}\_{3, \sigma} a ^ {\dagger}\_{2, \rho} a\_{6, \rho} a\_{1, \sigma}-0,1 a ^ {\dagger}\_{3, \sigma} a ^ {\dagger}\_{2 , \rho} a\_{1, \rho} a\_{6, \sigma}-0,1 a ^ {\dagger}\_{2, \sigma} a ^ {\dagger}\_{3, \rho} a\_{6, \rho} a\_{1, \sigma}-0,1 a ^ {\dagger}\_{2 , \sigma} a ^ {\dagger}\_{3, \rho} a\_{1, \rho} a\_{6, \sigma}\Biggr)\\, \textrm{Ha}.</span><span class="sxs-lookup"><span data-stu-id="7873d-197">$$ H = \frac12 \sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}}\Biggr( 1.6 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{1,\rho} a\_{1,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{2,\rho} a\_{3,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{2,\rho} a\_{3,\sigma} $$ $$- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{1,\rho} a\_{6,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{1,\rho} a\_{6,\sigma}\Biggr)\\,\textrm{Ha}.</span></span>
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

### <a name="initial-state-section"></a><span data-ttu-id="7873d-198">Seção de estado inicial</span><span class="sxs-lookup"><span data-stu-id="7873d-198">Initial State Section</span></span> ###

<span data-ttu-id="7873d-199">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="7873d-199">This section is normative.</span></span>

<span data-ttu-id="7873d-200">O objeto `initial_state_suggestion` cujo valor é uma matriz JSON especifica os Estados de Quantum inicial de interesse para o Hamiltonian especificado.</span><span class="sxs-lookup"><span data-stu-id="7873d-200">The `initial_state_suggestion` object whose value is a JSON array specifies initial quantum states of interest to the specified Hamiltonian.</span></span> <span data-ttu-id="7873d-201">Cada item no valor da propriedade `initial_state_suggestion` deve ser um objeto JSON que descreve um estado Quantum, conforme descrito no restante desta seção.</span><span class="sxs-lookup"><span data-stu-id="7873d-201">Each item in the value of the `initial_state_suggestion` property MUST be a JSON object describing one quantum state, as described in the remainder of this section.</span></span>
<span data-ttu-id="7873d-202">No restante desta seção, o termo "objeto de estado" fará referência a um item no valor da propriedade `initial_state_suggestion` do objeto Broombridge.</span><span class="sxs-lookup"><span data-stu-id="7873d-202">In the remainder of this section, the term "state object" will refer to an item in the value of the `initial_state_suggestion` property of the Broombridge object.</span></span>

#### <a name="state-object"></a><span data-ttu-id="7873d-203">Objeto de estado</span><span class="sxs-lookup"><span data-stu-id="7873d-203">State object</span></span> ####

<span data-ttu-id="7873d-204">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="7873d-204">This section is normative.</span></span>

<span data-ttu-id="7873d-205">Cada objeto de Estado deve ter uma propriedade `label` contendo uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7873d-205">Each state object MUST have a `label` property containing a string.</span></span> <span data-ttu-id="7873d-206">Cada objeto de Estado deve ter uma propriedade `method`.</span><span class="sxs-lookup"><span data-stu-id="7873d-206">Each state object MUST have a `method` property.</span></span> <span data-ttu-id="7873d-207">O valor da propriedade `method` deve ser um dos valores permitidos listados na tabela 3.</span><span class="sxs-lookup"><span data-stu-id="7873d-207">The value of the `method` property MUST be one of the allowed values listed in Table 3.</span></span>
<span data-ttu-id="7873d-208">Cada objeto de estado pode ter uma propriedade `energy` cujo valor deve ser um objeto de quantidade simples.</span><span class="sxs-lookup"><span data-stu-id="7873d-208">Each state object MAY have a property `energy` whose value MUST be a simple quantity object.</span></span>

<span data-ttu-id="7873d-209">Se o valor da propriedade `method` for `sparse_multi_configurational`, o objeto de estado deverá ter uma propriedade `superposition` que contenha uma matriz de Estados de base e suas amplitudes não normalizadas.</span><span class="sxs-lookup"><span data-stu-id="7873d-209">If the value of the `method` property is `sparse_multi_configurational`, the state object MUST have a `superposition` property containing an array of basis states and their unnormalized amplitudes.</span></span>

<span data-ttu-id="7873d-210">Por exemplo, os Estados iniciais $ $ \ket{G0} = \ket{G1} = \ket{G2} = (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) \ket{0} $ $ $ $ \ket{E} = \frac{0.1 (a ^ {\dagger}\_{1 , \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) + 0.2 (^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{3, \uparrow}a ^ {\dagger}\_{2, \downarrow})} {\sqrt{| 0,1 | ^ 2 + | 0.2 | ^ 2}} \ket{0}, $ $, em que $ \ket{E} $ tem Energy $0.987 \textrm{Ha} $, são representados por</span><span class="sxs-lookup"><span data-stu-id="7873d-210">For example, the initial states $$ \ket{G0}=\ket{G1}=\ket{G2}=(a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})\ket{0} $$ $$ \ket{E}=\frac{0.1 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})+0.2 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{3,\uparrow}a^{\dagger}\_{2,\downarrow})}{\sqrt{|0.1|^2+|0.2|^2}}\ket{0}, $$ where $\ket{E}$ has energy $0.987 \textrm{Ha}$, are represented by</span></span>
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

<span data-ttu-id="7873d-211">Se o valor da propriedade `method` for `unitary_coupled_cluster`, o objeto de estado deverá ter uma propriedade `cluster_operator` cujo valor é um objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="7873d-211">If the value of the `method` property is `unitary_coupled_cluster`, the state object MUST have a `cluster_operator` property whose value is a JSON object.</span></span>
<span data-ttu-id="7873d-212">O objeto JSON deve ter uma propriedade `reference_state` cujo valor é um estado base.</span><span class="sxs-lookup"><span data-stu-id="7873d-212">The JSON object MUST have a `reference_state` property whose value is a basis state.</span></span>
<span data-ttu-id="7873d-213">O objeto JSON pode ter uma propriedade `one_body_amplitudes` cujo valor é uma matriz de operadores de cluster de um corpo e suas amplitudes.</span><span class="sxs-lookup"><span data-stu-id="7873d-213">The JSON object MAY have a `one_body_amplitudes` property whose value is an array of one-body cluster operators and their amplitudes.</span></span>
<span data-ttu-id="7873d-214">O objeto JSON pode ter uma propriedade `two_body_amplitudes` cujo valor é uma matriz de operadores de cluster de dois corpo e suas amplitudes.</span><span class="sxs-lookup"><span data-stu-id="7873d-214">The JSON object MAY have a `two_body_amplitudes` property whose value is an array of two-body cluster operators and their amplitudes.</span></span>
<span data-ttu-id="7873d-215">que contém uma matriz de Estados de base e suas amplitudes não normalizadas.</span><span class="sxs-lookup"><span data-stu-id="7873d-215">containing an array of basis states and their unnormalized amplitudes.</span></span>

<span data-ttu-id="7873d-216">Por exemplo, o estado $ $ \ket{\Text{Reference}} = (um ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) \ket{0}, $ $</span><span class="sxs-lookup"><span data-stu-id="7873d-216">For example, the state $$ \ket{\text{reference}}=(a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})\ket{0}, $$</span></span>

<span data-ttu-id="7873d-217">$ $ \ket{\text{UCCSD}} = e ^ {T-T ^ \dagger}\ket{\Text{Reference}}, $ $</span><span class="sxs-lookup"><span data-stu-id="7873d-217">$$ \ket{\text{UCCSD}}=e^{T-T^\dagger}\ket{\text{reference}}, $$</span></span>

<span data-ttu-id="7873d-218">$ $ T = 0,1 a ^ {\dagger}\_{3, \uparrow}a\_{2, \downarrow} + 0,2 a ^ {\dagger}\_{2, \uparrow}a\_{2, \downarrow}-0,3 a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{3, \downarrow}a\_{3 , \uparrow}a\_{2, \downarrow} $ $ é representado por</span><span class="sxs-lookup"><span data-stu-id="7873d-218">$$ T = 0.1 a^{\dagger}\_{3,\uparrow}a\_{2,\downarrow} + 0.2 a^{\dagger}\_{2,\uparrow}a\_{2,\downarrow} - 0.3 a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{3,\downarrow}a\_{3,\uparrow}a\_{2,\downarrow} $$ is represented by</span></span>
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

#### <a name="basis-set-object"></a><span data-ttu-id="7873d-219">Objeto de conjunto base</span><span class="sxs-lookup"><span data-stu-id="7873d-219">Basis Set Object</span></span> ####

<span data-ttu-id="7873d-220">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="7873d-220">This section is normative.</span></span>

<span data-ttu-id="7873d-221">Cada objeto de descrição do problema pode ter uma propriedade `basis_set`.</span><span class="sxs-lookup"><span data-stu-id="7873d-221">Each problem description object MAY have a `basis_set` property.</span></span>
<span data-ttu-id="7873d-222">Se houver, o valor da propriedade `basis_set` deve ser um objeto com duas propriedades, `type` e `name`.</span><span class="sxs-lookup"><span data-stu-id="7873d-222">If present, the value of the `basis_set` property MUST be an object with two properties, `type` and `name`.</span></span>

<span data-ttu-id="7873d-223">As funções base identificadas pelo valor da propriedade `basis_set` devem ser de valor real.</span><span class="sxs-lookup"><span data-stu-id="7873d-223">The basis functions identified by the value of the `basis_set` property MUST be real-valued.</span></span>

> [!NOTE]
> <span data-ttu-id="7873d-224">A suposição de que todas as funções de base tenham valor real pode ser reduzida em versões futuras desta especificação.</span><span class="sxs-lookup"><span data-stu-id="7873d-224">The assumption that all basis functions are real-valued may be relaxed in future versions of this specification.</span></span>

## <a name="tables-and-lists"></a><span data-ttu-id="7873d-225">Tabelas e listas</span><span class="sxs-lookup"><span data-stu-id="7873d-225">Tables and Lists</span></span> ##

### <a name="table-1-allowed-physical-units"></a><span data-ttu-id="7873d-226">Tabela 1.</span><span class="sxs-lookup"><span data-stu-id="7873d-226">Table 1.</span></span> <span data-ttu-id="7873d-227">Unidades físicas permitidas</span><span class="sxs-lookup"><span data-stu-id="7873d-227">Allowed Physical Units</span></span> ###

<span data-ttu-id="7873d-228">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="7873d-228">This section is normative.</span></span>

<span data-ttu-id="7873d-229">Qualquer cadeia de caracteres especificando uma unidade deve ser uma das seguintes:</span><span class="sxs-lookup"><span data-stu-id="7873d-229">Any string specifying a unit MUST be one of the following:</span></span>

- `hartree`
- `ev`

<span data-ttu-id="7873d-230">Analisadores e produtores devem tratar os seguintes objetos de quantidade simples como equivalentes:</span><span class="sxs-lookup"><span data-stu-id="7873d-230">Parsers and producers MUST treat the following simple quantity objects as equivalent:</span></span>

```yaml
- {"units": "hartree", "value": 1}
- {"units": "ev", "value": 27.2113831301723}
```

### <a name="table-2-allowed-index-conventions"></a><span data-ttu-id="7873d-231">Tabela 2.</span><span class="sxs-lookup"><span data-stu-id="7873d-231">Table 2.</span></span> <span data-ttu-id="7873d-232">Convenções de índice permitidas</span><span class="sxs-lookup"><span data-stu-id="7873d-232">Allowed Index Conventions</span></span> ###

<span data-ttu-id="7873d-233">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="7873d-233">This section is normative.</span></span>

<span data-ttu-id="7873d-234">Qualquer cadeia de caracteres especificando uma Convenção de índice deve ser uma das seguintes:</span><span class="sxs-lookup"><span data-stu-id="7873d-234">Any string specifying an index convention MUST be one of the following:</span></span>

- `mulliken`

<span data-ttu-id="7873d-235">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="7873d-235">This section is informative.</span></span>

<span data-ttu-id="7873d-236">As convenções de índice adicionais podem ser introduzidas em versões futuras desta especificação.</span><span class="sxs-lookup"><span data-stu-id="7873d-236">Additional index conventions may be introduced in future versions of this specification.</span></span>

#### <a name="interpretation-of-index-conventions"></a><span data-ttu-id="7873d-237">Interpretação de convenções de índice</span><span class="sxs-lookup"><span data-stu-id="7873d-237">Interpretation of Index Conventions</span></span> ####

<span data-ttu-id="7873d-238">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="7873d-238">This section is informative.</span></span>

### <a name="table-3-allowed-state-methods"></a><span data-ttu-id="7873d-239">Tabela 3.</span><span class="sxs-lookup"><span data-stu-id="7873d-239">Table 3.</span></span> <span data-ttu-id="7873d-240">Métodos de estado permitidos</span><span class="sxs-lookup"><span data-stu-id="7873d-240">Allowed State methods</span></span> ###

<span data-ttu-id="7873d-241">Esta seção é normativas.</span><span class="sxs-lookup"><span data-stu-id="7873d-241">This section is normative.</span></span>

<span data-ttu-id="7873d-242">Qualquer cadeia de caracteres especificando um método de Estado deve ser uma das seguintes:</span><span class="sxs-lookup"><span data-stu-id="7873d-242">Any string specifying a state method MUST be one of the following:</span></span>

- `sparse_multi_configurational`
- `unitary_coupled_cluster`

<span data-ttu-id="7873d-243">Esta seção é informativa.</span><span class="sxs-lookup"><span data-stu-id="7873d-243">This section is informative.</span></span>

<span data-ttu-id="7873d-244">Métodos de estado adicionais podem ser introduzidos em versões futuras desta especificação.</span><span class="sxs-lookup"><span data-stu-id="7873d-244">Additional state methods may be introduced in future versions of this specification.</span></span>
