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
# <a name="q-file-structure"></a>Estrutura de arquivos de Q #

Cada operação de Q #, função e tipo definido pelo usuário é definido em um namespace.

Um arquivo Q # consiste em uma sequência de *declarações de namespace*.
Cada declaração de namespace contém declarações para tipos, operações e funções definidas pelo usuário.
Uma declaração de namespace pode conter qualquer número de cada tipo de declaração e em qualquer ordem.
Siga estes links para obter mais detalhes sobre como declarar tipos, [operações](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations)e [funções](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions) [definidas pelo usuário](xref:microsoft.quantum.guide.types#user-defined-types)em um namespace.

O único texto que pode aparecer fora de uma declaração de namespace é comments.
Em particular, comentários de documentação (mais detalhes abaixo) para um namespace precedem a declaração.

## <a name="namespace-declarations"></a>Declarações de namespace

Um arquivo Q # normalmente terá exatamente uma declaração de namespace, mas pode ter nenhum (e estar vazio ou apenas conter comentários) ou pode conter vários namespaces.
Declarações de namespace não podem ser aninhadas.

O mesmo namespace pode ser declarado em vários arquivos Q # que são compilados juntos, desde que não haja nenhuma declaração de tipo, operação ou função com o mesmo nome.
Em particular, é inválido definir o mesmo tipo no mesmo namespace em vários arquivos, mesmo que as declarações sejam idênticas.

Uma declaração de namespace consiste na palavra-chave `namespace` , seguida pelo nome do namespace, uma chave de abertura `{` , as declarações contidas no namespace e uma chave de fechamento `}` .
Os nomes de namespace seguem o padrão .NET de uma sequência de um ou mais símbolos legais separados por pontos `.` .
Por exemplo, `MyQuantumStuff` e `Microsoft.Quantum.Intrinsic` são nomes de namespace válidos.
Por convenção, os símbolos em um nome de namespace estão em letras maiúsculas, mas isso não é necessário.

Referências a tipos ou chamadores declarados mais abaixo em um arquivo são resolvidos corretamente; Não há necessidade de tipo, operação ou declaração de função para preceder uma referência a ele.

## <a name="open-directives"></a>Abrir diretivas

Em um bloco de namespace, a `open` diretiva pode ser usada para importar todos os tipos e chamadores declarados em um determinado namespace e consultá-los por seu nome não qualificado.
Essa `open` diretiva consiste na `open` palavra-chave, seguida pelo namespace a ser aberto e um ponto e vírgula de terminação.

> [!NOTE] 
> Todas as `open` diretivas devem aparecer antes de qualquer `function` `operation` declaração, ou `newtype` no bloco de namespace.

Opcionalmente, um nome curto para o namespace aberto pode ser definido de modo que todos os elementos desse namespace possam (e precisam) ser qualificados pelo nome curto definido. Por exemplo, considerando a seguinte declaração de namespace e as diretivas abertas,

```qsharp
namespace NS {
    open Microsoft.Quantum.Intrinsic; // opens the namespace
    open Microsoft.Quantum.Math as Math; // defines a short name for the namespace

    // operation, function, and newtype declarations

}
```

se uma operação que declararmos usar uma operação `Op` de `Microsoft.Quantum.Intrinsic` , nós a chamaremos simplesmente usando `Op` .
No entanto, se quiséssemos uma chamada a determinada função `Fn` `Microsoft.Quantum.Math` , precisaremos chamá-la usando `Math.Fn` .

A `open` diretiva se aplica a todo o bloco de namespace dentro de um arquivo.
Portanto, se tivéssemos de definir um namespace adicional no mesmo arquivo Q # como `NS` acima, quaisquer operações/funções/tipos definidos no segundo namespace não teriam acesso a nada de `Microsoft.Quantum.Intrinsic` ou `Microsoft.Quantum.Math` a menos que tenhamos repetido as diretivas abertas. 

Um tipo ou callable definido em outro namespace que *não* está aberto no namespace atual deve ser referenciado por seu nome totalmente qualificado.
Por exemplo, uma operação chamada `Op` do `X.Y` namespace deve ser referenciada por seu nome totalmente qualificado `X.Y.Op` , a menos que o `X.Y` namespace tenha sido aberto anteriormente no bloco atual. Conforme mencionado acima, mesmo que o `X` namespace tenha sido aberto, não é possível fazer referência à operação como `Y.Op` .
Se um nome curto `Z` para `X.Y` tiver sido definido nesse namespace e arquivo, `Op` o deverá ser referenciado como `Z.Op` . 

Geralmente, é melhor incluir um namespace usando uma `open` diretiva.
Usar um nome totalmente qualificado é necessário se dois namespaces definem construções com o mesmo nome e a fonte atual usa construções de ambos.

O Q # segue as mesmas regras para nomear como outras linguagens .NET.
No entanto, Q # não oferece suporte a referências relativas a namespaces.
Ou seja, se o namespace `a.b` tiver sido aberto, uma referência a uma operação chamada `c.d` *não* será resolvida para uma operação com o nome completo `a.b.c.d` .

## <a name="formatting"></a>Formatação

A maioria das instruções Q # e diretivas terminam com um ponto e vírgula de terminação, `;` .
Instruções e declarações como `for` e `operation` que terminam com um bloco de instruções (veja abaixo) não exigem um ponto e vírgula de terminação.
Cada descrição de instrução observa se o ponto e vírgula de terminação é necessário.

Instruções, como expressões, declarações e diretivas, podem ser divididas em várias linhas.
Ter várias instruções em uma única linha deve ser evitada.

## <a name="statement-blocks"></a>Blocos de instrução

As instruções Q # são agrupadas em blocos de instrução.
Um bloco de instruções começa com uma abertura `{` e termina com um fechamento `}` .

Um bloco de instrução que está delimitado de forma lexical dentro de outro bloco é considerado um subbloco do bloco de contenção; os blocos e os subcontêineres também são chamados de bloco externo e interno.

## <a name="comments"></a>Comentários

Os comentários começam com duas barras, `//` e continuam até o fim da linha.
Um comentário pode aparecer em qualquer lugar em um arquivo de origem Q #.

## <a name="documentation-comments"></a>Comentários de documentação

Os comentários que começam com três barras "/", `///` são tratados especialmente pelo compilador quando aparecem imediatamente antes de um namespace, operação, especialização, função ou definição de tipo.
Nesse caso, seu conteúdo é levado como documentação para o tipo definido pelo usuário ou callable, como para outras linguagens .NET.

Em `///` comentários, o texto a ser exibido como parte da documentação da API é formatado como [redução](https://daringfireball.net/projects/markdown/syntax), com diferentes partes da documentação que estão sendo indicadas por cabeçalhos nomeados especialmente.
Como uma extensão para redução, as referências cruzadas a operações, funções e tipos definidos pelo usuário em Q # podem ser incluídas usando o `@"<ref target>"` , onde `<ref target>` é substituído pelo nome totalmente qualificado do objeto de código que está sendo referenciado.
Opcionalmente, um mecanismo de documentação também pode oferecer suporte a extensões de redução adicionais.

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

Os nomes a seguir são reconhecidos como cabeçalhos de comentário da documentação.

- **Resumo**: um breve resumo do comportamento de uma função ou operação, ou da finalidade de um tipo. O primeiro parágrafo do resumo é usado para informações de foco. Ele deve ser texto sem formatação.
- **Descrição**: uma descrição do comportamento de uma função ou operação, ou da finalidade de um tipo. O resumo e a descrição são concatenados para formar o arquivo de documentação gerado para a função, a operação ou o tipo.
  A descrição pode conter símbolos e equações LaTeX e formatados em linha.
- **Entrada**: uma descrição da tupla de entrada para uma operação ou função.
  Pode conter subseções de redução adicionais indicando cada elemento individual da tupla de entrada.
- **Saída**: uma descrição da tupla retornada por uma operação ou função.
- **Parâmetros de tipo**: uma seção vazia que contém uma subseção adicional para cada parâmetro de tipo genérico.
- **Exemplo**: um breve exemplo da operação, função ou tipo em uso.
- **Comentários**: o Proseware variado que descreve algum aspecto da operação, função ou tipo.
- **Consulte também**: uma lista de nomes totalmente qualificados que indica funções relacionadas, operações ou tipos definidos pelo usuário.
- **Referências**: uma lista de referências e citações para o item que está sendo documentado.

## <a name="next-steps"></a>Próximas etapas

Saiba mais sobre [as operações e funções](xref:microsoft.quantum.guide.operationsfunctions) em Q #.