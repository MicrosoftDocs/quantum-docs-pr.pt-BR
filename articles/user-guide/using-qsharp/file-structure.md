---
title: 'Estrutura de arquivos de Q #'
description: 'Descreve a estrutura e a sintaxe de um arquivo Q #.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.filestructure
ms.openlocfilehash: b8c24dae6cc8d8f37ad4f1f74017c05cabe3a4b4
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327451"
---
# <a name="q-file-structure"></a><span data-ttu-id="8c2e2-103">Estrutura de arquivos de Q #</span><span class="sxs-lookup"><span data-stu-id="8c2e2-103">Q# File Structure</span></span>

<span data-ttu-id="8c2e2-104">Cada operação de Q #, função e tipo definido pelo usuário é definido em um namespace.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-104">Every Q# operation, function, and user-defined type is defined within a namespace.</span></span>

<span data-ttu-id="8c2e2-105">Um arquivo Q # consiste em uma sequência de *declarações de namespace*.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-105">A Q# file consists of a sequence of *namespace declarations*.</span></span>
<span data-ttu-id="8c2e2-106">Cada declaração de namespace contém declarações para tipos, operações e funções definidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-106">Each namespace declaration contains declarations for user-defined types, operations, and functions.</span></span>
<span data-ttu-id="8c2e2-107">Uma declaração de namespace pode conter qualquer número de cada tipo de declaração e em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-107">A namespace declaration may contain any number of each type of declaration, and in any order.</span></span>
<span data-ttu-id="8c2e2-108">Siga estes links para obter mais detalhes sobre como declarar tipos, [operações](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations)e [funções](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions) [definidas pelo usuário](xref:microsoft.quantum.guide.types#user-defined-types)em um namespace.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-108">Follow these links for more details on declaring [user-defined types](xref:microsoft.quantum.guide.types#user-defined-types), [operations](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations), and [functions](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions) within a namespace.</span></span>

<span data-ttu-id="8c2e2-109">O único texto que pode aparecer fora de uma declaração de namespace é comments.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-109">The only text that can appear outside of a namespace declaration is comments.</span></span>
<span data-ttu-id="8c2e2-110">Em particular, comentários de documentação (mais detalhes abaixo) para um namespace precedem a declaração.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-110">In particular, documentation comments (more details below) for a namespace precede the declaration.</span></span>

## <a name="namespace-declarations"></a><span data-ttu-id="8c2e2-111">Declarações de namespace</span><span class="sxs-lookup"><span data-stu-id="8c2e2-111">Namespace Declarations</span></span>

<span data-ttu-id="8c2e2-112">Um arquivo Q # normalmente terá exatamente uma declaração de namespace, mas pode ter nenhum (e estar vazio ou apenas conter comentários) ou pode conter vários namespaces.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-112">A Q# file will typically have exactly one namespace declaration, but may have none (and be empty or just contain comments) or may contain multiple namespaces.</span></span>
<span data-ttu-id="8c2e2-113">Declarações de namespace não podem ser aninhadas.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-113">Namespace declarations may not be nested.</span></span>

<span data-ttu-id="8c2e2-114">O mesmo namespace pode ser declarado em vários arquivos Q # que são compilados juntos, desde que não haja nenhuma declaração de tipo, operação ou função com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-114">The same namespace may be declared in multiple Q# files that are compiled together, as long as there are no type, operation, or function declarations with the same name.</span></span>
<span data-ttu-id="8c2e2-115">Em particular, é inválido definir o mesmo tipo no mesmo namespace em vários arquivos, mesmo que as declarações sejam idênticas.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-115">In particular, it is invalid to define the same type in the same namespace in multiple files, even if the declarations are identical.</span></span>

<span data-ttu-id="8c2e2-116">Uma declaração de namespace consiste na palavra-chave `namespace` , seguida pelo nome do namespace, uma chave de abertura `{` , as declarações contidas no namespace e uma chave de fechamento `}` .</span><span class="sxs-lookup"><span data-stu-id="8c2e2-116">A namespace declaration consists of the keyword `namespace`, followed by the name of the namespace, an open brace `{`, the declarations contained in the namespace, and a close brace `}`.</span></span>
<span data-ttu-id="8c2e2-117">Os nomes de namespace seguem o padrão .NET de uma sequência de um ou mais símbolos legais separados por pontos `.` .</span><span class="sxs-lookup"><span data-stu-id="8c2e2-117">Namespace names follow the .NET pattern of a sequence of one or more legal symbols separated by periods `.`.</span></span>
<span data-ttu-id="8c2e2-118">Por exemplo, `MyQuantumStuff` e `Microsoft.Quantum.Intrinsic` são nomes de namespace válidos.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-118">For instance, `MyQuantumStuff` and `Microsoft.Quantum.Intrinsic` are valid namespace names.</span></span>
<span data-ttu-id="8c2e2-119">Por convenção, os símbolos em um nome de namespace estão em letras maiúsculas, mas isso não é necessário.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-119">By convention, the symbols in a namespace name are capitalized, but this is not required.</span></span>

<span data-ttu-id="8c2e2-120">Referências a tipos ou chamadores declarados mais abaixo em um arquivo são resolvidos corretamente; Não há necessidade de tipo, operação ou declaração de função para preceder uma referência a ele.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-120">References to types or callables declared further down in a file are resolved properly; there is no need for the type, operation, or function declaration to precede a reference to it.</span></span>

## <a name="open-directives"></a><span data-ttu-id="8c2e2-121">Abrir diretivas</span><span class="sxs-lookup"><span data-stu-id="8c2e2-121">Open Directives</span></span>

<span data-ttu-id="8c2e2-122">Em um bloco de namespace, a `open` diretiva pode ser usada para importar todos os tipos e chamadores declarados em um determinado namespace e consultá-los por seu nome não qualificado.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-122">Within a namespace block, the `open` directive may be used to import all types and callables declared in a certain namespace and refer to them by their unqualified name.</span></span>
<span data-ttu-id="8c2e2-123">Essa `open` diretiva consiste na `open` palavra-chave, seguida pelo namespace a ser aberto e um ponto e vírgula de terminação.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-123">Such an `open` directive consists of the `open` keyword, followed by the namespace to be opened and a terminating semicolon.</span></span>

> [!NOTE] 
> <span data-ttu-id="8c2e2-124">Todas as `open` diretivas devem aparecer antes de qualquer `function` `operation` declaração, ou `newtype` no bloco de namespace.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-124">All `open` directives must appear before any `function`, `operation`, or `newtype` declarations in the namespace block.</span></span>

<span data-ttu-id="8c2e2-125">Opcionalmente, um nome curto para o namespace aberto pode ser definido de modo que todos os elementos desse namespace possam (e precisam) ser qualificados pelo nome curto definido.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-125">Optionally, a short name for the opened namespace may be defined such that all elements from that namespace can (and need) to be qualified by the defined short name.</span></span> <span data-ttu-id="8c2e2-126">Por exemplo, considerando a seguinte declaração de namespace e as diretivas abertas,</span><span class="sxs-lookup"><span data-stu-id="8c2e2-126">For example, given the following namespace declaration and open directives,</span></span>

```qsharp
namespace NS {
    open Microsoft.Quantum.Intrinsic; // opens the namespace
    open Microsoft.Quantum.Math as Math; // defines a short name for the namespace

    // operation, function, and newtype declarations

}
```

<span data-ttu-id="8c2e2-127">se uma operação que declararmos usar uma operação `Op` de `Microsoft.Quantum.Intrinsic` , nós a chamaremos simplesmente usando `Op` .</span><span class="sxs-lookup"><span data-stu-id="8c2e2-127">if an operation we declare uses an operation `Op` from `Microsoft.Quantum.Intrinsic`, we would call it by simply using `Op`.</span></span>
<span data-ttu-id="8c2e2-128">No entanto, se quiséssemos uma chamada a determinada função `Fn` `Microsoft.Quantum.Math` , precisaremos chamá-la usando `Math.Fn` .</span><span class="sxs-lookup"><span data-stu-id="8c2e2-128">However, if we wanted a call a certain function `Fn` from `Microsoft.Quantum.Math`, we would need to call it using `Math.Fn`.</span></span>

<span data-ttu-id="8c2e2-129">A `open` diretiva se aplica a todo o bloco de namespace dentro de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-129">The `open` directive applies to the entire namespace block within a file.</span></span>
<span data-ttu-id="8c2e2-130">Portanto, se tivéssemos de definir um namespace adicional no mesmo arquivo Q # como `NS` acima, quaisquer operações/funções/tipos definidos no segundo namespace não teriam acesso a nada de `Microsoft.Quantum.Intrinsic` ou `Microsoft.Quantum.Math` a menos que tenhamos repetido as diretivas abertas.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-130">Hence, if we were to define an additional namespace in the same Q# file as `NS` above, then any operations/functions/types defined in the second namespace would not have access to anything from `Microsoft.Quantum.Intrinsic` or `Microsoft.Quantum.Math` unless we repeated the open directives therein.</span></span> 

<span data-ttu-id="8c2e2-131">Um tipo ou callable definido em outro namespace que *não* está aberto no namespace atual deve ser referenciado por seu nome totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-131">A type or callable defined in another namespace that is *not* opened in the current namespace must be referenced by its fully-qualified name.</span></span>
<span data-ttu-id="8c2e2-132">Por exemplo, uma operação chamada `Op` do `X.Y` namespace deve ser referenciada por seu nome totalmente qualificado `X.Y.Op` , a menos que o `X.Y` namespace tenha sido aberto anteriormente no bloco atual.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-132">For example, an operation named `Op` from the `X.Y` namespace must be referenced by its fully-qualified name `X.Y.Op`, unless the `X.Y` namespace has been opened earlier in the current block.</span></span> <span data-ttu-id="8c2e2-133">Conforme mencionado acima, mesmo que o `X` namespace tenha sido aberto, não é possível fazer referência à operação como `Y.Op` .</span><span class="sxs-lookup"><span data-stu-id="8c2e2-133">As mentioned above, even if the `X` namespace has been opened, it is not possible to reference the operation as `Y.Op`.</span></span>
<span data-ttu-id="8c2e2-134">Se um nome curto `Z` para `X.Y` tiver sido definido nesse namespace e arquivo, `Op` o deverá ser referenciado como `Z.Op` .</span><span class="sxs-lookup"><span data-stu-id="8c2e2-134">If a short name `Z` for `X.Y` has been defined in that namespace and file, then `Op` needs to be referred to as `Z.Op`.</span></span> 

<span data-ttu-id="8c2e2-135">Geralmente, é melhor incluir um namespace usando uma `open` diretiva.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-135">It is usually better to include a namespace by using an `open` directive.</span></span>
<span data-ttu-id="8c2e2-136">Usar um nome totalmente qualificado é necessário se dois namespaces definem construções com o mesmo nome e a fonte atual usa construções de ambos.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-136">Using a fully-qualified name is required if two namespaces define constructs with the same name, and the current source uses constructs from both.</span></span>

<span data-ttu-id="8c2e2-137">O Q # segue as mesmas regras para nomear como outras linguagens .NET.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-137">Q# follows the same rules for naming as other .NET languages.</span></span>
<span data-ttu-id="8c2e2-138">No entanto, Q # não oferece suporte a referências relativas a namespaces.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-138">However, Q# does not support relative references to namespaces.</span></span>
<span data-ttu-id="8c2e2-139">Ou seja, se o namespace `a.b` tiver sido aberto, uma referência a uma operação chamada `c.d` *não* será resolvida para uma operação com o nome completo `a.b.c.d` .</span><span class="sxs-lookup"><span data-stu-id="8c2e2-139">That is, if the namespace `a.b` has been opened, a reference to an operation named `c.d` will *not* be resolved to an operation with full name `a.b.c.d`.</span></span>

## <a name="formatting"></a><span data-ttu-id="8c2e2-140">Formatação</span><span class="sxs-lookup"><span data-stu-id="8c2e2-140">Formatting</span></span>

<span data-ttu-id="8c2e2-141">A maioria das instruções Q # e diretivas terminam com um ponto e vírgula de terminação, `;` .</span><span class="sxs-lookup"><span data-stu-id="8c2e2-141">Most Q# statements and directives end with a terminating semicolon, `;`.</span></span>
<span data-ttu-id="8c2e2-142">Instruções e declarações como `for` e `operation` que terminam com um bloco de instruções (veja abaixo) não exigem um ponto e vírgula de terminação.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-142">Statements and declarations such as `for` and `operation` that end with a statement block (see below) do not require a terminating semicolon.</span></span>
<span data-ttu-id="8c2e2-143">Cada descrição de instrução observa se o ponto e vírgula de terminação é necessário.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-143">Each statement description notes whether the terminating semicolon is required.</span></span>

<span data-ttu-id="8c2e2-144">Instruções, como expressões, declarações e diretivas, podem ser divididas em várias linhas.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-144">Statements, like expressions, declarations, and directives, may be broken out across multiple lines.</span></span>
<span data-ttu-id="8c2e2-145">Ter várias instruções em uma única linha deve ser evitada.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-145">Having multiple statements on a single line should be avoided.</span></span>

## <a name="statement-blocks"></a><span data-ttu-id="8c2e2-146">Blocos de instrução</span><span class="sxs-lookup"><span data-stu-id="8c2e2-146">Statement Blocks</span></span>

<span data-ttu-id="8c2e2-147">As instruções Q # são agrupadas em blocos de instrução.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-147">Q# statements are grouped into statement blocks.</span></span>
<span data-ttu-id="8c2e2-148">Um bloco de instruções começa com uma abertura `{` e termina com um fechamento `}` .</span><span class="sxs-lookup"><span data-stu-id="8c2e2-148">A statement block starts with an opening `{` and ends with a closing `}`.</span></span>

<span data-ttu-id="8c2e2-149">Um bloco de instrução que está delimitado de forma lexical dentro de outro bloco é considerado um subbloco do bloco de contenção; os blocos e os subcontêineres também são chamados de bloco externo e interno.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-149">A statement block that is lexically enclosed within another block is considered to be a sub-block of the containing block; containing and sub-blocks are also called outer and inner blocks.</span></span>

## <a name="comments"></a><span data-ttu-id="8c2e2-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c2e2-150">Comments</span></span>

<span data-ttu-id="8c2e2-151">Os comentários começam com duas barras, `//` e continuam até o fim da linha.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-151">Comments begin with two forward slashes, `//`, and continue until the end of line.</span></span>
<span data-ttu-id="8c2e2-152">Um comentário pode aparecer em qualquer lugar em um arquivo de origem Q #.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-152">A comment may appear anywhere in a Q# source file.</span></span>

## <a name="documentation-comments"></a><span data-ttu-id="8c2e2-153">Comentários de documentação</span><span class="sxs-lookup"><span data-stu-id="8c2e2-153">Documentation Comments</span></span>

<span data-ttu-id="8c2e2-154">Os comentários que começam com três barras "/", `///` são tratados especialmente pelo compilador quando aparecem imediatamente antes de um namespace, operação, especialização, função ou definição de tipo.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-154">Comments that begin with three forward slashes, `///`, are treated specially by the compiler when they appear immediately before a namespace, operation, specialization, function, or type definition.</span></span>
<span data-ttu-id="8c2e2-155">Nesse caso, seu conteúdo é levado como documentação para o tipo definido pelo usuário ou callable, como para outras linguagens .NET.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-155">In that case, their contents are taken as documentation for the defined callable or user-defined type, as for other .NET languages.</span></span>

<span data-ttu-id="8c2e2-156">Em `///` comentários, o texto a ser exibido como parte da documentação da API é formatado como [redução](https://daringfireball.net/projects/markdown/syntax), com diferentes partes da documentação que estão sendo indicadas por cabeçalhos nomeados especialmente.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-156">Within `///` comments, text to appear as a part of API documentation is formatted as [Markdown](https://daringfireball.net/projects/markdown/syntax), with different parts of the documentation being indicated by specially-named headers.</span></span>
<span data-ttu-id="8c2e2-157">Como uma extensão para redução, as referências cruzadas a operações, funções e tipos definidos pelo usuário em Q # podem ser incluídas usando o `@"<ref target>"` , onde `<ref target>` é substituído pelo nome totalmente qualificado do objeto de código que está sendo referenciado.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-157">As an extension to Markdown, cross references to operations, functions and user-defined types in Q# can be included using the `@"<ref target>"`, where `<ref target>` is replaced by the fully qualified name of the code object being referenced.</span></span>
<span data-ttu-id="8c2e2-158">Opcionalmente, um mecanismo de documentação também pode oferecer suporte a extensões de redução adicionais.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-158">Optionally, a documentation engine may also support additional Markdown extensions.</span></span>

<span data-ttu-id="8c2e2-159">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="8c2e2-159">For example:</span></span>

```qsharp
/// # Summary
/// Given an operation and a target for that operation,
/// applies the given operation twice.
///
/// # Input
/// ## op
/// The operation to be applied.
/// ## target
/// The target to which the operation is to be applied.
///
/// # Type Parameters
/// ## 'T
/// The type expected by the given operation as its input.
///
/// # Example
/// ```Q#
/// // Should be equivalent to the identity.
/// ApplyTwice(H, qubit);
/// ```
///
/// # See Also
/// - Microsoft.Quantum.Intrinsic.H
operation ApplyTwice<'T>(op : ('T => Unit), target : 'T) : Unit {
    op(target);
    op(target);
}
```

<span data-ttu-id="8c2e2-160">Os nomes a seguir são reconhecidos como cabeçalhos de comentário da documentação.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-160">The following names are recognized as documentation comment headers.</span></span>

- <span data-ttu-id="8c2e2-161">**Resumo**: um breve resumo do comportamento de uma função ou operação, ou da finalidade de um tipo.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-161">**Summary**: A short summary of the behavior of a function or operation, or of the purpose of a type.</span></span> <span data-ttu-id="8c2e2-162">O primeiro parágrafo do resumo é usado para informações de foco.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-162">The first paragraph of the summary is used for hover information.</span></span> <span data-ttu-id="8c2e2-163">Ele deve ser texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-163">It should be plain text.</span></span>
- <span data-ttu-id="8c2e2-164">**Descrição**: uma descrição do comportamento de uma função ou operação, ou da finalidade de um tipo.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-164">**Description**: A description of the behavior of a function or operation, or of the purpose of a type.</span></span> <span data-ttu-id="8c2e2-165">O resumo e a descrição são concatenados para formar o arquivo de documentação gerado para a função, a operação ou o tipo.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-165">The summary and description are concatenated to form the generated documentation file for the function, operation, or type.</span></span>
  <span data-ttu-id="8c2e2-166">A descrição pode conter símbolos e equações LaTeX e formatados em linha.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-166">The description may contain in-line LaTeX-formatted symbols and equations.</span></span>
- <span data-ttu-id="8c2e2-167">**Entrada**: uma descrição da tupla de entrada para uma operação ou função.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-167">**Input**: A description of the input tuple for an operation or function.</span></span>
  <span data-ttu-id="8c2e2-168">Pode conter subseções de redução adicionais indicando cada elemento individual da tupla de entrada.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-168">May contain additional Markdown subsections indicating each individual element of the input tuple.</span></span>
- <span data-ttu-id="8c2e2-169">**Saída**: uma descrição da tupla retornada por uma operação ou função.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-169">**Output**: A description of the tuple returned by an operation or function.</span></span>
- <span data-ttu-id="8c2e2-170">**Parâmetros de tipo**: uma seção vazia que contém uma subseção adicional para cada parâmetro de tipo genérico.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-170">**Type Parameters**: An empty section which contains one additional subsection for each generic type parameter.</span></span>
- <span data-ttu-id="8c2e2-171">**Exemplo**: um breve exemplo da operação, função ou tipo em uso.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-171">**Example**: A short example of the operation, function or type in use.</span></span>
- <span data-ttu-id="8c2e2-172">**Comentários**: o Proseware variado que descreve algum aspecto da operação, função ou tipo.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-172">**Remarks**: Miscellaneous prose describing some aspect of the operation, function, or type.</span></span>
- <span data-ttu-id="8c2e2-173">**Consulte também**: uma lista de nomes totalmente qualificados que indica funções relacionadas, operações ou tipos definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-173">**See Also**: A list of fully qualified names indicating related functions, operations, or user-defined types.</span></span>
- <span data-ttu-id="8c2e2-174">**Referências**: uma lista de referências e citações para o item que está sendo documentado.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-174">**References**: A list of references and citations for the item being documented.</span></span>

## <a name="next-steps"></a><span data-ttu-id="8c2e2-175">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="8c2e2-175">Next steps</span></span>

<span data-ttu-id="8c2e2-176">Saiba mais sobre [as operações e funções](xref:microsoft.quantum.guide.operationsfunctions) em Q #.</span><span class="sxs-lookup"><span data-stu-id="8c2e2-176">Learn about [Operations and Functions](xref:microsoft.quantum.guide.operationsfunctions) in Q#.</span></span>