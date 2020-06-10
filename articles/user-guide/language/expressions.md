---
title: 'Expressões de tipo em Q #'
description: 'Entenda como especificar, referenciar e combinar constantes, variáveis, operadores, operações e funções como expressões em Q #.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.expressions
ms.openlocfilehash: b32644382bb88fb11da00d0d7d78bbd797a0eaaa
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2020
ms.locfileid: "84629992"
---
# <a name="type-expressions-in-q"></a>Expressões de tipo em Q #

## <a name="numeric-expressions"></a>Expressões numéricas

Expressões numéricas são expressões do tipo `Int` , `BigInt` ou `Double` .
Ou seja, eles são números inteiros ou de ponto flutuante.

`Int`os literais em Q # são escritos simplesmente como uma sequência de dígitos.
Os inteiros hexadecimais e binários têm suporte com `0x` um `0b` prefixo e, respectivamente.

`BigInt`os literais em Q # são gravados com um `l` sufixo ou à direita `L` .
Há suporte para inteiros grandes hexadecimais com um prefixo "0x".
Portanto, veja a seguir todos os usos válidos de `BigInt` literais:

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

`Double`literais em Q # são números de ponto flutuante gravados usando dígitos decimais.
Eles podem ser escritos com um ponto decimal, `.` e/ou uma parte exponencial indicada com ' e ' ou ' e ' (após o qual apenas um possível sinal negativo e dígitos decimais são válidos).
Os seguintes são `Double` literais válidos: `0.0` , `1.2e5` , `1e-5` .

Dada uma expressão de matriz de qualquer tipo de elemento, uma `Int` expressão pode ser formada usando a [`Length`](xref:microsoft.quantum.core.length) função interna, com a expressão de matriz entre parênteses `(` e `)` .
Por exemplo, se `a` estiver associado a uma matriz, `Length(a)` será uma expressão de inteiro.
Se `b` é uma matriz de matrizes de inteiros, `Int[][]` , `Length(b)` é o número de submatrizes em `b` e `Length(b[1])` é o número de inteiros na segunda submatriz no `b` .

Dadas duas expressões numéricas do mesmo tipo, os operadores binários,, `+` `-` `*` e `/` podem ser usados para formar uma nova expressão numérica.
O tipo da nova expressão será o mesmo que os tipos das expressões constituintes.

Dadas duas expressões de inteiro, o operador binário `^` (potência) pode ser usado para formar uma nova expressão de inteiro.
Da mesma forma, `^` pode ser usado com duas expressões duplas para formar uma nova expressão Double.
Por fim, `^` pode ser usado com um inteiro grande à esquerda e um inteiro à direita para formar uma nova expressão de inteiro grande.
Nesse caso, o segundo parâmetro deve caber em 32 bits; caso contrário, um erro de tempo de execução será gerado.

Dadas duas expressões de inteiro ou grandes inteiros, um novo inteiro ou uma expressão de inteiro grande pode ser formada usando os `%` operadores (módulo), `&&&` (bit e), (OR-bit or `|||` ) ou `^^^` (XOR).

Dado um inteiro ou uma expressão de inteiro grande à esquerda e uma expressão de inteiro à direita, os `<<<` operadores (deslocamento aritmético à esquerda) ou `>>>` (deslocamento aritmético à direita) podem ser usados para criar uma nova expressão com o mesmo tipo que a expressão esquerda.

O segundo parâmetro (o valor de deslocamento) para a operação de deslocamento deve ser maior ou igual a zero; o comportamento para valores de deslocamento negativos é indefinido.
O valor de deslocamento para uma das operações de deslocamento também deve se ajustar a 32 bits; caso contrário, um erro de tempo de execução será gerado.
Se o número a ser deslocado for um inteiro, o valor de deslocamento será interpretado `mod 64` ; ou seja, um deslocamento de 1 e um deslocamento de 65 terão o mesmo efeito.

Para os valores inteiros e inteiros grandes, as turnos são aritméticas.
A mudança de um valor negativo para a esquerda ou direita resultará em um número negativo.
Ou seja, mudar uma etapa para a esquerda ou para a direita é exatamente o mesmo que multiplicar ou dividir por 2, respectivamente.

Divisão de inteiros e módulo de inteiro seguem o mesmo comportamento para números negativos em C#.
Ou seja, `a % b` sempre terá o mesmo sinal de `a` e `b * (a / b) + a % b` sempre será igual `a` .
Por exemplo:

 `A` | `B` | `A / B` | `A % B`
---------|----------|---------|---------
 5 | 2 | 2 | 1
 5 | -2 | -2 | 1
 -5 | 2 | -2 | -1
 -5 | -2 | 2 | -1

Divisão de inteiro grande e módulo funciona da mesma maneira.

Dada qualquer expressão numérica, uma nova expressão pode ser formada usando o `-` operador unário.
A nova expressão será o mesmo tipo da expressão constituinte.

Devido a qualquer inteiro ou expressão de inteiro grande, uma nova expressão do mesmo tipo pode ser formada usando o `~~~` operador unário (complemento de bits).

## <a name="boolean-expressions"></a>Expressões boolianas

Os dois `Bool` valores literais são `true` e `false` .

Dadas as duas expressões do mesmo tipo primitivo, os `==` `!=` operadores binários e podem ser usados para construir uma `Bool` expressão.
A expressão será true se as duas expressões forem iguais e false se não.

Os valores de tipos definidos pelo usuário não podem ser comparados, apenas seus valores não encapsulados podem ser comparados. Por exemplo, usando o operador "sem encapsulamento" `!` (explicado em detalhes em [tipos em Q #](xref:microsoft.quantum.guide.types#access-anonymous-items-with-the-unwrap-operator)),

```qsharp
newtype WrappedInt = Int;     // Yes, this is a contrived example
let x = WrappedInt(1);
let y = WrappedInt(2);
let z = x! == y!;             // This will compile and yield z = false.
let t = x == y;               // This will cause a compiler error.
```

A comparação de igualdade para `Qubit` valores é igualdade de identidade; ou seja, se as duas expressões identificam o mesmo qubit.
O estado dos dois qubits não são comparados, acessados, medidos ou modificados por essa comparação.

A comparação de igualdade para `Double` valores pode ser enganosa devido a efeitos de arredondamento.
Por exemplo, `49.0 * (1.0/49.0) != 1.0` .

Dadas quaisquer duas expressões numéricas, os operadores binários,, `>` `<` `>=` e `<=` podem ser usados para construir uma nova expressão booliana que seja verdadeira se a primeira expressão for maior que, menor que, maior ou igual ou menor ou igual à segunda expressão.

Dadas quaisquer duas expressões booleanas, os `and` `or` operadores binários e podem ser usados para construir uma nova expressão booliana que seja verdadeira se ambos (resp. ou ambos) as duas expressões forem true.

Dada qualquer expressão booliana, o `not` operador unário pode ser usado para construir uma nova expressão booliana que seja verdadeira se a expressão constituinte for falsa.

## <a name="string-expressions"></a>Expressões de cadeia de caracteres

Q # permite que as cadeias de caracteres sejam usadas na `fail` instrução (explicada em [fluxo de controle](xref:microsoft.quantum.guide.controlflow#fail-statement)) e na [`Message`](xref:microsoft.quantum.intrinsic.message) função padrão.
O comportamento específico do segundo depende do simulador que está sendo usado, mas normalmente grava uma mensagem no console do host quando chamado durante um programa Q #.

Cadeias de caracteres em Q # são literais ou cadeias de caracteres interpoladas.

Literais de cadeia de caracteres são semelhantes a literais de cadeia de caracteres simples na maioria dos idiomas: uma sequência de caracteres Unicode entre aspas duplas, `"` .
Dentro de uma cadeia de caracteres, o caractere de barra invertida `\` pode ser usado para escapar de um caractere de aspas duplas e para inserir uma linha nova como `\n` , um retorno de carro como `\r` e uma tabulação como `\t` .
Por exemplo:

```qsharp
"\"Hello world!\", she said.\n"
```
### <a name="interpolated-strings"></a>Cadeias de caracteres interpoladas

A sintaxe de Q # para interpolações de cadeia de caracteres é um subconjunto da sintaxe do C#, mas resumimos aqui os pontos principais conforme eles pertencem a Q #.
As distinções principais são discutidas abaixo.

Para identificar uma literal de cadeia de caracteres como uma cadeia de caracteres interpolada, preceda-o com o símbolo `$`.
Você não pode ter nenhum espaço em branco entre o `$` e o `"` que inicia uma cadeia de caracteres literal.

Veja a seguir um exemplo básico usando a [`Message`](xref:microsoft.quantum.intrinsic.message) função para gravar o resultado de uma medida no console, juntamente com outras expressões Q #.

```qsharp
    let num = 8;       // some Q# expression
    let res = M(q);
    Message($"Number: {num}, Result: {res}");
```
Qualquer expressão Q # válida pode aparecer em uma cadeia de caracteres interpolada.

Mais detalhes sobre a sintaxe do C# podem ser encontrados em [*cadeias de caracteres interpoladas*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings).
A distinção mais notável é que Q # não oferece suporte a cadeias de caracteres interpoladas (várias linhas) textuais.
As expressões dentro de uma cadeia de caracteres interpolada seguem a sintaxe Q #, e não a sintaxe C#.

## <a name="range-expressions"></a>Expressões de intervalo

Dadas as três `Int` expressões `start` , `step` e `stop` , `start .. step .. stop` é uma expressão de intervalo cujo primeiro elemento é `start` , o segundo elemento é, o `start+step` terceiro elemento é `start+step+step` , etc., até que `stop` seja passado.
Um intervalo pode estar vazio se, por exemplo, `step` for positivo e `stop < start` .
O último elemento do intervalo será `stop` se a diferença entre `start` e `stop` for um múltiplo integral de `step` ; ou seja, o intervalo é inclusivo em ambas as extremidades.

Dadas as duas `Int` expressões `start` e `stop` , `start .. stop` é uma expressão de intervalo igual a `start .. 1 .. stop` .
Observe que o implícito `step` é + 1, mesmo se `stop` for menor que `start` ; nesse caso, o intervalo estará vazio.

Alguns intervalos de exemplo são:

- `1..3`é o intervalo 1, 2, 3.
- `2..2..5`é o intervalo de 2, 4.
- `2..2..6`é o intervalo de 2, 4, 6.
- `6..-2..2`é o intervalo de 6, 4, 2.
- `2..1`é o intervalo vazio.
- `2..6..7`é o intervalo 2.
- `2..2..1`é o intervalo vazio.
- `1..-1..2`é o intervalo vazio.

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

Um literal de tupla é uma sequência de expressões de elemento do tipo apropriado, separados por vírgulas, colocadas em `(` e `)` .
Por exemplo, `(1, One)` é uma `(Int, Result)` expressão.

Além de literais, as únicas expressões de tupla são símbolos associados a valores de tupla, elementos de matriz de matrizes de tupla e invocações que retornam tuplas.

## <a name="user-defined-type-expressions"></a>Expressões de tipo definidas pelo usuário

Um literal de um tipo definido pelo usuário consiste no nome do tipo seguido por um literal de tupla do tipo de tupla base do tipo.
Por exemplo, se `IntPair` for um tipo definido pelo usuário com base em `(Int, Int)` , `IntPair(2, 3)` seria um literal válido desse tipo.

Além de literais, as únicas expressões de um tipo definido pelo usuário são símbolos que são associados a valores desse tipo, elementos da matriz de matrizes desse tipo e invocações que retornam esse tipo.

## <a name="unwrap-expressions"></a>Desencapsular expressões

Em Q #, o operador de desencapsulamento é um ponto de exclamação à direita `!` .
Por exemplo, se `IntPair` é um tipo definido pelo usuário com o tipo subjacente `(Int, Int)` e `s` era uma variável com valor `IntPair(2, 3)` , `s!` seria `(2, 3)` .

Para tipos definidos pelo usuário definidos em termos de outros tipos definidos pelo usuário, o operador de desencapsulamento pode ser repetido; por exemplo, `s!!` indica o valor duplo não encapsulado de `s` .
Portanto, se `WrappedPair` for um tipo definido pelo usuário com o tipo subjacente `IntPair` , e `t` for uma variável com valor `WrappedPair(IntPair(1,2))` , será `t!!` `(1,2)` .

O `!` operador tem precedência maior do que todos os outros operadores diferentes de `[]` para indexação e divisão de matriz.
`!`e `[]` Associate posicionalmente, ou seja, `a[i]![3]` deve ser lido como `((a[i])!)[3]` : pegar o `i` ' th element ' `a` , desencapsulá-lo e, em seguida, obter o terceiro elemento do valor não encapsulado (que deve ser uma matriz).

A precedência do `!` operador tem um impacto que pode não ser óbvio.
Se uma função ou operação retorna um valor que, em seguida, é desencapsulada, a função ou a chamada de operação deve ser colocada entre parênteses para que a tupla de argumento seja associada à chamada em vez de ser desencapsulada.
Por exemplo:

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a>Expressões de matriz

Um literal de matriz é uma sequência de uma ou mais expressões de elemento, separadas por vírgulas, colocadas em `[` e `]` .
Todos os elementos devem ser compatíveis com o mesmo tipo.

Dadas duas matrizes do mesmo tipo, o `+` operador binário pode ser usado para formar uma nova matriz que é a concatenação das duas matrizes.
Por exemplo, `[1,2,3] + [4,5,6]` é `[1,2,3,4,5,6]` .

### <a name="array-creation"></a>Criação de matriz

Dado um tipo e uma `Int` expressão, o `new` operador pode ser usado para alocar uma nova matriz do tamanho determinado.
Por exemplo, `new Int[i + 1]` alocaria uma nova `Int` matriz com `i + 1` elementos.

Literais de matriz vazios, `[]` , não são permitidos.
Em vez disso, o uso de `new ★[0]` , onde `★` é o espaço reservado para um tipo adequado, permite criar a matriz desejada de comprimento zero.

Os elementos de uma nova matriz são inicializados para um valor padrão dependente de tipo.
Na maioria dos casos, essa é uma variação de zero.

Para qubits e callableies, que são referências a entidades, não há nenhum valor padrão razoável.
Portanto, para esses tipos, o padrão é uma referência inválida que não pode ser usada sem causar um erro de tempo de execução.
Isso é semelhante a uma referência nula em linguagens como C# ou Java.
As matrizes que contêm qubits ou callables devem ser inicializadas corretamente com valores não padrão antes que seus elementos possam ser usados com segurança. Rotinas de inicialização adequadas podem ser encontradas em <xref:microsoft.quantum.arrays> .

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
 `Range` | O intervalo vazio,`1..1..0`
 `Callable` | _callable inválido_
 `Array['T]` | `'T[0]`

Os tipos de tupla são inicializados elemento por elemento.


### <a name="array-elements"></a>Elementos da matriz

Dada uma expressão de matriz e uma `Int` expressão, uma nova expressão pode ser formada usando o `[` operador de elemento de matriz e `]` .
A nova expressão será do mesmo tipo que o tipo de elemento da matriz.
Por exemplo, se `a` estiver associado a uma matriz de `Double` s, `a[4]` será uma `Double` expressão.

Se a expressão de matriz não for um identificador simples, ela deverá ser colocada entre parênteses para selecionar um elemento.
Por exemplo, se `a` e `b` forem ambas matrizes de `Int` s, um elemento da concatenação seria expresso como:

```qsharp
(a + b)[13]
```

Todas as matrizes em Q # são baseadas em zero.
Ou seja, o primeiro elemento de uma matriz `a` é sempre `a[0]` .


### <a name="array-slices"></a>Fatias de matriz

Dada uma expressão de matriz e uma `Range` expressão, uma nova expressão pode ser formada usando o `[` `]` operador matriz de fatia e.
A nova expressão será do mesmo tipo que a matriz e conterá os itens de matriz indexados pelos elementos de `Range` , na ordem definida pelo `Range` .
Por exemplo, se `a` estiver associado a uma matriz de `Double` s, `a[3..-1..0]` será uma `Double[]` expressão que contém os quatro primeiros elementos de, `a` mas na ordem inversa, conforme aparecem `a` .

Se o `Range` estiver vazio, a fatia da matriz resultante será de comprimento zero.

Assim como ocorre com a referência de elementos de matriz, se a expressão de matriz não for um identificador simples, ela deverá ser colocada entre parênteses, para fatiar.
Se `a` e `b` forem ambas matrizes de `Int` s, uma fatia da concatenação seria expressa como:

```qsharp
(a+b)[1..2..7]
```

#### <a name="inferred-startend-values"></a>Valores de início/término inferidos

A partir da nossa versão 0,8, damos suporte a expressões contextuais para divisão de intervalo. Em particular, os valores de início e término do intervalo podem ser omitidos no contexto de uma expressão de divisão do intervalo. Nesse caso, o compilador aplicará as regras a seguir para inferir os delimitadores pretendidos para o intervalo. 

Por exemplo, se o valor de início do intervalo for omitido, o valor inicial inferido 
- será zero se nenhuma etapa for especificada ou a etapa especificada for positiva e 
- é o comprimento da matriz segmentada menos uma se a etapa especificada for negativa. 

Se o valor final do intervalo for omitido, o valor final inferido 
- é o comprimento da matriz segmentada menos uma se nenhuma etapa for especificada ou a etapa especificada for positiva e 
- será zero se a etapa especificada for negativa. 

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

Como todos os tipos de Q # são tipos de valor — com o qubits usando uma função especial, formalmente, uma "cópia" é criada quando um valor é associado a um símbolo ou quando um símbolo é reassociado. Isso significa que o comportamento de Q # é o mesmo que se uma cópia fosse criada na atribuição.
É claro que, na prática, apenas as partes relevantes são, na verdade, recriadas, conforme necessário. 

Isso, em particular, também inclui matrizes.
Em particular, não é possível atualizar itens de matriz. Para modificar uma matriz existente, é necessário aproveitar um mecanismo de *copiar e atualizar* .

Novas matrizes podem ser criadas a partir de existentes por meio de expressões *de copiar e atualizar* .
Uma expressão de copiar e atualizar é uma expressão do formulário `expression1 w/ expression2 <- expression3` , onde `expression1` deve ser do tipo `T[]` para algum tipo `T` .
O segundo `expression2` define os índices dos elementos a serem modificados em comparação com a matriz em `expression1` e deve ser do tipo `Int` ou do tipo `Range` .
Se `expression2` for do tipo `Int` , `expression3` deve ser do tipo `T` . Se `expression2` for do tipo `Range` , `expression3` deve ser do tipo `T[]` .

Uma expressão de copiar e atualizar `arr w/ idx <- value` constrói uma nova matriz com todos os elementos definidos para o elemento correspondente no `arr` , exceto para os elementos em `idx` , que são definidos como os (s) em `value` . Por exemplo, se `arr` contiver uma matriz `[0,1,2,3]` , 
- `arr w/ 0 <- 10`é a matriz `[10,1,2,3]` .
- `arr w/ 2 <- 10`é a matriz `[0,1,10,3]` .
- `arr w/ 0..2..3 <- [10,12]`é a matriz `[10,1,12,3]` .

#### <a name="copy-and-update-expressions-for-named-items"></a>Copiar e atualizar expressões para itens nomeados

Existem expressões semelhantes para itens nomeados em tipos definidos pelo usuário. 

Considere, por exemplo, o tipo 

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

Observe que mais detalhes sobre os tipos callable podem ser encontrados abaixo, bem como na próxima página, [operações e funções em Q #](xref:microsoft.quantum.guide.operationsfunctions).

Se o tipo de elemento comum for uma operação ou tipo de função, todos os elementos deverão ter os mesmos tipos de entrada e saída.
O tipo de elemento da matriz dará suporte a qualquer transmissão functors que tenha suporte de todos os elementos.
Por exemplo, se `Op1` , `Op2` , e `Op3` todos forem `Qubit[] => Unit` , mas o oferecer suporte a, o oferece suporte a `Op1` `Adjoint` `Op2` `Controlled` , e `Op3` dá suporte a ambos:

- `[Op1, Op2]`é uma matriz de `(Qubit[] => Unit)` operações.
- `[Op1, Op3]`é uma matriz de `(Qubit[] => Unit is Adj)` operações.
- `[Op2, Op3]`é uma matriz de `(Qubit[] => Unit is Ctl)` operações.

No entanto, enquanto `(Qubit[] => Unit is Adj)` `(Qubit[] => Unit is Ctl)` as operações têm o tipo base comum de `(Qubit[] => Unit)` , observe *of* que as matrizes desses operadores não compartilham um tipo base comum. Por exemplo, `[[Op1], [Op2]]` no momento, o geraria um erro porque ele está tentando criar uma matriz dos tipos de matriz incompatíveis `(Qubit[] => Unit is Adj)[]` e `(Qubit[] => Unit is Ctl)[]` .


## <a name="conditional-expressions"></a>Expressões condicionais

Dadas duas outras expressões do mesmo tipo e uma expressão booliana, a expressão condicional pode ser formada usando o ponto de interrogação `?` e a barra vertical `|` .
Por exemplo, `a==b ? c | d` .
Neste exemplo, o valor da expressão condicional será `c` se `a==b` for true e `d` se for false.

### <a name="conditional-expressions-with-callables"></a>Expressões condicionais com callablefiles

As duas expressões podem ser avaliadas como operações que têm as mesmas entradas e saídas, mas dão suporte a diferentes transmissão functors.
Nesse caso, o tipo da expressão condicional é uma operação com as entradas e saídas que dão suporte a qualquer transmissão functors com suporte em ambas as expressões.
Por exemplo, se `Op1` , `Op2` , e `Op3` todos forem `Qubit[]=>Unit` , mas o oferecer suporte a, o oferece suporte a `Op1` `Adjoint` `Op2` `Controlled` , e `Op3` dá suporte a ambos:

- `flag ? Op1 | Op2`é uma `(Qubit[] => Unit)` operação.
- `flag ? Op1 | Op3`é uma `(Qubit[] => Unit is Adj)` operação.
- `flag ? Op2 | Op3`é uma `(Qubit[] => Unit is Ctl)` operação.

Se qualquer uma das duas expressões de resultado possíveis incluir uma função ou uma chamada de operação, essa chamada só ocorrerá se o resultado for aquele que será o valor da chamada.
Por exemplo, no caso `a==b ? C(qs) | D(qs)` , se `a==b` for true, a `C` operação será invocada e, se for false, somente `D` será invocada.
Isso é semelhante ao curto circuito em outras linguagens.

## <a name="callable-expressions"></a>Expressões que podem ser chamadas

Um literal que pôde ser chamado é o nome de uma operação ou função definida no escopo de compilação.
Por exemplo, `X` é um literal de operação que se refere à operação de biblioteca padrão `X` e `Message` é um literal de função que se refere à função de biblioteca padrão `Message` .

Se uma operação oferecer suporte a `Adjoint` functor, `Adjoint op` será uma expressão de operação.
Da mesma forma, se a operação oferecer suporte a `Controlled` functor, `Controlled op` será uma expressão de operação.
Os tipos dessas expressões são especificados na [chamada de especializações de operação](xref:microsoft.quantum.guide.operationsfunctions#calling-operation-specializations).

Transmissão functors ( `Adjoint` e `Controlled` ) associam-se mais de todos os outros operadores, exceto para o operador de desencapsulamento `!` e indexação de matriz com [] ".
Portanto, as seguintes são todas legais, supondo que as operações suportam o transmissão functors usado:

```qsharp
Adjoint Op(qs)
Controlled Op(controls, targets)
Controlled Adjoint Op(controls, targets)
Adjoint WrappedOp!(qs)
```

### <a name="type-parameterized-callable-expressions"></a>Expressões callable parametrizadas de tipo

Um literal resgatável pode ser usado como um valor, digamos para atribuir a uma variável ou passar para outro callable.
Nesse caso, se o callable tiver [parâmetros de tipo](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables), eles deverão ser fornecidos como parte do valor que pode ser chamado.
Um valor callable não pode ter nenhum parâmetro de tipo não especificado.

Por exemplo, se `Fun` é uma função com assinatura `'T1->Unit` :

```qsharp
let f = Fun<Int>;            // f is (Int->Unit).
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun<Double>);   // A (Double->Unit) is passed to SomOtherFun.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a>Expressões de invocação que podem ser chamadas

Dada uma expressão resgatável (operação ou função) e uma expressão de tupla do tipo de entrada da assinatura do callable, uma expressão de invocação pode ser formada acrescentando-se a expressão de tupla à expressão que pode ser chamada.
O tipo da expressão de invocação é o tipo de saída da assinatura do callable.

Por exemplo, se `Op` for uma operação com assinatura `((Int, Qubit) => Double)` , `Op(3, qubit1)` é uma expressão do tipo `Double` .
Da mesma forma, se `Sin` é uma função com assinatura `(Double -> Double)` , `Sin(0.1)` é uma expressão do tipo `Double` .
Por fim, se `Builder` for uma função com assinatura `(Int -> (Int -> Int))` , `Builder(3)` será uma função de em para int.

Invocar o resultado de uma expressão com valor callable requer um par extra de parênteses em volta da expressão callable.
Portanto, para invocar o resultado da chamada `Builder` do parágrafo anterior, a sintaxe correta é:

```qsharp
(Builder(3))(2)
```

Ao invocar um callable [com parâmetros de tipo](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) , os parâmetros do tipo real podem ser especificados entre colchetes angulares `<` e `>` após a expressão que pode ser chamada.
Isso geralmente é desnecessário, pois o compilador Q # inferirá os tipos reais.
No entanto, ele *será* necessário para o [aplicativo parcial](xref:microsoft.quantum.guide.operationsfunctions#partial-application) se um argumento de tipo parametrizado for deixado não especificado.
Às vezes, também é útil ao passar operações com functor diferentes para um callable.

Por exemplo, se `Func` tem assinatura `('T1, 'T2, 'T1) -> 'T2` `Op1` e tem assinatura e `Op2` `(Qubit[] => Unit is Adj)` `Op3` tem assinatura `(Qubit[] => Unit)` , para invocar `Func` com `Op1` como o primeiro argumento, `Op2` como o segundo, e `Op3` como o terceiro:

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

A especificação de tipo é necessária porque `Op3` e `Op1` tem tipos diferentes, portanto, o compilador tratará isso como ambíguo sem a especificação.


## <a name="operator-precedence"></a>Precedência de operador

Todos os operadores binários são associativos à direita, exceto para `^` .

Colchetes e `[` `]` , para a divisão e a indexação de matriz, associe antes de qualquer operador.

A transmissão functors `Adjoint` e a `Controlled` Associação após a indexação da matriz, mas antes de todos os outros operadores.

Parênteses para operação e invocação de função também são associados antes de qualquer operador, mas após a indexação de matriz e transmissão functors.

Operadores em ordem de precedência, do mais alto ao mais baixo:

Operador | Arity | Descrição | Tipos de operando
---------|----------|---------|---------------
 à direita`!` | Unário | Desencapsular | Qualquer tipo definido pelo usuário
 `-`, `~~~`, `not` | Unário | Numérico negativo, complemento de bit-nte, negação lógica | `Int`, `BigInt` ou `Double` para `-` , `Int` ou `BigInt` para `~~~` , `Bool` para`not`
 `^` | Binário | Potência de inteiro | `Int`ou `BigInt` para a base, `Int` para o expoente
 `/`, `*`, `%` | Binário | Divisão, multiplicação, módulo de inteiro | `Int`, `BigInt` ou `Double` para `/` e `*` , `Int` ou `BigInt` para`%`
 `+`, `-` | Binário | Adição ou concatenação de cadeia de caracteres e matriz, subtração | `Int`, `BigInt` ou `Double` , além disso, `String` ou qualquer tipo de matriz para`+`
 `<<<`, `>>>` | Binário | Deslocamento à esquerda, deslocamento à direita | `Int` ou `BigInt`
 `<`, `<=`, `>`, `>=` | Binário | Comparações de menor que, menor que ou igual a, maior que, maior que ou igual a | `Int``BigInt`ou`Double`
 `==`, `!=` | Binário | comparações iguais, não iguais | qualquer tipo primitivo
 `&&&` | Binário | AND bit a bit | `Int` ou `BigInt`
 `^^^` | Binário | XOR bit a bit | `Int` ou `BigInt`
 <code>\|\|\|</code> | Binário | OR bit a bit | `Int` ou `BigInt`
 `and` | Binário | AND lógico | `Bool`
 `or` | Binário | OR lógico | `Bool`
 `..` | Binary/ternário | Operador de intervalo | `Int`
 `?` `|` | Ternário | Condicional | `Bool`para o lado esquerdo
`w/` `<-` | Ternário | Copiar e atualizar | consulte [expressões de copiar e atualizar](#copy-and-update-expressions)

## <a name="next-steps"></a>Próximas etapas

Agora que você pode trabalhar com expressões em Q #, você pode ir para [operações e funções em q #](xref:microsoft.quantum.guide.operationsfunctions) para saber como definir e chamar operações e funções.
