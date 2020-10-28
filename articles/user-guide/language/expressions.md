---
title: Expressões em Q#
description: Entenda como especificar, referenciar e combinar constantes, variáveis, operadores, operações e funções como expressões no Q# .
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.expressions
no-loc:
- Q#
- $$v
ms.openlocfilehash: e95a7cb9b74136ef9a6f51b4bbc32d1d93c43a0d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691597"
---
# <a name="expressions-in-no-locq"></a>Expressões em Q#

## <a name="numeric-expressions"></a>Expressões numéricas

Expressões numéricas são expressões do tipo `Int` , `BigInt` ou `Double` .
Ou seja, eles são números inteiros ou de ponto flutuante.

`Int` os literais no Q# são gravados como uma sequência de dígitos.
Os inteiros hexadecimais e binários têm suporte e são gravados com um `0x` `0b` prefixo e, respectivamente.

`BigInt` os literais no Q# têm um `l` sufixo ou à direita `L` .
Há suporte para inteiros grandes hexadecimais e gravados com um prefixo "0x".
Portanto, veja a seguir todos os usos válidos de `BigInt` literais:

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

`Double` os literais no Q# são números de ponto flutuante gravados usando dígitos decimais.
Eles podem ser escritos com ou sem um ponto decimal, `.` ou uma parte exponencial indicada com ' e ' ou ' e ' (após o qual apenas um possível sinal negativo e dígitos decimais são válidos).
Os seguintes são `Double` literais válidos: `0.0` , `1.2e5` , `1e-5` .

Dada uma expressão de matriz de qualquer tipo de elemento, você pode formar uma `Int` expressão usando a [`Length`](xref:Microsoft.Quantum.Core.Length) função interna, com a expressão de matriz entre parênteses.
Por exemplo, se `a` estiver associado a uma matriz, `Length(a)` será uma expressão de inteiro.
Se `b` é uma matriz de matrizes de inteiros, `Int[][]` , `Length(b)` é o número de submatrizes em `b` e `Length(b[1])` é o número de inteiros na segunda submatriz no `b` .

Dadas duas expressões numéricas do mesmo tipo, os operadores binários,, `+` `-` `*` e `/` podem ser usados para formar uma nova expressão numérica.
O tipo da nova expressão é o mesmo que os tipos das expressões constituintes.

Dadas duas expressões de inteiro, use o operador Binary `^` (Power) para formar uma nova expressão de inteiro.
Da mesma forma, você também pode usar `^` com duas expressões duplas para formar uma nova expressão Double.
Por fim, você pode usar `^` com um inteiro grande à esquerda e um inteiro à direita para formar uma nova expressão de inteiro grande.
Nesse caso, o segundo parâmetro deve caber em 32 bits; caso contrário, ele gera um erro de tempo de execução.

Dadas duas expressões de inteiro ou grandes inteiros, formate um novo inteiro ou uma expressão de inteiro grande usando os `%` operadores (módulo), `&&&` (bit e), (OR bit a bit `|||` ) ou `^^^` (XOR).

Dado um inteiro ou uma expressão de inteiro grande à esquerda e uma expressão de inteiro à direita, use os `<<<` operadores (deslocamento aritmético à esquerda) ou `>>>` (deslocamento aritmético à direita) para criar uma nova expressão com o mesmo tipo que a expressão esquerda.

O segundo parâmetro (o valor de deslocamento) para a operação de deslocamento deve ser maior ou igual a zero; o comportamento para valores de deslocamento negativos é indefinido.
O valor de deslocamento para uma das operações de deslocamento também deve se ajustar a 32 bits; caso contrário, ele gera um erro de tempo de execução.
Se o número deslocado for um inteiro, o valor de deslocamento será interpretado `mod 64` ; ou seja, um deslocamento de 1 e um deslocamento de 65 terão o mesmo efeito.

Para os valores inteiros e inteiros grandes, as turnos são aritméticas.
A mudança de um valor negativo para a esquerda ou para a direita resulta em um número negativo.
Ou seja, mudar uma etapa para a esquerda ou para a direita é o mesmo que multiplicar ou dividir por 2, respectivamente.

Divisão de inteiros e módulo de inteiro seguem o mesmo comportamento para números negativos em C#. Ou seja, `a % b` sempre tem o mesmo sinal como `a` e `b * (a / b) + a % b` sempre é igual a `a` . Por exemplo:

|`A` | `B` | `A / B` | `A % B`|
|:---------:|:----------:|:---------:|:---------:|
| 5 | 2 | 2 | 1 |
| 5 | -2 | -2 | 1 |
| -5 | 2 | -2 | -1 |
| -5 | -2 | 2 | -1 |

A divisão de inteiro grande e as operações de módulo funcionam da mesma maneira.

Dada qualquer expressão numérica, você pode formar uma nova expressão usando o `-` operador unário.
A nova expressão é do mesmo tipo que a expressão constituir.

Dada qualquer inteiro ou expressão de inteiro grande, você pode formar uma nova expressão do mesmo tipo usando o `~~~` operador unário (complemento bit a bit).

## <a name="boolean-expressions"></a>Expressões boolianas

Os dois `Bool` valores literais são `true` e `false` .

Dadas as duas expressões do mesmo tipo primitivo, os `==` `!=` operadores binários e podem ser usados para construir uma `Bool` expressão.
A expressão será true se as duas expressões forem iguais e false se não.

Os valores de tipos definidos pelo usuário não podem ser comparados, apenas seus valores não encapsulados podem ser comparados. Por exemplo, usando o operador "sem encapsulamento" `!` (explicado em detalhes em [tipos Q# em ](xref:microsoft.quantum.guide.types#access-anonymous-items-with-the-unwrap-operator)),

```qsharp
newtype WrappedInt = Int;     // Yes, this is a contrived example
let x = WrappedInt(1);
let y = WrappedInt(2);
let z = x! == y!;             // This will compile and yield z = false.
let t = x == y;               // This will cause a compiler error.
```

A comparação de igualdade para `Qubit` valores é igualdade de identidade; ou seja, se as duas expressões identificam o mesmo qubit.
Os Estados dos dois qubits não são comparados, acessados, medidos ou modificados por essa comparação.

A comparação de igualdade para `Double` valores pode ser enganosa devido a efeitos de arredondamento.
Por exemplo, `49.0 * (1.0/49.0) != 1.0`.

Dadas quaisquer duas expressões numéricas, os operadores binários,, `>` `<` `>=` e `<=` podem ser usados para construir uma nova expressão booliana que seja verdadeira se a primeira expressão for maior que, menor que, maior ou igual ou menor ou igual à segunda expressão.

Dadas quaisquer duas expressões booleanas, use o `and` operador binário para construir uma nova expressão booliana que seja verdadeira se ambas as duas expressões forem verdadeiras. Da mesma forma, usar o `or` operador criará uma expressão que será verdadeira se uma das duas expressões for verdadeira.

Dada qualquer expressão booliana, o `not` operador unário pode ser usado para construir uma nova expressão booliana que seja verdadeira se a expressão constituinte for falsa.

## <a name="string-expressions"></a>Expressões de cadeia de caracteres

Q# permite que as cadeias de caracteres sejam usadas na `fail` instrução (explicada no [fluxo de controle](xref:microsoft.quantum.guide.controlflow#fail-statement)) e na [`Message`](xref:Microsoft.Quantum.Intrinsic.Message) função padrão. O comportamento específico do segundo depende do simulador usado, mas normalmente grava uma mensagem no console do host quando chamado durante um Q# programa.

Cadeias de caracteres no Q# são literais ou cadeias de caracteres interpoladas.

Literais de cadeia de caracteres são semelhantes a literais de cadeia de caracteres simples na maioria dos idiomas: uma sequência de caracteres Unicode entre aspas duplas `" "` .
Dentro de uma cadeia de caracteres, use o caractere de barra invertida `\` para escapar de um caractere de aspas duplas ( `\"` ) ou para inserir uma linha ( `\n` ), um retorno de carro ( `\r` ) ou uma tabulação ( `\t` ).
Por exemplo:

```qsharp
"\"Hello world!\", she said.\n"
```
### <a name="interpolated-strings"></a>Cadeias de caracteres interpoladas

A Q# sintaxe para interpolações de cadeia de caracteres é um subconjunto da sintaxe C#. A seguir estão os principais pontos que pertencem a Q# :

* Para identificar uma literal de cadeia de caracteres como uma cadeia de caracteres interpolada, preceda-o com o símbolo `$`. Não pode haver nenhum espaço em branco entre o `$` e o `"` que inicia uma cadeia de caracteres literal.

* Veja a seguir um exemplo básico usando a [`Message`](xref:Microsoft.Quantum.Intrinsic.Message) função para gravar o resultado de uma medida no console, juntamente com outras Q# expressões.

```qsharp
    let num = 8;       // some Q# expression
    let res = M(q);
    Message($"Number: {num}, Result: {res}");
```

* Qualquer Q# expressão válida pode aparecer em uma cadeia de caracteres interpolada.

* As expressões dentro de uma cadeia de caracteres interpolada seguem a Q# sintaxe, e não a sintaxe C#. A distinção mais notável é que o não Q# oferece suporte a cadeias de caracteres interpoladas (várias linhas) textuais.

Para obter mais detalhes sobre a sintaxe C#, consulte [*cadeias de caracteres interpoladas*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings).

## <a name="range-expressions"></a>Expressões de intervalo

Dadas todas as três `Int` expressões `start` , `step` e `stop` , a expressão `start .. step .. stop` é uma expressão de intervalo cujo primeiro elemento é `start` , o segundo elemento é, o `start+step` terceiro elemento é `start+step+step` , e assim por diante, até que você passe `stop` .
Um intervalo pode estar vazio se, por exemplo, `step` for positivo e `stop < start` .

O intervalo é inclusivo em ambas as extremidades. Ou seja, se a diferença entre `start` e `stop` for um inteiro múltiplo de `step` , o último elemento do intervalo será `stop` .

Dadas as duas `Int` expressões `start` e `stop` , a expressão `start .. stop` é uma expressão de intervalo igual a `start .. 1 .. stop` .
Observe que o implícito `step` é + 1, mesmo se `stop` for menor que `start` ; nesse caso, o intervalo estará vazio.

Alguns intervalos de exemplo são:

- `1..3` é o intervalo 1, 2, 3.
- `2..2..5` é o intervalo de 2, 4.
- `2..2..6` é o intervalo de 2, 4, 6.
- `6..-2..2` é o intervalo de 6, 4, 2.
- `2..1` é o intervalo vazio.
- `2..6..7` é o intervalo 2.
- `2..2..1` é o intervalo vazio.
- `1..-1..2` é o intervalo vazio.

## <a name="qubit-expressions"></a>Expressões qubit

As únicas `Qubit` expressões são símbolos que são associados a `Qubit` valores ou elementos de matriz de `Qubit` matrizes.
Não há `Qubit` literais.

## <a name="pauli-expressions"></a>Expressões Pauli

Os quatro `Pauli` valores, `PauliI` , `PauliX` , `PauliY` e `PauliZ` , são expressões válidas `Pauli` .

Além disso, as únicas `Pauli` expressões são símbolos associados a `Pauli` valores ou elementos de matriz de `Pauli` matrizes.

## <a name="result-expressions"></a>Expressões de resultado

Os dois `Result` valores, `One` e `Zero` , são expressões válidas `Result` .

Além disso, as únicas `Result` expressões são símbolos associados a `Result` valores ou elementos de matriz de `Result` matrizes.
Em particular, observe que `One` não é o mesmo que o inteiro `1` , e não há nenhuma conversão direta entre eles.
O mesmo é verdadeiro para `Zero` e `0` .

## <a name="tuple-expressions"></a>Expressões de tupla

Um literal de tupla é uma sequência de expressões de elemento do tipo apropriado, separadas por vírgulas, delimitadas por parênteses.
Por exemplo, `(1, One)` é uma `(Int, Result)` expressão.

Além de literais, as únicas expressões de tupla são símbolos associados a valores de tupla, elementos de matriz de matrizes de tupla e invocações que retornam tuplas.

## <a name="user-defined-type-expressions"></a>Expressões de tipo de User-Defined

Um literal de um tipo definido pelo usuário consiste no nome do tipo seguido por um literal de tupla do tipo de tupla base do tipo.
Por exemplo, se `IntPair` for um tipo definido pelo usuário baseado em `(Int, Int)` , `IntPair(2, 3)` será um literal válido desse tipo.

Além de literais, as únicas expressões de um tipo definido pelo usuário são símbolos que são associados a valores desse tipo, elementos da matriz de matrizes desse tipo e invocações que retornam esse tipo.

## <a name="unwrap-expressions"></a>Desencapsular expressões

No Q# , o operador de desencapsulamento é um ponto de exclamação à direita `!` .
Por exemplo, se `IntPair` for um tipo definido pelo usuário com o tipo subjacente `(Int, Int)` e `s` for uma variável com valor `IntPair(2, 3)` , `s!` será `(2, 3)` .

Para tipos definidos pelo usuário definidos em termos de outros tipos definidos pelo usuário, você pode repetir o operador de desencapsulamento. Por exemplo, `s!!` indica o valor duplo não encapsulado de `s` .
Portanto, se `WrappedPair` for um tipo definido pelo usuário com o tipo subjacente `IntPair` , e `t` for uma variável com valor `WrappedPair(IntPair(1,2))` , `t!!` será `(1,2)` .

O `!` operador tem precedência maior do que todos os outros operadores diferentes de `[]` para indexação e divisão de matriz.
`!` e `[]` Associate posicionalmente, ou seja, `a[i]![3]` é lido como `((a[i])!)[3]` : Pegue o `i` elemento th `a` , desenvolva-o e, em seguida, obtenha o terceiro elemento do valor não encapsulado (que deve ser uma matriz).

A precedência do `!` operador tem um impacto que pode não ser óbvio.
Se uma função ou operação retorna um valor que, em seguida, é desencapsulada, a função ou a chamada de operação deve ser colocada entre parênteses para que a tupla de argumento seja associada à chamada em vez de ser desencapsulada.
Por exemplo:

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a>Expressões de matriz

Um literal de matriz é uma sequência de uma ou mais expressões de elemento, separadas por vírgulas, delimitadas entre colchetes `[]` .
Todos os elementos devem ser compatíveis com o mesmo tipo.

Dadas duas matrizes do mesmo tipo, use o `+` operador Binary para formar uma nova matriz que é a concatenação das duas matrizes.
Por exemplo, `[1,2,3] + [4,5,6]` = `[1,2,3,4,5,6]`.

### <a name="array-creation"></a>Criação de matriz

Dado um tipo e uma `Int` expressão, use o `new` operador para alocar uma nova matriz do tamanho determinado.
Por exemplo, `new Int[i + 1]` aloca uma nova `Int` matriz com `i + 1` elementos.

Literais de matriz vazios, como `[]` , não são permitidos.
Em vez disso, você pode criar uma matriz de comprimento zero usando `new T[0]` , em que `T` é um espaço reservado para um tipo adequado.

Os elementos de uma nova matriz são inicializados para um valor padrão dependente de tipo.
Na maioria dos casos, essa é uma variação de zero.

Para qubits e callableies, que são referências a entidades, não há nenhum valor padrão razoável.
Portanto, para esses tipos, o padrão é uma referência inválida que você não pode usar sem causar um erro de tempo de execução, semelhante a uma referência nula em linguagens como C# ou Java.
As matrizes que contêm qubits ou callables devem ser inicializadas com valores não padrão antes de você poder usar seus elementos com segurança. Para rotinas de inicialização adequadas, consulte <xref:Microsoft.Quantum.Arrays> .

Os valores padrão para cada tipo são:

Type | Padrão
---------|----------
 `Int` | `0`
 `BigInt` | `0L`
 `Double` | `0.0`
 `Bool` | `false`
 `String` | `""`
 `Qubit` | _qubit inválido_
 `Pauli` | `PauliI`
 `Result` | `Zero`
 `Range` | O intervalo vazio, `1..1..0`
 `Callable` | _callable inválido_
 `Array['T]` | `'T[0]`

Os tipos de tupla inicializam elemento por elemento.


### <a name="array-elements"></a>Elementos da matriz

Dada uma expressão de matriz e uma `Int` expressão, formam uma nova expressão usando o operador de elemento de matriz `[]` .
A nova expressão é do mesmo tipo que o tipo de elemento da matriz.
Por exemplo, se `a` estiver associado a uma matriz do tipo `Double` , `a[4]` será uma `Double` expressão.

Se a expressão de matriz não for um identificador simples, você deverá colocá-la entre parênteses para selecionar um elemento.
Por exemplo, se `a` e `b` forem ambas matrizes do tipo `Int` , um elemento da concatenação será expresso como:

```qsharp
(a + b)[13]
```

Todas as matrizes no Q# são baseadas em zero.
Ou seja, o primeiro elemento de uma matriz `a` é sempre `a[0]` .


### <a name="array-slices"></a>Fatias de matriz

Dada uma expressão de matriz e uma `Range` expressão, formam uma nova expressão usando o operador matriz de fatia `[ ]` .
A nova expressão é do mesmo tipo que a matriz e contém os itens de matriz indexados pelos elementos de `Range` , na ordem definida pelo `Range` .
Por exemplo, se `a` estiver associado a uma matriz do tipo `Double` , `a[3..-1..0]` é uma `Double[]` expressão que contém os quatro primeiros elementos de `a` , mas na ordem inversa, conforme eles aparecem `a` .

Se o `Range` estiver vazio, a fatia da matriz resultante terá comprimento zero.

Assim como ocorre com a referência de elementos de matriz, se a expressão de matriz não for um identificador simples, você deverá colocá-la entre parênteses para dividir a tabela.
Por exemplo, se `a` e `b` forem ambas matrizes do tipo `Int` , uma fatia da concatenação será expressa como:

```qsharp
(a+b)[1..2..7]
```

#### <a name="inferred-startend-values"></a>Valores de início/término inferidos

A partir da nossa [versão 0,8](xref:microsoft.quantum.relnotes), damos suporte a expressões contextuais para divisão de intervalo. Em particular, você pode omitir os valores de início e término do intervalo no contexto de uma expressão de divisão de intervalo. Nesse caso, o compilador aplica as seguintes regras para inferir os delimitadores pretendidos para o intervalo:

* Se o valor de *início* do intervalo for omitido, o valor inicial inferido
  * será zero se nenhuma etapa for especificada ou se a etapa especificada for positiva.  
  * é o comprimento da matriz segmentada menos uma se a etapa especificada é negativa.

* Se o valor *final* do intervalo for omitido, o valor final inferido
  * é o comprimento da matriz segmentada menos uma se nenhuma etapa for especificada ou a etapa especificada for positiva.
  * será zero se a etapa especificada for negativa.

Alguns exemplos são:

```qsharp
let arr = [1,2,3,4,5,6];
let slice1  = arr[3...];      // slice1 is [4,5,6];
let slice2  = arr[0..2...];   // slice2 is [1,3,5];
let slice3  = arr[...2];      // slice3 is [1,2,3];
let slice4  = arr[...2..3];   // slice4 is [1,3];
let slice5  = arr[...2...];   // slice5 is [1,3,5];
let slice7  = arr[4..-2...];  // slice7 is [5,3,1];
let slice8  = arr[...-1..3];  // slice8 is [6,5,4];
let slice9  = arr[...-1...];  // slice9 is [6,5,4,3,2,1];
let slice10 = arr[...];       // slice10 is [1,2,3,4,5,6];
```

### <a name="copy-and-update-expressions"></a>Expressões Copy-and-Update

Como todos os Q# tipos são tipos de valor (com o qubits que assume uma função especial), formalmente uma "cópia" é criada quando um valor é associado a um símbolo ou quando um símbolo é reassociado. Isso significa que o comportamento do Q# é o mesmo que se uma cópia fosse criada usando um operador de atribuição. 

É claro que, na prática, apenas as partes relevantes são recriadas conforme necessário. Isso afeta a maneira como você copia matrizes porque não é possível atualizar itens de matriz. Para modificar uma matriz existente, é necessário aproveitar um mecanismo de *copiar e atualizar* .

Você pode criar uma nova matriz de uma matriz existente por meio de expressões de *copiar e atualizar* , que usam os `w/` operadores `<-` e.
Uma expressão de copiar e atualizar é uma expressão do formulário `expression1 w/ expression2 <- expression3` , em que

* `expression1` deve ser tipo `T[]` para algum tipo `T` .
* `expression2` define quais índices na matriz especificados em `expression1` para modificar. `expression2` deve ser tipo `Int` ou tipo `Range` .
* `expression3` são os valores usados para atualizar elementos no `expression1` , com base nos índices especificados em `expression2` . Se `expression2` for Type `Int` , `expression3` deverá ser Type `T` . Se `expression2` for Type `Range` , `expression3` deverá ser Type `T[]` .

Por exemplo, a expressão Copy-and-update `arr w/ idx <- value` constrói uma nova matriz com todos os elementos definidos para os elementos correspondentes no `arr` , exceto para o elemento especificado por `idx` , que é definido como o (s) valor (es) em `value` . 

Fornecido `arr` contém a matriz `[0,1,2,3]` , então 

- `arr w/ 0 <- 10` é a matriz `[10,1,2,3]` .
- `arr w/ 2 <- 10` é a matriz `[0,1,10,3]` .
- `arr w/ 0..2..3 <- [10,12]` é a matriz `[10,1,12,3]` .

#### <a name="copy-and-update-expressions-for-named-items"></a>Copiar e atualizar expressões para itens nomeados

Existem expressões semelhantes para itens nomeados em tipos definidos pelo usuário. 

Por exemplo, considere o tipo 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
Se `c` contiver o valor do tipo `Complex(1., -1.)` , `c w/ Re <- 0.` será uma expressão do tipo `Complex` que é avaliada como `Complex(0., -1.)` .

### <a name="jagged-arrays"></a>Matrizes denteadas

Uma matriz denteada, às vezes chamada de "matriz de matrizes", é uma matriz cujos elementos são matrizes.
Os elementos de uma matriz denteada podem ser de tamanhos diferentes.
O exemplo a seguir mostra como declarar e inicializar uma matriz denteada que representa uma tabela de multiplicação.

```qsharp
let N = 4;
mutable multiplicationTable = new Int[][N];
for (i in 1..N) {
    mutable row = new Int[i];
    for (j in 1..i) {
        set row w/= j-1 <- i * j;
    }
    set multiplicationTable w/= i-1 <- row;
}
```

### <a name="arrays-of-callables"></a>Matrizes de callablefiles 

Você também pode criar uma matriz de chamadores.

* Se o tipo de elemento comum for uma operação ou tipo de função, todos os elementos deverão ter os mesmos tipos de entrada e saída.
* O tipo de elemento da matriz dá suporte a qualquer [transmissão functors](xref:microsoft.quantum.guide.operationsfunctions) que tenha suporte de todos os elementos.
Por exemplo, If `Op1` , `Op2` e `Op3` All são `Qubit[] => Unit` operações, mas `Op1` dá suporte a, dá suporte a `Adjoint` `Op2` `Controlled` e `Op3` dá suporte a ambos:
  * `[Op1, Op2]` é uma matriz de `(Qubit[] => Unit)` operações.
  * `[Op1, Op3]` é uma matriz de `(Qubit[] => Unit is Adj)` operações.
  * `[Op2, Op3]` é uma matriz de `(Qubit[] => Unit is Ctl)` operações.

No entanto, enquanto as operações `(Qubit[] => Unit is Adj)` e  `(Qubit[] => Unit is Ctl)` têm o tipo base comum de `(Qubit[] => Unit)` , as *matrizes* dessas operações não compartilham um tipo base comum.

Por exemplo, `[[Op1], [Op2]]` no momento, o geraria um erro porque ele tenta criar uma matriz dos dois tipos de matriz incompatíveis `(Qubit[] => Unit is Adj)[]` e `(Qubit[] => Unit is Ctl)[]` .

Para obter mais informações sobre o callables, consulte [expressões chamáveis](#callable-expressions) nesta página ou [operações e Q# funções no ](xref:microsoft.quantum.guide.operationsfunctions).

## <a name="conditional-expressions"></a>Expressões condicionais

Dadas duas expressões do mesmo tipo e uma expressão booleana, formate uma expressão condicional usando o ponto de interrogação, `?` e a barra vertical `|` . Dado `a==b ? c | d` , o valor da expressão condicional é `c` se `a==b` for true e `d` se for false.

### <a name="conditional-expressions-with-callables"></a>Expressões condicionais com callablefiles

Expressões condicionais podem ser avaliadas como operações que têm as mesmas entradas e saídas, mas dão suporte a diferentes transmissão functors. Nesse caso, o tipo da expressão condicional é uma operação com entradas e saídas que dão suporte a qualquer transmissão functors com suporte em ambas as expressões.
Por exemplo, se `Op1` , `Op2` , e `Op3` todos forem `Qubit[]=>Unit` , mas o oferecer suporte a, o oferece suporte a `Op1` `Adjoint` `Op2` `Controlled` , e `Op3` dá suporte a ambos:

- `flag ? Op1 | Op2` é uma `(Qubit[] => Unit)` operação.
- `flag ? Op1 | Op3` é uma `(Qubit[] => Unit is Adj)` operação.
- `flag ? Op2 | Op3` é uma `(Qubit[] => Unit is Ctl)` operação.

Se qualquer uma das duas expressões de resultado possíveis incluir uma função ou uma chamada de operação, essa chamada só ocorrerá se o resultado for aquele que é o valor da chamada. Por exemplo, no caso `a==b ? C(qs) | D(qs)` , se `a==b` for true, a `C` operação será invocada e, se for false, somente a `D` operação será invocada. Essa abordagem é semelhante ao *curto circuito* em outras linguagens.

## <a name="callable-expressions"></a>Expressões que podem ser chamadas

Um literal que pôde ser chamado é o nome de uma operação ou função definida no escopo de compilação. Por exemplo, `X` é um literal de operação que se refere à operação de biblioteca padrão `X` e `Message` é um literal de função que se refere à função de biblioteca padrão `Message` .

Se uma operação oferecer suporte a `Adjoint` functor, `Adjoint op` será uma expressão de operação.
Da mesma forma, se a operação oferecer suporte a `Controlled` functor, `Controlled op` será uma expressão de operação.
Para obter mais informações sobre os tipos dessas expressões, consulte [chamando especializações de operação](xref:microsoft.quantum.guide.operationsfunctions#calling-operation-specializations).

Transmissão functors ( `Adjoint` e `Controlled` ) associam-se mais de todos os outros operadores, exceto para o operador de desencapsulamento `!` e a indexação de matriz com `[ ]` .
Portanto, as seguintes são todas válidas, supondo que as operações suportam o transmissão functors usado:

```qsharp
Adjoint Op(qs)
Controlled Op(controls, targets)
Controlled Adjoint Op(controls, targets)
Adjoint WrappedOp!(qs)
```

### <a name="type-parameterized-callable-expressions"></a>Expressões callable parametrizadas de tipo

Você pode usar um literal chamável como um valor, por exemplo, para atribuí-lo a uma variável ou passá-lo para outro callable. Nesse caso, se o callable tiver [parâmetros de tipo](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables), você deverá fornecer os parâmetros como parte do valor que pode ser chamado.

Um valor callable não pode ter nenhum parâmetro de tipo não especificado. Por exemplo, se `Fun` for uma função com a assinatura `'T1->Unit` :

```qsharp
let f = Fun<Int>;            // f is (Int->Unit).
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun<Double>);   // A (Double->Unit) is passed to SomeOtherFun.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a>Expressões de invocação que podem ser chamadas

Dada uma expressão resgatável (operação ou função) e uma expressão de tupla do tipo de entrada da assinatura do callable, você pode formar uma *expressão de invocação* acrescentando a expressão de tupla à expressão que pode ser chamada.
O tipo da expressão de invocação é o tipo de saída da assinatura do callable.

Por exemplo, se `Op` for uma operação com a assinatura `((Int, Qubit) => Double)` , `Op(3, qubit1)` será uma expressão do tipo `Double` .
Da mesma forma, se `Sin` for uma função com a assinatura `(Double -> Double)` , `Sin(0.1)` será uma expressão do tipo `Double` .
Por fim, se `Builder` for uma função com a assinatura `(Int -> (Int -> Int))` , `Builder(3)` será uma função de `Int` para `Int` .

Invocar o resultado de uma expressão com valor callable requer um par extra de parênteses em volta da expressão callable.
Portanto, para invocar o resultado da chamada `Builder` do parágrafo anterior, a sintaxe correta é:

```qsharp
(Builder(3))(2)
```

Ao invocar um callable [-parametrizado de tipo](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) , você pode especificar os parâmetros de tipo reais dentro de colchetes angulares `< >` após a expressão que pode ser chamada.
Normalmente, essa ação é desnecessária, pois o Q# compilador infere os tipos reais.
No entanto, ele *será* necessário para o [aplicativo parcial](xref:microsoft.quantum.guide.operationsfunctions#partial-application) se um argumento de tipo parametrizado for deixado não especificado.
Ele também é útil ao passar operações com suporte diferente para o functor para um callable.

Por exemplo, se `Func` tem assinatura e tem assinatura e `('T1, 'T2, 'T1) -> 'T2` `Op1` `Op2` `(Qubit[] => Unit is Adj)` `Op3` tem assinatura `(Qubit[] => Unit)` , para invocar `Func` com `Op1` como o primeiro argumento, `Op2` como o segundo, e `Op3` como o terceiro:

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

A especificação de tipo é necessária porque `Op3` e `Op1` tem tipos diferentes, portanto, o compilador tratará isso como ambíguo sem a especificação.


## <a name="operator-precedence"></a>Precedência de operador

* Todos os operadores binários são associativos à direita, exceto para `^` .

* Colchetes, `[ ]` , para a divisão e a indexação de matriz, associe antes de qualquer operador.

* A transmissão functors `Adjoint` e a `Controlled` Associação após a indexação da matriz, mas antes de todos os outros operadores.

* Parênteses para operação e invocação de função também são associados antes de qualquer operador, mas após a indexação de matriz e transmissão functors.

Q# operadores em ordem de precedência, do mais alto ao mais baixo:

Operador | Arity | Descrição | Tipos de operando
---------|----------|---------|---------------
 à direita `!` | Unário | Desencapsular | Qualquer tipo definido pelo usuário
 `-`, `~~~`, `not` | Unário | Numérico negativo, complemento de bit-nte, negação lógica | `Int`, `BigInt` ou `Double` para `-` , `Int` ou `BigInt` para `~~~` , `Bool` para `not`
 `^` | Binário | Potência de inteiro | `Int` ou `BigInt` para a base, `Int` para o expoente
 `/`, `*`, `%` | Binário | Divisão, multiplicação, módulo de inteiro | `Int`, `BigInt` ou `Double` para `/` e `*` , `Int` ou `BigInt` para `%`
 `+`, `-` | Binário | Adição ou concatenação de cadeia de caracteres e matriz, subtração | `Int`, `BigInt` ou `Double` , além disso, `String` ou qualquer tipo de matriz para `+`
 `<<<`, `>>>` | Binário | Deslocamento à esquerda, deslocamento à direita | `Int` ou `BigInt`
 `<`, `<=`, `>`, `>=` | Binário | Comparações de menor que, menor que ou igual a, maior que, maior que ou igual a | `Int`, `BigInt` ou `Double`
 `==`, `!=` | Binário | comparações iguais, não iguais | qualquer tipo primitivo
 `&&&` | Binário | AND bit a bit | `Int` ou `BigInt`
 `^^^` | Binário | XOR bit a bit | `Int` ou `BigInt`
 <code>\|\|\|</code> | Binário | OR bit a bit | `Int` ou `BigInt`
 `and` | Binário | AND lógico | `Bool`
 `or` | Binário | OR lógico | `Bool`
 `..` | Binary/ternário | Operador de intervalo | `Int`
 `?` `|` | Ternário | Condicional | `Bool` para o lado esquerdo
`w/` `<-` | Ternário | Copiar e atualizar | Consulte [expressões de copiar e atualizar](#copy-and-update-expressions)

## <a name="next-steps"></a>Próximas etapas

Agora que você pode trabalhar com expressões no Q# , vá para [operações e funções Q# no](xref:microsoft.quantum.guide.operationsfunctions) para saber como definir e chamar operações e funções.
