---
title: Q# Estrutura de arquivos
description: Descreve a estrutura e a sintaxe de um Q# arquivo.
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.filestructure
no-loc:
- Q#
- $$v
ms.openlocfilehash: 98b3a2e35186989b8191cc566a5d5310bc26eafc
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833303"
---
# <a name="no-locq-file-structure"></a><span data-ttu-id="96cc0-103">Q# Estrutura de arquivos</span><span class="sxs-lookup"><span data-stu-id="96cc0-103">Q# File Structure</span></span>

<span data-ttu-id="96cc0-104">Um Q# arquivo consiste em uma sequência de *declarações de namespace*.</span><span class="sxs-lookup"><span data-stu-id="96cc0-104">A Q# file consists of a sequence of *namespace declarations*.</span></span>
<span data-ttu-id="96cc0-105">Cada declaração de namespace contém declarações para tipos, operações e funções definidas pelo usuário, e pode conter qualquer número de cada tipo de declaração e em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="96cc0-105">Each namespace declaration contains declarations for user-defined types, operations, and functions, and can contain any number of each type of declaration and in any order.</span></span>
<span data-ttu-id="96cc0-106">Para obter mais informações sobre declarações em um namespace, consulte tipos, [operações](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations)e [funções](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions) [definidas pelo usuário](xref:microsoft.quantum.guide.types#user-defined-types).</span><span class="sxs-lookup"><span data-stu-id="96cc0-106">For more information on declarations within a namespace, see [user-defined types](xref:microsoft.quantum.guide.types#user-defined-types), [operations](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations), and [functions](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions).</span></span>

<span data-ttu-id="96cc0-107">O único texto que pode aparecer fora de uma declaração de namespace é comments.</span><span class="sxs-lookup"><span data-stu-id="96cc0-107">The only text that can appear outside of a namespace declaration is comments.</span></span>
<span data-ttu-id="96cc0-108">Em particular, comentários de documentação para um namespace precedem a declaração.</span><span class="sxs-lookup"><span data-stu-id="96cc0-108">In particular, documentation comments for a namespace precede the declaration.</span></span> <span data-ttu-id="96cc0-109">Para obter mais informações, consulte comentários sobre a [documentação](#documentation-comments) neste artigo.</span><span class="sxs-lookup"><span data-stu-id="96cc0-109">For more information, see [Documentation comments](#documentation-comments) in this article.</span></span> 

## <a name="namespace-declarations"></a><span data-ttu-id="96cc0-110">Declarações de namespace</span><span class="sxs-lookup"><span data-stu-id="96cc0-110">Namespace Declarations</span></span>

<span data-ttu-id="96cc0-111">Um Q# arquivo normalmente tem apenas uma declaração de namespace, mas pode ter nenhum (e estar vazio ou apenas conter comentários) ou pode conter vários namespaces.</span><span class="sxs-lookup"><span data-stu-id="96cc0-111">A Q# file typically has just one namespace declaration, but could have none (and be empty or just contain comments) or could contain multiple namespaces.</span></span>
<span data-ttu-id="96cc0-112">Declarações de namespace não podem ser aninhadas.</span><span class="sxs-lookup"><span data-stu-id="96cc0-112">Namespace declarations can not be nested.</span></span>

<span data-ttu-id="96cc0-113">Você pode declarar o mesmo namespace em vários Q# arquivos que são compilados juntos, desde que não haja nenhuma declaração de tipo, operação ou função com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="96cc0-113">You can declare the same namespace in multiple Q# files that are compiled together, as long as there are no type, operation, or function declarations with the same name.</span></span>
<span data-ttu-id="96cc0-114">Em particular, é inválido definir o mesmo tipo no mesmo namespace em vários arquivos, mesmo que as declarações sejam idênticas.</span><span class="sxs-lookup"><span data-stu-id="96cc0-114">In particular, it is invalid to define the same type in the same namespace in multiple files, even if the declarations are identical.</span></span>

<span data-ttu-id="96cc0-115">Uma declaração de namespace consiste na palavra-chave `namespace` , seguida pelo nome do namespace e as declarações contidas no namespace entre chaves `{ }` .</span><span class="sxs-lookup"><span data-stu-id="96cc0-115">A namespace declaration consists of the keyword `namespace`, followed by the name of the namespace, and the declarations contained in the namespace enclosed in braces `{ }`.</span></span>
<span data-ttu-id="96cc0-116">Os nomes de namespace seguem o padrão .NET de uma sequência de um ou mais símbolos legais separados por pontos `.` .</span><span class="sxs-lookup"><span data-stu-id="96cc0-116">Namespace names follow the .NET pattern of a sequence of one or more legal symbols separated by periods `.`.</span></span>
<span data-ttu-id="96cc0-117">Por exemplo, `MyQuantumStuff` e `Microsoft.Quantum.Intrinsic` são nomes de namespace válidos.</span><span class="sxs-lookup"><span data-stu-id="96cc0-117">For example, `MyQuantumStuff` and `Microsoft.Quantum.Intrinsic` are valid namespace names.</span></span>
<span data-ttu-id="96cc0-118">Por convenção, colocar os símbolos em maiúsculas em um nome de namespace, no entanto, isso não é necessário.</span><span class="sxs-lookup"><span data-stu-id="96cc0-118">By convention, capitalize the symbols in a namespace name, however, this is not required.</span></span>

<span data-ttu-id="96cc0-119">Referências a tipos ou chamadores declarados mais abaixo em um arquivo são resolvidos corretamente; Não há necessidade de tipo, operação ou declaração de função para preceder uma referência a ele.</span><span class="sxs-lookup"><span data-stu-id="96cc0-119">References to types or callables declared further down in a file resolve properly; there is no need for the type, operation, or function declaration to precede a reference to it.</span></span>

## <a name="open-directives"></a><span data-ttu-id="96cc0-120">Abrir diretivas</span><span class="sxs-lookup"><span data-stu-id="96cc0-120">Open Directives</span></span>

<span data-ttu-id="96cc0-121">Em um bloco de namespace, use a `open` diretiva para importar todos os tipos e chamadores declarados em um determinado namespace e consulte-os por seu nome não qualificado.</span><span class="sxs-lookup"><span data-stu-id="96cc0-121">Within a namespace block, use the `open` directive to import all types and callables declared in a certain namespace and refer to them by their unqualified name.</span></span>
<span data-ttu-id="96cc0-122">Essa `open` diretiva consiste na `open` palavra-chave, seguida pelo namespace a ser aberto e um ponto e vírgula de terminação.</span><span class="sxs-lookup"><span data-stu-id="96cc0-122">Such an `open` directive consists of the `open` keyword, followed by the namespace to be opened and a terminating semicolon.</span></span>

> [!NOTE] 
> <span data-ttu-id="96cc0-123">Todas as `open` diretivas devem aparecer antes de qualquer `function` `operation` declaração, ou `newtype` no bloco de namespace.</span><span class="sxs-lookup"><span data-stu-id="96cc0-123">All `open` directives must appear before any `function`, `operation`, or `newtype` declarations in the namespace block.</span></span>

<span data-ttu-id="96cc0-124">Opcionalmente, você pode definir um nome curto para o namespace aberto.</span><span class="sxs-lookup"><span data-stu-id="96cc0-124">Optionally, you can define a short name for the opened namespace.</span></span> <span data-ttu-id="96cc0-125">Se um nome curto for definido, você deverá qualificar todos os elementos desse namespace pelo nome curto definido.</span><span class="sxs-lookup"><span data-stu-id="96cc0-125">If a short name is defined, you must qualify all elements from that namespace by the defined short name.</span></span> <span data-ttu-id="96cc0-126">Por exemplo, considerando a seguinte declaração de namespace e as diretivas abertas,</span><span class="sxs-lookup"><span data-stu-id="96cc0-126">For example, given the following namespace declaration and open directives,</span></span>

```qsharp
namespace NS {
    open Microsoft.Quantum.Intrinsic; // opens the namespace
    open Microsoft.Quantum.Math as Math; // defines a short name for the namespace

    // operation, function, and newtype declarations

}
```

<span data-ttu-id="96cc0-127">se uma operação declarada usar uma operação `Op` do `Microsoft.Quantum.Intrinsic` , você a chamará simplesmente usando `Op` .</span><span class="sxs-lookup"><span data-stu-id="96cc0-127">if a declared operation uses an operation `Op` from `Microsoft.Quantum.Intrinsic`, you call it by simply using `Op`.</span></span>
<span data-ttu-id="96cc0-128">No entanto, para chamar uma determinada função `Fn` do `Microsoft.Quantum.Math` , você deve chamá-la usando `Math.Fn` .</span><span class="sxs-lookup"><span data-stu-id="96cc0-128">However, to call a certain function `Fn` from `Microsoft.Quantum.Math`, you must call it using `Math.Fn`.</span></span>

<span data-ttu-id="96cc0-129">A `open` diretiva se aplica a todo o bloco de namespace dentro de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="96cc0-129">The `open` directive applies to the entire namespace block within a file.</span></span>
<span data-ttu-id="96cc0-130">Portanto, se você definir um namespace adicional no mesmo Q# arquivo `NS` anterior, quaisquer operações/funções/tipos definidos no segundo namespace não teriam acesso a nada de `Microsoft.Quantum.Intrinsic` ou `Microsoft.Quantum.Math` a menos que você tenha repetido as diretivas abertas.</span><span class="sxs-lookup"><span data-stu-id="96cc0-130">Hence, if you define an additional namespace in the same Q# file as `NS` earlier, then any operations/functions/types defined in the second namespace would not have access to anything from `Microsoft.Quantum.Intrinsic` or `Microsoft.Quantum.Math` unless you repeated the open directives therein.</span></span> 

<span data-ttu-id="96cc0-131">Para fazer referência a um tipo ou callable definido em outro namespace que *não* está aberto no namespace atual, você deve fazer referência a ele pelo nome totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="96cc0-131">To reference a type or callable defined in another namespace that is *not* opened in the current namespace, you must reference it by its fully-qualified name.</span></span>
<span data-ttu-id="96cc0-132">Por exemplo, dada uma operação chamada `Op` do `X.Y` namespace:</span><span class="sxs-lookup"><span data-stu-id="96cc0-132">For example, given an operation named `Op` from the `X.Y` namespace:</span></span>

* <span data-ttu-id="96cc0-133">Você deve referenciá-lo por seu nome totalmente qualificado `X.Y.Op` , a menos que o `X.Y` namespace tenha sido aberto anteriormente no bloco atual.</span><span class="sxs-lookup"><span data-stu-id="96cc0-133">You must reference it by its fully-qualified name `X.Y.Op`, unless the `X.Y` namespace has been opened earlier in the current block.</span></span> 
* <span data-ttu-id="96cc0-134">Mesmo que o `X` namespace seja aberto, não é possível fazer referência à operação como `Y.Op` .</span><span class="sxs-lookup"><span data-stu-id="96cc0-134">Even if the `X` namespace is opened, it is not possible to reference the operation as `Y.Op`.</span></span>
* <span data-ttu-id="96cc0-135">Se você tiver definido o nome curto `Z` para `X.Y` nesse namespace e arquivo, deverá referenciar `Op` como `Z.Op` .</span><span class="sxs-lookup"><span data-stu-id="96cc0-135">If you defined the short name `Z` for `X.Y` in that namespace and file, you must reference `Op` as `Z.Op`.</span></span> 

<span data-ttu-id="96cc0-136">Geralmente, é melhor incluir um namespace usando uma `open` diretiva.</span><span class="sxs-lookup"><span data-stu-id="96cc0-136">It is usually better to include a namespace by using an `open` directive.</span></span>
<span data-ttu-id="96cc0-137">Usar um nome totalmente qualificado é necessário se dois namespaces definem construções com o mesmo nome e a fonte atual usa construções de ambos.</span><span class="sxs-lookup"><span data-stu-id="96cc0-137">Using a fully-qualified name is required if two namespaces define constructs with the same name, and the current source uses constructs from both.</span></span>

<span data-ttu-id="96cc0-138">Q# segue as mesmas regras para nomear como outras linguagens .NET.</span><span class="sxs-lookup"><span data-stu-id="96cc0-138">Q# follows the same rules for naming as other .NET languages.</span></span>
<span data-ttu-id="96cc0-139">No entanto, Q# o não oferece suporte a referências relativas a namespaces.</span><span class="sxs-lookup"><span data-stu-id="96cc0-139">However, Q# does not support relative references to namespaces.</span></span>
<span data-ttu-id="96cc0-140">Por exemplo, se o namespace `a.b` estiver aberto, uma referência a uma operação chamada `c.d` não *será* resolvida para uma operação com o nome completo `a.b.c.d` .</span><span class="sxs-lookup"><span data-stu-id="96cc0-140">For example, if the namespace `a.b` is open, a reference to an operation named `c.d` does *not* resolve to an operation with full name `a.b.c.d`.</span></span>

## <a name="formatting"></a><span data-ttu-id="96cc0-141">Formatação</span><span class="sxs-lookup"><span data-stu-id="96cc0-141">Formatting</span></span>

<span data-ttu-id="96cc0-142">A maioria das Q# instruções e diretivas terminam com um ponto e vírgula de terminação, `;` .</span><span class="sxs-lookup"><span data-stu-id="96cc0-142">Most Q# statements and directives end with a terminating semicolon, `;`.</span></span>
<span data-ttu-id="96cc0-143">Instruções e declarações como `for` e `operation` que terminam com um bloco de instruções (consulte a seção a seguir) não exigem um ponto e vírgula de terminação.</span><span class="sxs-lookup"><span data-stu-id="96cc0-143">Statements and declarations such as `for` and `operation` that end with a statement block (see the following section) do not require a terminating semicolon.</span></span>
<span data-ttu-id="96cc0-144">Cada descrição de instrução observa se o ponto e vírgula de terminação é necessário.</span><span class="sxs-lookup"><span data-stu-id="96cc0-144">Each statement description notes whether the terminating semicolon is required.</span></span>

<span data-ttu-id="96cc0-145">Instruções, como expressões, declarações e diretivas, podem ser divididas em várias linhas.</span><span class="sxs-lookup"><span data-stu-id="96cc0-145">Statements, like expressions, declarations, and directives, can be broken out across multiple lines.</span></span>
<span data-ttu-id="96cc0-146">Evite colocar várias instruções em uma única linha.</span><span class="sxs-lookup"><span data-stu-id="96cc0-146">Avoid putting multiple statements on a single line.</span></span>

## <a name="statement-blocks"></a><span data-ttu-id="96cc0-147">Blocos de instrução</span><span class="sxs-lookup"><span data-stu-id="96cc0-147">Statement Blocks</span></span>

<span data-ttu-id="96cc0-148">Q# as instruções são agrupadas em blocos de instrução, que estão contidos com chaves `{ }` .</span><span class="sxs-lookup"><span data-stu-id="96cc0-148">Q# statements are grouped into statement blocks, which are contained with braces `{ }`.</span></span> <span data-ttu-id="96cc0-149">Um bloco de instruções começa com uma abertura `{` e termina com um fechamento `}` .</span><span class="sxs-lookup"><span data-stu-id="96cc0-149">A statement block starts with an opening `{` and ends with a closing `}`.</span></span>

<span data-ttu-id="96cc0-150">Um bloco de instrução que está delimitado de forma lexical dentro de outro bloco é considerado um subbloco do bloco de contenção; os blocos e os subcontêineres também são chamados de bloco externo e interno.</span><span class="sxs-lookup"><span data-stu-id="96cc0-150">A statement block that is lexically enclosed within another block is considered to be a sub-block of the containing block; containing and sub-blocks are also called outer and inner blocks.</span></span>

## <a name="comments"></a><span data-ttu-id="96cc0-151">Comentários</span><span class="sxs-lookup"><span data-stu-id="96cc0-151">Comments</span></span>

<span data-ttu-id="96cc0-152">Os comentários começam com duas barras, `//` e continuam até o final da linha.</span><span class="sxs-lookup"><span data-stu-id="96cc0-152">Comments begin with two forward slashes, `//`, and continue until the end of the line.</span></span>
<span data-ttu-id="96cc0-153">Um comentário pode aparecer em qualquer lugar em um Q# arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="96cc0-153">A comment can appear anywhere in a Q# source file.</span></span>

## <a name="documentation-comments"></a><span data-ttu-id="96cc0-154">Comentários de documentação</span><span class="sxs-lookup"><span data-stu-id="96cc0-154">Documentation Comments</span></span>

<span data-ttu-id="96cc0-155">Os comentários que começam com três barras "/", `///` são tratados especialmente pelo compilador quando aparecem imediatamente antes de um namespace, operação, especialização, função ou definição de tipo.</span><span class="sxs-lookup"><span data-stu-id="96cc0-155">Comments that begin with three forward slashes, `///`, are treated specially by the compiler when they appear immediately before a namespace, operation, specialization, function, or type definition.</span></span>
<span data-ttu-id="96cc0-156">Nesse caso, o compilador os trata como documentação para o tipo definido pelo usuário ou callable, o mesmo que outras linguagens .NET.</span><span class="sxs-lookup"><span data-stu-id="96cc0-156">In that case, the compiler treats them as documentation for the defined callable or user-defined type, the same as other .NET languages.</span></span>

<span data-ttu-id="96cc0-157">Em `///` comentários, o texto a ser exibido como parte da documentação da API é formatado como [redução](https://daringfireball.net/projects/markdown/syntax), com diferentes partes da documentação indicada por cabeçalhos nomeados especialmente.</span><span class="sxs-lookup"><span data-stu-id="96cc0-157">Within `///` comments, text to appear as a part of API documentation is formatted as [Markdown](https://daringfireball.net/projects/markdown/syntax), with different parts of the documentation indicated by specially-named headers.</span></span>
<span data-ttu-id="96cc0-158">Em redução, use a `@"<ref target>"` extensão para operações de referência cruzada, funções e tipos definidos pelo usuário no Q# .</span><span class="sxs-lookup"><span data-stu-id="96cc0-158">In Markdown, use the `@"<ref target>"` extension to cross-reference operations, functions, and user-defined types in Q#.</span></span> <span data-ttu-id="96cc0-159">Substituir `<ref target>` pelo nome totalmente qualificado do objeto de código referenciado.</span><span class="sxs-lookup"><span data-stu-id="96cc0-159">Replace `<ref target>` with the fully qualified name of the referenced code object.</span></span>
<span data-ttu-id="96cc0-160">Mecanismos de documentação diferentes também podem oferecer suporte a extensões de redução adicionais.</span><span class="sxs-lookup"><span data-stu-id="96cc0-160">Different documentation engines may also support additional Markdown extensions.</span></span>

<span data-ttu-id="96cc0-161">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="96cc0-161">For example:</span></span>

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

<span data-ttu-id="96cc0-162">Os nomes a seguir são válidos como cabeçalhos de comentário da documentação.</span><span class="sxs-lookup"><span data-stu-id="96cc0-162">The following names are valid as documentation comment headers.</span></span>

- <span data-ttu-id="96cc0-163">**Resumo**: um breve resumo do comportamento de uma função ou operação, ou a finalidade de um tipo.</span><span class="sxs-lookup"><span data-stu-id="96cc0-163">**Summary**: A short summary of the behavior of a function or operation, or the purpose of a type.</span></span> <span data-ttu-id="96cc0-164">O primeiro parágrafo do resumo é usado para informações de foco.</span><span class="sxs-lookup"><span data-stu-id="96cc0-164">The first paragraph of the summary is used for hover information.</span></span> <span data-ttu-id="96cc0-165">Ele deve ser texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="96cc0-165">It should be plain text.</span></span>
- <span data-ttu-id="96cc0-166">**Descrição**: uma descrição do comportamento de uma função ou operação ou a finalidade de um tipo.</span><span class="sxs-lookup"><span data-stu-id="96cc0-166">**Description**: A description of the behavior of a function or operation, or the purpose of a type.</span></span> <span data-ttu-id="96cc0-167">Juntos, o resumo e a descrição formam o arquivo de documentação gerado para a função, a operação ou o tipo.</span><span class="sxs-lookup"><span data-stu-id="96cc0-167">Together, the summary and description form the generated documentation file for the function, operation, or type.</span></span>
  <span data-ttu-id="96cc0-168">A descrição oferece suporte a equações e símbolos formatados para LaTeX em linha.</span><span class="sxs-lookup"><span data-stu-id="96cc0-168">The description supports in-line LaTeX-formatted symbols and equations.</span></span>
- <span data-ttu-id="96cc0-169">**Entrada**: uma descrição da tupla de entrada para uma operação ou função.</span><span class="sxs-lookup"><span data-stu-id="96cc0-169">**Input**: A description of the input tuple for an operation or function.</span></span>
  <span data-ttu-id="96cc0-170">Pode conter subseções de redução adicionais indicando cada elemento da tupla de entrada.</span><span class="sxs-lookup"><span data-stu-id="96cc0-170">Can contain additional Markdown subsections indicating each element of the input tuple.</span></span>
- <span data-ttu-id="96cc0-171">**Saída**: uma descrição da tupla retornada por uma operação ou função.</span><span class="sxs-lookup"><span data-stu-id="96cc0-171">**Output**: A description of the tuple returned by an operation or function.</span></span>
- <span data-ttu-id="96cc0-172">**Parâmetros de tipo**: uma seção vazia que contém uma subseção adicional para cada parâmetro de tipo genérico.</span><span class="sxs-lookup"><span data-stu-id="96cc0-172">**Type Parameters**: An empty section that contains one additional subsection for each generic type parameter.</span></span>
- <span data-ttu-id="96cc0-173">**Exemplo**: um breve exemplo da operação, da função ou do tipo em uso.</span><span class="sxs-lookup"><span data-stu-id="96cc0-173">**Example**: A short example of the operation, function, or type in use.</span></span>
- <span data-ttu-id="96cc0-174">**Comentários**: o Proseware variado que descreve algum aspecto da operação, função ou tipo.</span><span class="sxs-lookup"><span data-stu-id="96cc0-174">**Remarks**: Miscellaneous prose describing some aspect of the operation, function, or type.</span></span>
- <span data-ttu-id="96cc0-175">**Consulte também**: uma lista de nomes totalmente qualificados que indica funções relacionadas, operações ou tipos definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="96cc0-175">**See Also**: A list of fully qualified names indicating related functions, operations, or user-defined types.</span></span>
- <span data-ttu-id="96cc0-176">**References**: uma lista de referências e citações para o item documentado.</span><span class="sxs-lookup"><span data-stu-id="96cc0-176">**References**: A list of references and citations for the documented item.</span></span>

## <a name="next-steps"></a><span data-ttu-id="96cc0-177">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="96cc0-177">Next steps</span></span>

<span data-ttu-id="96cc0-178">Saiba mais sobre [as operações e funções](xref:microsoft.quantum.guide.operationsfunctions) no Q# .</span><span class="sxs-lookup"><span data-stu-id="96cc0-178">Learn about [Operations and Functions](xref:microsoft.quantum.guide.operationsfunctions) in Q#.</span></span>