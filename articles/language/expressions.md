---
title: 'Expressões Q #'
description: 'Entenda como especificar, referenciar e combinar constantes, variáveis, operadores, operações e funções como expressões em Q #.'
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.language.expressions
ms.openlocfilehash: 095be52af27f827f3e52d39a70702f50d6d59ee8
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/01/2020
ms.locfileid: "82683922"
---
# <a name="expressions"></a>Expressões

## <a name="grouping"></a>Agrupamento

Dada qualquer expressão, a mesma expressão entre parênteses é uma expressão do mesmo tipo.
Por exemplo, `(7)` é uma `Int` expressão, `([1,2,3])` é uma expressão do tipo matriz de `Int`s e `((1,2))` é uma expressão com tipo `(Int, Int)`.

A equivalência entre valores simples e tuplas de elemento único descritos no [modelo de tipo](xref:microsoft.quantum.language.type-model#tuple-types) remove a ambiguidade entre `(6)` como um grupo e `(6)` como uma tupla de elemento único.

## <a name="symbols"></a>Símbolos

O nome de um símbolo associado ou atribuído a um valor do tipo `'T` é uma expressão do tipo `'T`.
Por exemplo, se o símbolo `count` estiver associado ao valor `5`inteiro, `count` será uma expressão de inteiro.

## <a name="numeric-expressions"></a>Expressões numéricas

Expressões numéricas são expressões do `Int`tipo `BigInt`, ou `Double`.
Ou seja, eles são números inteiros ou de ponto flutuante.

`Int`os literais em Q # são idênticos aos literais inteiros em C#, exceto pelo fato de que nenhum "l" ou "L" à direita é necessário (ou permitido).
Os inteiros hexadecimais e binários têm suporte com um prefixo "0x" e "0B", respectivamente.

`BigInt`os literais em Q # são idênticos às cadeias de caracteres inteiros grandes no .NET, com um "l" ou "L" à direita.
Há suporte para inteiros grandes hexadecimais com um prefixo "0x".
Portanto, veja a seguir todos os usos válidos `BigInt` de literais:

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

`Double`os literais em Q # são idênticos aos literais duplos em C#, exceto pelo fato de que nenhum "d" ou "D" à direita é necessário (ou permitido).

Dada uma expressão de matriz de qualquer tipo de elemento `Int` , uma expressão pode ser formada usando a `Length` função interna, com a expressão de matriz entre parênteses `(` e `)`.
Por exemplo, se `a` estiver associado a uma matriz, `Length(a)` será uma expressão de inteiro.
Se `b` é uma matriz de matrizes de inteiros, `Int[][]`, `Length(b)` é o número de submatrizes em `b`e `Length(b[1])` é o número de inteiros na segunda submatriz no. `b`

Dadas duas expressões numéricas do mesmo tipo `+`, os operadores `-` `*`binários,, e `/` podem ser usados para formar uma nova expressão numérica.
O tipo da nova expressão será o mesmo que os tipos das expressões constituintes.

Dadas duas expressões de inteiro, o operador `^` binário (potência) pode ser usado para formar uma nova expressão de inteiro.
Da mesma `^` forma, pode ser usado com duas expressões duplas para formar uma nova expressão Double.
Por fim `^` , pode ser usado com um inteiro grande à esquerda e um inteiro à direita para formar uma nova expressão de inteiro grande.
Nesse caso, o segundo parâmetro deve caber em 32 bits; caso contrário, um erro de tempo de execução será gerado.

Dadas duas expressões de inteiro ou grandes inteiros, um novo inteiro ou uma expressão de inteiro grande pode ser `%` formada usando os `&&&` operadores (módulo), `|||` (bit e), ( `^^^` OR-bit or) ou (XOR).

Dado um inteiro ou uma expressão de inteiro grande à esquerda e uma expressão de inteiro à direita, os `<<<` operadores (deslocamento aritmético à esquerda) `>>>` ou (deslocamento aritmético à direita) podem ser usados para criar uma nova expressão com o mesmo tipo que a expressão esquerda.

O segundo parâmetro (o valor de deslocamento) para a operação de deslocamento deve ser maior ou igual a zero; o comportamento para valores de deslocamento negativos é indefinido.
O valor de deslocamento para uma das operações de deslocamento também deve se ajustar a 32 bits; caso contrário, um erro de tempo de execução será gerado.
Se o número a ser deslocado for um inteiro, o valor de deslocamento será interpretado `mod 64`; ou seja, uma mudança de 1 e uma mudança de 65 têm o mesmo efeito.

Para os valores inteiros e inteiros grandes, as turnos são aritméticas.
A mudança de um valor negativo para a esquerda ou direita resultará em um número negativo.
Ou seja, mudar uma etapa para a esquerda ou para a direita é exatamente o mesmo que multiplicar ou dividir por 2, respectivamente.

Divisão de inteiros e módulo de inteiro seguem o mesmo comportamento para números negativos em C#.
Ou seja, `a % b` sempre terá o mesmo sinal `a`de e `b * (a / b) + a % b` sempre será igual. `a`
Por exemplo: 

 `A` | `B` | `A / B` | `A % B`
---------|----------|---------|---------
 5 | 2 | 2 | 1
 5 | -2 | -2 | 1
 -5 | 2 | -2 | -1
 -5 | -2 | 2 | -1

Divisão de inteiro grande e módulo funciona da mesma maneira.

Dada qualquer expressão numérica, uma nova expressão pode ser formada usando `-` o operador unário.
A nova expressão será o mesmo tipo da expressão constituinte.

Devido a qualquer inteiro ou expressão de inteiro grande, uma nova expressão do mesmo tipo pode ser formada `~~~` usando o operador unário (complemento de bits).

## <a name="boolean-expressions"></a>Expressões boolianas

Os dois `Bool` valores literais `true` são `false`e.

Dadas as duas expressões do mesmo tipo primitivo, os `==` operadores binários e `!=` podem ser usados para construir uma `Bool` expressão.
A expressão será true se as duas expressões forem iguais e false se não.

Os valores de tipos definidos pelo usuário não podem ser comparados, apenas seus valores não encapsulados podem ser comparados. Por exemplo, usando o operador `!` "sem encapsulamento" (explicado na [página modelo do tipo Q #](xref:microsoft.quantum.language.type-model#user-defined-types)),

```qsharp
newtype WrappedInt = Int;     // Yes, this is a contrived example
let x = WrappedInt(1);
let y = WrappedInt(2);
let z = x! == y!;             // This will compile and yield z = false.
let t = x == y;               // This will cause a compiler error.
```

A comparação de `Qubit` igualdade para valores é igualdade de identidade; ou seja, se as duas expressões identificam o mesmo qubit.
O estado dos dois qubits não são comparados, acessados, medidos ou modificados por essa comparação.

A comparação de `Double` igualdade para valores pode ser enganosa devido a efeitos de arredondamento.
Por exemplo, `49.0 * (1.0/49.0) != 1.0`.

Dadas quaisquer duas expressões numéricas, os operadores `>` `<` `>=`binários,, `<=` e podem ser usados para construir uma nova expressão booliana que seja verdadeira se a primeira expressão for maior que, menor que, maior ou igual ou menor ou igual à segunda expressão.

Dadas quaisquer duas expressões booleanas, os `and` operadores `or` binários e podem ser usados para construir uma nova expressão booliana que seja verdadeira se ambos (resp. ou ambos) as duas expressões forem true.

Dada qualquer expressão booliana, `not` o operador unário pode ser usado para construir uma nova expressão booliana que seja verdadeira se a expressão constituinte for falsa.

## <a name="string-expressions"></a>Expressões de cadeia de caracteres

Q # permite que as cadeias de caracteres `fail` sejam usadas na `Log` instrução e na função padrão.

Cadeias de caracteres em Q # são literais ou cadeias de caracteres interpoladas.
Literais de cadeia de caracteres são semelhantes a literais de cadeia de caracteres simples na maioria dos idiomas: uma sequência de `"`caracteres Unicode entre aspas duplas,.
Dentro de uma cadeia de caracteres, `\` o caractere de barra invertida pode ser usado para escapar de um caractere de aspas duplas e para inserir `\n`uma linha nova como, `\r`um retorno de carro como `\t`e uma tabulação como.
Por exemplo:

```qsharp
"\"Hello world!\", she said.\n"
```

A sintaxe de Q # para interpolações de cadeia de caracteres é um subconjunto da sintaxe C# 7,0; Q # não oferece suporte a cadeias de caracteres interpoladas (várias linhas) textuais.
Consulte [*cadeias de caracteres interpoladas*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings) para a sintaxe C#.

As expressões dentro de uma cadeia de caracteres interpolada seguem a sintaxe Q #, e não a sintaxe C#.
Qualquer expressão Q # válida pode aparecer em uma cadeia de caracteres interpolada.

## <a name="qubit-expressions"></a>Expressões qubit

As únicas `Qubit` expressões são símbolos que são associados a `Qubit` valores ou elementos de matriz `Qubit` de matrizes.
Não há `Qubit` literais.

## <a name="pauli-expressions"></a>Expressões Pauli

Os quatro `Pauli` valores, `PauliI`, `PauliX` `PauliY`, e `PauliZ`, são expressões válidas `Pauli` .

Além disso, as únicas `Pauli` expressões são símbolos associados a `Pauli` valores ou elementos de matriz de `Pauli` matrizes.

## <a name="result-expressions"></a>Expressões de resultado

Os dois `Result` valores, `One` e `Zero`, são expressões `Result` válidas.

Além disso, as únicas `Result` expressões são símbolos associados a `Result` valores ou elementos de matriz de `Result` matrizes.
Em particular, observe que `One` não é o mesmo que o inteiro `1`, e não há nenhuma conversão direta entre eles.
O mesmo é verdadeiro para `Zero` e `0`.

## <a name="range-expressions"></a>Expressões de intervalo

Dadas as três `Int` expressões `start`, `step`e `stop`, `start .. step .. stop` é uma expressão de intervalo cujo primeiro elemento é `start`, o segundo elemento `start+step`é, o terceiro `start+step+step`elemento é, etc. `stop` , até que seja passado.
Um intervalo pode estar vazio se, por exemplo, `step` for positivo e `stop < start`.
O último elemento do intervalo `stop` será se a diferença entre `start` e `stop` for um múltiplo integral de; `step` ou seja, o intervalo é inclusivo em ambas as extremidades.

Dadas as duas `Int` expressões `start` e `stop`, `start .. stop` é uma expressão de intervalo igual a `start .. 1 .. stop`.
Observe que o implícito `step` é + 1, mesmo se `stop` for menor que `start`; Nesse caso, o intervalo está vazio.

Alguns intervalos de exemplo são:

- `1..3`é o intervalo 1, 2, 3.
- `2..2..5`é o intervalo de 2, 4.
- `2..2..6`é o intervalo de 2, 4, 6.
- `6..-2..2`é o intervalo de 6, 4, 2.
- `2..1`é o intervalo vazio.
- `2..6..7`é o intervalo 2.
- `2..2..1`é o intervalo vazio.
- `1..-1..2`é o intervalo vazio.

## <a name="callable-expressions"></a>Expressões que podem ser chamadas

Um literal que pôde ser chamado é o nome de uma operação ou função definida no escopo de compilação.
Por exemplo, `X` é um literal de operação que se refere à operação `X` de biblioteca padrão `Message` e é um literal de função que se refere à `Message` função de biblioteca padrão.

Se uma operação oferecer suporte `Adjoint` a functor, `Adjoint op` será uma expressão de operação.
Da mesma forma, se a operação `Controlled` oferecer suporte a `Controlled op` functor, será uma expressão de operação.
Os tipos dessas expressões são especificados em [transmissão functors](xref:microsoft.quantum.language.type-model#functors).

Transmissão functors (`Adjoint` e `Controlled`) associam-se mais de todos os outros operadores, exceto para o `!` operador de desencapsulamento `[]`e a indexação de matriz com.
Portanto, as seguintes são todas legais, supondo que as operações suportam o transmissão functors usado:

```qsharp
Adjoint Op(qs)
Controlled Op(controls, targets)
Controlled Adjoint Op(controls, targets)
Adjoint WrappedOp!(qs)
```

Um literal resgatável pode ser usado como um valor, digamos para atribuir a uma variável ou passar para outro callable.
Nesse caso, se o callable tiver parâmetros de tipo, eles deverão ser fornecidos como parte do valor que pode ser chamado.
Um valor callable não pode ter nenhum parâmetro de tipo não especificado.

Por exemplo, se `Fun` é uma função com assinatura `'T1->Unit`:

```qsharp
let f = Fun<Int>;            // f is Int->Unit.
SomeOtherFun(Fun<Double>);   // A Double->Unit is passed to SomeOtherFun.
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a>Expressões de invocação que podem ser chamadas

Dada uma expressão resgatável (operação ou função) e uma expressão de tupla do tipo de entrada da assinatura do callable, uma expressão de invocação pode ser formada acrescentando-se a expressão de tupla à expressão que pode ser chamada.
O tipo da expressão de invocação é o tipo de saída da assinatura do callable.

Por exemplo, se `Op` for uma operação com assinatura `((Int, Qubit) => Double)`, `Op(3, qubit1)` é uma expressão do tipo `Double`.
Da mesma forma `Sin` , se é uma função `(Double -> Double)`com `Sin(0.1)` assinatura, é uma expressão `Double`do tipo.
Por fim, `Builder` se for uma função com `(Int -> (Int -> Int))`assinatura, `Builder(3)` será uma função de em para int.

Invocar o resultado de uma expressão com valor callable requer um par extra de parênteses em volta da expressão callable.
Portanto, para invocar o resultado da `Builder` chamada do parágrafo anterior, a sintaxe correta é:

```qsharp
(Builder(3))(2)
```

Ao invocar um callable com parâmetros de tipo, os parâmetros do tipo real podem ser especificados entre colchetes `<` angulares e `>` após a expressão que pode ser chamada.
Isso geralmente é desnecessário, pois o compilador Q # inferirá os tipos reais.
Ele é necessário para o aplicativo parcial (veja abaixo) se um argumento com parâmetros de tipo for deixado não especificado.
Às vezes, também é útil ao passar operações com functor diferentes para um callable.

Por exemplo, se `Func` tem assinatura `('T1, 'T2, 'T1) -> 'T2` `Op1` `Op2` e tem `(Qubit[] => Unit is Adj)`assinatura e `Op3` tem assinatura `(Qubit[] => Unit)`, para invocar `Func` com `Op1` como o primeiro argumento, `Op2` como o segundo, e `Op3` como o terceiro:

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

A especificação de tipo é necessária `Op3` porque `Op1` e tem tipos diferentes, portanto, o compilador tratará isso como ambíguo sem a especificação.

### <a name="partial-application"></a>Aplicativo parcial

Dada uma expressão resgatável, um novo callable pode ser criado fornecendo um subconjunto dos argumentos para o callable.
Isso é chamado de _aplicativo parcial_.

Em Q #, um resgatável aplicado parcialmente é expresso escrevendo uma expressão de invocação normal, mas usando um sublinhado, `_`, para os argumentos não especificados.
O callable que resultau tem o mesmo tipo de resultado que o callable de base, e as mesmas especializações para operações.
O tipo de entrada do aplicativo parcial é simplesmente o tipo original com os argumentos especificados removidos.

Se uma variável mutável for passada como um argumento especificado ao criar um aplicativo parcial, o valor atual da variável será usado.
Alterar o valor da variável subsequentemente não afetará o aplicativo parcial.

Por exemplo, se `Op` tiver o `((Int, ((Qubit, Qubit), Double)) => Unit is Adj)`tipo:

- `Op(5,(_,_))`tem o `(((Qubit,Qubit), Double) => Unit is Adj)`tipo e, portanto `Op(5,_)`, tem.
- `Op(_,(_,1.0))` tem o tipo `((Int, (Qubit,Qubit)) => Unit is Adj)`.
- `Op(_,((q1,q2),_))` tem o tipo `((Int,Double) => Unit is Adj)`.
   Observe que aplicamos a equivalência de tupla singleton aqui.

Se o chamado parcialmente aplicado tiver parâmetros de tipo que não podem ser inferidos pelo compilador, eles deverão ser fornecidos no site de invocação.
O aplicativo parcial não pode ter nenhum parâmetro de tipo não especificado.

Por exemplo, se `Op` tiver o `(('T1, Qubit, 'T1) => Unit : Adjoint)`tipo:

```qsharp
let f1 = Op<Int>(_, qb, _); // f1 has type ((Int,Int) => Unit is Adj)
let f2 = Op(5, qb, _);      // f2 has type (Int => Unit is Adj)
let f3 = Op(_,qb, _);       // f3 generates a compilation error
```

### <a name="recursion"></a>Recursão

Os chamadores do Q # podem ser recursivos direta ou indiretamente.
Ou seja, uma operação ou função pode chamar a si mesma ou chamar outro callable que chama direta ou indiretamente a operação que pode ser chamada.

No entanto, há dois comentários importantes sobre o uso da recursão:

- O uso da recursão nas operações provavelmente interfere em determinadas otimizações.
  Isso pode ter um impacto significativo no tempo de execução do algoritmo.
- Ao executar em um dispositivo Quantum real, o espaço de pilha pode ser limitado e, portanto, a recursão profunda pode levar a um erro de tempo de execução.
  Em particular, o compilador e o tempo de execução do Q # não identificam e otimizam a recursão da cauda.

## <a name="tuple-expressions"></a>Expressões de tupla

Um literal de tupla é uma sequência de expressões de elemento do tipo apropriado, separados por vírgulas, colocadas `(` em `)`e.
Por exemplo, `(1, One)` é uma `(Int, Result)` expressão.

Além de literais, as únicas expressões de tupla são símbolos associados a valores de tupla, elementos de matriz de matrizes de tupla e invocações que retornam tuplas.

## <a name="user-defined-type-expressions"></a>Expressões de tipo definidas pelo usuário

Um literal de um tipo definido pelo usuário consiste no nome do tipo seguido por um literal de tupla do tipo de tupla base do tipo.
Por exemplo, se `IntPair` for um tipo definido pelo usuário com base `(Int, Int)`em, `IntPair(2,3)` seria um literal válido desse tipo.

Além de literais, as únicas expressões de um tipo definido pelo usuário são símbolos que são associados a valores desse tipo, elementos da matriz de matrizes desse tipo e invocações que retornam esse tipo.

## <a name="unwrap-expressions"></a>Desencapsular expressões

Em Q #, o operador de desencapsulamento é um ponto de exclamação `!`à direita.
Por exemplo, se `IntPair` é um tipo definido pelo usuário com o tipo `(Int, Int)`subjacente e `s` era uma variável com valor `IntPair(2,3)`, `s!` seria `(2,3)`.

Para tipos definidos pelo usuário definidos em termos de outros tipos definidos pelo usuário. o operador de desencapsulamento pode ser repetido; por exemplo, `s!!` indica o valor duplo não encapsulado de `s`.
Portanto, se `WrappedPair` for um tipo definido pelo usuário com o tipo `IntPair`subjacente, `t` e for uma variável com `WrappedPair(IntPair(1,2))`valor, `t!!` será `(1,2)`.

O `!` operador tem precedência maior do que todos os outros `[]` operadores diferentes de para indexação e divisão de matriz.
`!`e `[]` associar à posição; ou seja, `a[i]![3]` deve ser lido como `((a[i])!)[3]`: Pegue o `i`elemento ' th ' `a`, desenvolva-o e, em seguida, obtenha o terceiro elemento do valor não encapsulado (que deve ser uma matriz).

A precedência do `!` operador tem um impacto que pode não ser óbvio.
Se uma função ou operação retorna um valor que, em seguida, é desencapsulada, a função ou a chamada de operação deve ser colocada entre parênteses para que a tupla de argumento seja associada à chamada em vez de ser desencapsulada.
Por exemplo: 

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a>Expressões de matriz

Um literal de matriz é uma sequência de uma ou mais expressões de elemento, separadas por vírgulas, `[` colocadas `]`em e.
Todos os elementos devem ser compatíveis com o mesmo tipo.

Se o tipo de elemento comum for uma operação ou tipo de função, todos os elementos deverão ter os mesmos tipos de entrada e saída.
O tipo de elemento da matriz dará suporte a qualquer transmissão functors que tenha suporte de todos os elementos.
Por exemplo, se `Op1`, `Op2`, e `Op3` todos forem `Qubit[] => Unit`, mas `Op1` o `Adjoint`oferecer `Op2` suporte `Controlled`a, `Op3` o oferece suporte a, e dá suporte a ambos:

- `[Op1, Op2]`é uma matriz de `(Qubit[] => Unit)` operações.
- `[Op1, Op3]`é uma matriz de `(Qubit[] => Unit is Adj)` operações.
- `[Op2, Op3]`é uma matriz de `(Qubit[] => Unit is Ctl)` operações.

Literais de matriz vazios `[]`,, não são permitidos.
Em vez `new ★[0]`disso, `★` o uso de, onde é o espaço reservado para um tipo adequado, permite criar a matriz desejada de comprimento zero.

Dadas duas matrizes do mesmo tipo, o operador `+` binário pode ser usado para formar uma nova matriz que é a concatenação das duas matrizes.
Por exemplo, `[1,2,3] + [4,5,6]` é `[1,2,3,4,5,6]`.

### <a name="array-creation"></a>Criação de matriz

Dado um tipo e uma `Int` expressão, o `new` operador pode ser usado para alocar uma nova matriz do tamanho determinado.
Por exemplo, `new Int[i+1]` alocaria uma nova `Int` matriz com `i+1` elementos.

Os elementos de uma nova matriz são inicializados para um valor padrão dependente de tipo.
Na maioria dos casos, essa é uma variação de zero.

Para qubits e callableies, que são referências a entidades, não há nenhum valor padrão razoável.
Portanto, para esses tipos, o padrão é uma referência inválida que não pode ser usada sem causar um erro de tempo de execução.
Isso é semelhante a uma referência nula em linguagens como C# ou Java.
As matrizes que contêm qubits ou callables devem ser inicializadas corretamente com valores não padrão antes que seus elementos possam ser usados com segurança. Rotinas de inicialização adequadas podem ser <xref:microsoft.quantum.arrays>encontradas em.

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


### <a name="jagged-arrays"></a>Matrizes denteadas

Uma matriz denteada, às vezes chamada de "matriz de matrizes", é uma matriz cujos elementos são matrizes. Os elementos de uma matriz denteada podem ser de tamanhos diferentes. O exemplo a seguir mostra como declarar e inicializar uma matriz denteada que representa uma tabela de multiplicação.

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


### <a name="array-slices"></a>Fatias de matriz

Dada uma expressão de matriz e `Range` uma expressão, uma nova expressão pode ser formada `[` usando `]` o operador matriz de fatia e.
A nova expressão será do mesmo tipo que a matriz e conterá os itens de matriz indexados pelos elementos de `Range`, na ordem definida pelo. `Range`
Por exemplo, se `a` estiver associado a uma matriz de `Double`s, `a[3..-1..0]` será uma `Double[]` expressão que contém os quatro primeiros elementos de `a` , mas na ordem inversa, conforme aparecem. `a`

Se o `Range` estiver vazio, a fatia da matriz resultante será de comprimento zero.

Se a expressão de matriz não for um identificador simples, ela deverá ser colocada entre parênteses, para fatiar.
Por exemplo, se `a` e `b` forem ambas matrizes `Int`de s, uma fatia da concatenação seria expressa como:

```qsharp
(a+b)[1..2..7]
```

Todas as matrizes em Q # são baseadas em zero.
Ou seja, o primeiro elemento de uma matriz `a` é sempre `a[0]`.

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

## <a name="array-element-expressions"></a>Expressões de elementos de matriz

Dada uma expressão de matriz e `Int` uma expressão, uma nova expressão pode ser formada `[` usando `]` o operador de elemento de matriz e.
A nova expressão será do mesmo tipo que o tipo de elemento da matriz.
Por exemplo, se `a` estiver associado a uma matriz de `Double`s, `a[4]` será uma `Double` expressão.

Se a expressão de matriz não for um identificador simples, ela deverá ser colocada entre parênteses para selecionar um elemento.
Por exemplo, se `a` e `b` forem ambas matrizes `Int`de s, um elemento da concatenação seria expresso como:

```qsharp
(a+b)[13]
```

Todas as matrizes em Q # são baseadas em zero.
Ou seja, o primeiro elemento de uma matriz `a` é sempre `a[0]`.


## <a name="copy-and-update-expressions"></a>Expressões Copy-and-Update

Novas matrizes podem ser criadas a partir de existentes por meio de expressões de copiar e atualizar.
Uma expressão `expression1 w/ expression2 <- expression3`de copiar e atualizar é uma expressão do formulário, onde `expression1` deve ser do tipo `T[]` para algum tipo. `T` O segundo `expression2` define os índices dos elementos a serem modificados em comparação com a matriz em `expression1` e deve ser do tipo `Int` ou do tipo. `Range` Se `expression2` for do tipo `Int`, `expression3` deve ser do tipo `T`. Se `expression2` for do tipo `Range`, `expression3` deve ser do tipo `T[]`.

Uma expressão `arr w/ idx <- value` de copiar e atualizar constrói uma nova matriz com todos os elementos definidos para o elemento correspondente no `arr`, exceto para os elementos em `idx`, que são definidos como os (s) em. `value` Por exemplo, se `arr` contiver uma `[0,1,2,3]`matriz, 
- `arr w/ 0 <- 10`é a matriz `[10,1,2,3]`.
- `arr w/ 2 <- 10`é a matriz `[0,1,10,3]`.
- `arr w/ 0..2..3 <- [10,12]`é a matriz `[10,1,12,3]`.

Existem expressões semelhantes para itens nomeados em tipos definidos pelo usuário. Considere, por exemplo, o tipo 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
Se `c` contiver o valor do `Complex(1.,-1.)`tipo, `c w/ Re <- 0.` será uma expressão do tipo `Complex` que é avaliada `Complex(0.,-1.)`como.

## <a name="conditional-expressions"></a>Expressões condicionais

Dadas duas outras expressões do mesmo tipo e uma expressão booliana, a expressão condicional pode ser formada usando o ponto `?` de interrogação e `|`a barra vertical.
Por exemplo, `a==b ? c | d`.
Neste exemplo, o valor da expressão condicional será `c` se `a==b` for true e `d` se for false.

As duas expressões podem ser avaliadas como operações que têm as mesmas entradas e saídas, mas dão suporte a diferentes transmissão functors.
Nesse caso, o tipo da expressão condicional é uma operação com as entradas e saídas que dão suporte a qualquer transmissão functors com suporte em ambas as expressões.
Por exemplo, se `Op1`, `Op2`, e `Op3` todos forem `Qubit[]=>Unit`, mas `Op1` o `Adjoint`oferecer `Op2` suporte `Controlled`a, `Op3` o oferece suporte a, e dá suporte a ambos:

- `flag ? Op1 | Op2`é uma `(Qubit[] => Unit)` operação.
- `flag ? Op1 | Op3`é uma `(Qubit[] => Unit is Adj)` operação.
- `flag ? Op2 | Op3`é uma `(Qubit[] => Unit is Ctl)` operação.

Se qualquer uma das duas expressões de resultado possíveis incluir uma função ou uma chamada de operação, essa chamada só ocorrerá se o resultado for aquele que será o valor da chamada.
Por exemplo `a==b ? C(qs) | D(qs)`, no caso, se `a==b` for true, a `C` operação será invocada e, se for false, somente `D` será invocada.
Isso é semelhante ao curto circuito em outras linguagens.


## <a name="operator-precedence"></a>Precedência de operador

Todos os operadores binários são associativos à direita, `^`exceto para.

`[` Colchetes e `]`, para a divisão e a indexação de matriz, associe antes de qualquer operador.

A transmissão functors `Adjoint` e `Controlled` a associação após a indexação da matriz, mas antes de todos os outros operadores.

Parênteses para operação e invocação de função também são associados antes de qualquer operador, mas após a indexação de matriz e transmissão functors.

Operadores em ordem de precedência, do mais alto ao mais baixo:

Operador | Arity | Descrição | Tipos de operando
---------|----------|---------|---------------
 à direita`!` | Unário | Desencapsular | Qualquer tipo definido pelo usuário
 `-`, `~~~`, `not` | Unário | Numérico negativo, complemento de bit-nte, negação lógica | `Int`, `BigInt` ou `Double` para `-`, `Int` ou `BigInt` para `~~~`, `Bool` para`not`
 `^` | Binário | Potência de inteiro | `Int`ou `BigInt` para a base, `Int` para o expoente
 `/`, `*`, `%` | Binário | Divisão, multiplicação, módulo de inteiro | `Int`, `BigInt` ou `Double` para `/` e `*`, `Int` ou `BigInt` para`%`
 `+`, `-` | Binário | Adição ou concatenação de cadeia de caracteres e matriz, subtração | `Int`, `BigInt` ou `Double`, além `String` disso, ou qualquer tipo de matriz para`+`
 `<<<`, `>>>` | Binário | Deslocamento à esquerda, deslocamento à direita | `Int` ou `BigInt`
 `<`, `<=`, `>`, `>=` | Binário | Comparações de menor que, menor que ou igual a, maior que, maior que ou igual a | `Int``BigInt` ou`Double`
 `==`, `!=` | Binário | comparações iguais, não iguais | qualquer tipo primitivo
 `&&&` | Binário | AND bit a bit | `Int` ou `BigInt`
 `^^^` | Binário | XOR bit a bit | `Int` ou `BigInt`
 <code>\|\|\|</code> | Binário | OR bit a bit | `Int` ou `BigInt`
 `and` | Binário | AND lógico | `Bool`
 `or` | Binário | OR lógico | `Bool`
 `..` | Binary/ternário | Operador de intervalo | `Int`
 `?` `|` | Ternário | Condicional | `Bool`para o lado esquerdo
`w/` `<-` | Ternário | Copiar e atualizar | consulte [expressões de copiar e atualizar](#copy-and-update-expressions)
