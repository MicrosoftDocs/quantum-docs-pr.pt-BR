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
# <a name="no-locq-file-structure"></a>Q# Estrutura de arquivos

Um Q# arquivo consiste em uma sequência de *declarações de namespace*.
Cada declaração de namespace contém declarações para tipos, operações e funções definidas pelo usuário, e pode conter qualquer número de cada tipo de declaração e em qualquer ordem.
Para obter mais informações sobre declarações em um namespace, consulte tipos, [operações](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations)e [funções](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions) [definidas pelo usuário](xref:microsoft.quantum.guide.types#user-defined-types).

O único texto que pode aparecer fora de uma declaração de namespace é comments.
Em particular, comentários de documentação para um namespace precedem a declaração. Para obter mais informações, consulte comentários sobre a [documentação](#documentation-comments) neste artigo. 

## <a name="namespace-declarations"></a>Declarações de namespace

Um Q# arquivo normalmente tem apenas uma declaração de namespace, mas pode ter nenhum (e estar vazio ou apenas conter comentários) ou pode conter vários namespaces.
Declarações de namespace não podem ser aninhadas.

Você pode declarar o mesmo namespace em vários Q# arquivos que são compilados juntos, desde que não haja nenhuma declaração de tipo, operação ou função com o mesmo nome.
Em particular, é inválido definir o mesmo tipo no mesmo namespace em vários arquivos, mesmo que as declarações sejam idênticas.

Uma declaração de namespace consiste na palavra-chave `namespace` , seguida pelo nome do namespace e as declarações contidas no namespace entre chaves `{ }` .
Os nomes de namespace seguem o padrão .NET de uma sequência de um ou mais símbolos legais separados por pontos `.` .
Por exemplo, `MyQuantumStuff` e `Microsoft.Quantum.Intrinsic` são nomes de namespace válidos.
Por convenção, colocar os símbolos em maiúsculas em um nome de namespace, no entanto, isso não é necessário.

Referências a tipos ou chamadores declarados mais abaixo em um arquivo são resolvidos corretamente; Não há necessidade de tipo, operação ou declaração de função para preceder uma referência a ele.

## <a name="open-directives"></a>Abrir diretivas

Em um bloco de namespace, use a `open` diretiva para importar todos os tipos e chamadores declarados em um determinado namespace e consulte-os por seu nome não qualificado.
Essa `open` diretiva consiste na `open` palavra-chave, seguida pelo namespace a ser aberto e um ponto e vírgula de terminação.

> [!NOTE] 
> Todas as `open` diretivas devem aparecer antes de qualquer `function` `operation` declaração, ou `newtype` no bloco de namespace.

Opcionalmente, você pode definir um nome curto para o namespace aberto. Se um nome curto for definido, você deverá qualificar todos os elementos desse namespace pelo nome curto definido. Por exemplo, considerando a seguinte declaração de namespace e as diretivas abertas,

```qsharp
namespace NS {
    open Microsoft.Quantum.Intrinsic; // opens the namespace
    open Microsoft.Quantum.Math as Math; // defines a short name for the namespace

    // operation, function, and newtype declarations

}
```

se uma operação declarada usar uma operação `Op` do `Microsoft.Quantum.Intrinsic` , você a chamará simplesmente usando `Op` .
No entanto, para chamar uma determinada função `Fn` do `Microsoft.Quantum.Math` , você deve chamá-la usando `Math.Fn` .

A `open` diretiva se aplica a todo o bloco de namespace dentro de um arquivo.
Portanto, se você definir um namespace adicional no mesmo Q# arquivo `NS` anterior, quaisquer operações/funções/tipos definidos no segundo namespace não teriam acesso a nada de `Microsoft.Quantum.Intrinsic` ou `Microsoft.Quantum.Math` a menos que você tenha repetido as diretivas abertas. 

Para fazer referência a um tipo ou callable definido em outro namespace que *não* está aberto no namespace atual, você deve fazer referência a ele pelo nome totalmente qualificado.
Por exemplo, dada uma operação chamada `Op` do `X.Y` namespace:

* Você deve referenciá-lo por seu nome totalmente qualificado `X.Y.Op` , a menos que o `X.Y` namespace tenha sido aberto anteriormente no bloco atual. 
* Mesmo que o `X` namespace seja aberto, não é possível fazer referência à operação como `Y.Op` .
* Se você tiver definido o nome curto `Z` para `X.Y` nesse namespace e arquivo, deverá referenciar `Op` como `Z.Op` . 

Geralmente, é melhor incluir um namespace usando uma `open` diretiva.
Usar um nome totalmente qualificado é necessário se dois namespaces definem construções com o mesmo nome e a fonte atual usa construções de ambos.

Q# segue as mesmas regras para nomear como outras linguagens .NET.
No entanto, Q# o não oferece suporte a referências relativas a namespaces.
Por exemplo, se o namespace `a.b` estiver aberto, uma referência a uma operação chamada `c.d` não *será* resolvida para uma operação com o nome completo `a.b.c.d` .

## <a name="formatting"></a>Formatação

A maioria das Q# instruções e diretivas terminam com um ponto e vírgula de terminação, `;` .
Instruções e declarações como `for` e `operation` que terminam com um bloco de instruções (consulte a seção a seguir) não exigem um ponto e vírgula de terminação.
Cada descrição de instrução observa se o ponto e vírgula de terminação é necessário.

Instruções, como expressões, declarações e diretivas, podem ser divididas em várias linhas.
Evite colocar várias instruções em uma única linha.

## <a name="statement-blocks"></a>Blocos de instrução

Q# as instruções são agrupadas em blocos de instrução, que estão contidos com chaves `{ }` . Um bloco de instruções começa com uma abertura `{` e termina com um fechamento `}` .

Um bloco de instrução que está delimitado de forma lexical dentro de outro bloco é considerado um subbloco do bloco de contenção; os blocos e os subcontêineres também são chamados de bloco externo e interno.

## <a name="comments"></a>Comentários

Os comentários começam com duas barras, `//` e continuam até o final da linha.
Um comentário pode aparecer em qualquer lugar em um Q# arquivo de origem.

## <a name="documentation-comments"></a>Comentários de documentação

Os comentários que começam com três barras "/", `///` são tratados especialmente pelo compilador quando aparecem imediatamente antes de um namespace, operação, especialização, função ou definição de tipo.
Nesse caso, o compilador os trata como documentação para o tipo definido pelo usuário ou callable, o mesmo que outras linguagens .NET.

Em `///` comentários, o texto a ser exibido como parte da documentação da API é formatado como [redução](https://daringfireball.net/projects/markdown/syntax), com diferentes partes da documentação indicada por cabeçalhos nomeados especialmente.
Em redução, use a `@"<ref target>"` extensão para operações de referência cruzada, funções e tipos definidos pelo usuário no Q# . Substituir `<ref target>` pelo nome totalmente qualificado do objeto de código referenciado.
Mecanismos de documentação diferentes também podem oferecer suporte a extensões de redução adicionais.

Por exemplo:

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

Os nomes a seguir são válidos como cabeçalhos de comentário da documentação.

- **Resumo**: um breve resumo do comportamento de uma função ou operação, ou a finalidade de um tipo. O primeiro parágrafo do resumo é usado para informações de foco. Ele deve ser texto sem formatação.
- **Descrição**: uma descrição do comportamento de uma função ou operação ou a finalidade de um tipo. Juntos, o resumo e a descrição formam o arquivo de documentação gerado para a função, a operação ou o tipo.
  A descrição oferece suporte a equações e símbolos formatados para LaTeX em linha.
- **Entrada**: uma descrição da tupla de entrada para uma operação ou função.
  Pode conter subseções de redução adicionais indicando cada elemento da tupla de entrada.
- **Saída**: uma descrição da tupla retornada por uma operação ou função.
- **Parâmetros de tipo**: uma seção vazia que contém uma subseção adicional para cada parâmetro de tipo genérico.
- **Exemplo**: um breve exemplo da operação, da função ou do tipo em uso.
- **Comentários**: o Proseware variado que descreve algum aspecto da operação, função ou tipo.
- **Consulte também**: uma lista de nomes totalmente qualificados que indica funções relacionadas, operações ou tipos definidos pelo usuário.
- **References**: uma lista de referências e citações para o item documentado.

## <a name="next-steps"></a>Próximas etapas

Saiba mais sobre [as operações e funções](xref:microsoft.quantum.guide.operationsfunctions) no Q# .