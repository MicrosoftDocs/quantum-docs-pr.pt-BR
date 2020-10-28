---
title: Operações intrínsecas e funções no QDK
description: Saiba mais sobre as operações intrínsecas e funções no QDK, incluindo funções clássicas e operações de rotação e medição.
author: QuantumWriter
ms.author: martinro
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.libraries.standard.prelude
no-loc:
- Q#
- $$v
ms.openlocfilehash: 4d15226fe46be79b7d3e6f414f33f1debd691f40
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92692123"
---
# <a name="the-prelude"></a>O prelúdio #

O Q# compilador e os computadores de destino incluídos no kit de desenvolvimento Quantum fornecem um conjunto de funções intrínsecas e operações que podem ser usadas durante a gravação de programas Quantum no Q# .

## <a name="intrinsic-operations-and-functions"></a>Operações intrínsecas e funções ##

As operações intrínsecas definidas na biblioteca padrão basicamente se enquadram em uma das várias categorias:

- Funções clássicas essenciais, coletadas no <xref:Microsoft.Quantum.Core> namespace.
- Operações que representam unidades compostas por [Clifford e $T $ Gates](xref:microsoft.quantum.concepts.qubit).
- Operações que representam rotações sobre vários operadores.
- Operações de implementação de medidas.

Como o conjunto de portão Clifford + $T $ é [Universal](xref:microsoft.quantum.concepts.multiple-qubits) para a computação Quantum, essas operações são suficientes para aproximadamente implementar qualquer algoritmo Quantum dentro de um erro pequeno negligibly.
Ao fornecer rotações também, Q# permite que o programador trabalhe dentro da única biblioteca de portão qubit unitário e CNOT. Essa biblioteca é muito mais fácil de pensar porque não exige que o programador expresse diretamente a descomposição Clifford + $T $ e porque existem métodos altamente eficientes para a compilação de unidades de qubit individuais em Clifford e $T $ Gates (consulte [aqui](xref:microsoft.quantum.more-information) para obter mais informações).

Sempre que possível, as operações definidas no prelúdio que atuam no qubits permitem a aplicação da `Controlled` variante, de modo que o computador de destino execute a decomposição apropriada.

Muitas das funções e operações definidas nesta parte do prelúdio estão no @"microsoft.quantum.intrinsic" namespace, de modo que a maioria dos Q# arquivos de origem terá uma `open Microsoft.Quantum.Intrinsic;` diretiva imediatamente após a declaração de namespace inicial.
O <xref:Microsoft.Quantum.Core> namespace é aberto automaticamente, para que funções como o <xref:Microsoft.Quantum.Core.Length> possam ser usadas sem uma `open` instrução.

### <a name="common-single-qubit-unitary-operations"></a>Operações de Single-Qubit unitários comuns ###

O prelúdio também define muitas [operações comuns de qubit único](xref:microsoft.quantum.concepts.qubit#single-qubit-operations).
Todas essas operações permitem o e o `Controlled` `Adjoint` transmissão functors.

#### <a name="pauli-operators"></a>Operadores Pauli ####

A <xref:Microsoft.Quantum.Intrinsic.X> operação implementa o operador Pauli $X $.
Às vezes, isso também é conhecido como `NOT` portão.
Ele tem assinatura `(Qubit => Unit is Adj + Ctl)` .
Ele corresponde ao único qubit unitário:

\begin{Equation} \begin{bmatrix} 0 & 1 \\ \\ % FIXME: isso atualmente usa o quadwhack hack.
1 & 0 \end{bmatrix} \end{Equation}

A <xref:Microsoft.Quantum.Intrinsic.Y> operação implementa o operador Pauli $Y $.
Ele tem assinatura `(Qubit => Unit is Adj + Ctl)` .
Ele corresponde ao único qubit unitário:

\begin{Equation} \begin{bmatrix} 0 &-i \\ \\ % FIXME: isso atualmente usa o quadwhack hack.
Eu & 0 \end{bmatrix} \end{Equation}

A <xref:Microsoft.Quantum.Intrinsic.Z> operação implementa o operador Pauli $Z $.
Ele tem assinatura `(Qubit => Unit is Adj + Ctl)` .
Ele corresponde ao único qubit unitário:

\begin{Equation} \begin{bmatrix} 1 & 0 \\ \\ % FIXME: isso atualmente usa o quadwhack hack.
0 &-1 \end{bmatrix} \end{Equation}

Abaixo, vemos essas transformações mapeadas para a [esfera Bloch](xref:microsoft.quantum.concepts.qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere) (o eixo de rotação em cada caso é vermelho realçado):

![Operações Pauli mapeadas para a esfera Bloch](~/media/prelude_pauliBloch.png)

É importante observar que aplicar o mesmo portão de Pauli duas vezes ao mesmo qubit cancela a operação (porque você executou uma rotação completa de 2π (360 °) na superfície para a esfera de Bloch, chegando ao ponto de partida). Isso nos leva à seguinte identidade:

$ $ X ^ 2 = Y ^ 2 = Z ^ 2 = \boldone $ $

Isso pode ser visualizado na esfera de Bloch:

![XX = I](~/media/prelude_blochIdentity.png)

#### <a name="other-single-qubit-cliffords"></a>Outros Single-Qubit Cliffords ####

A <xref:Microsoft.Quantum.Intrinsic.H> operação implementa o portão Hadamard.
Isso troca os eixos Pauli $X $ e $Z $ do qubit de destino, de modo que $H \ket {0} = \ket{+} \mathrel{: =} (\ket {0} + \ket {1} )/\sqrt {2} $ e $H \ket{+} = \ket {0} $.
Ele tem assinatura `(Qubit => Unit is Adj + Ctl)` e corresponde ao único qubit unitário:

\begin{Equation} \frac {1} {\sqrt {2} } \begin{bmatrix} 1 & 1 \\ \\ % FIXME: isso atualmente usa o quadwhack hack.
1 &-1 \end{bmatrix} \end{Equation}

A porta Hadamard é particularmente importante, pois pode ser usada para criar uma superposição dos Estados $ \ket {0} $ e $ \ket {1} $. Na representação do Bloch Sphere, é mais fácil imaginar isso como uma rotação de $ \ket{\psi} $ em volta do eixo x por $ \pi $ radianos ($ 180 ^ \circ $) seguido por uma rotação (no sentido horário) ao lado do eixo y em $ \ pi/2 $ radianos (US $90 ^ \circ $):

![Operação Hadamard mapeada na esfera Bloch](~/media/prelude_hadamardBloch.png)

A <xref:Microsoft.Quantum.Intrinsic.S> operação implementa o portão de fase $S $.
Esta é a raiz quadrada da matriz do Pauli $Z $ Operation.
Ou seja, $S ^ 2 = Z $.
Ele tem assinatura `(Qubit => Unit is Adj + Ctl)` e corresponde ao único qubit unitário:

\begin{Equation} \begin{bmatrix} 1 & 0 \\ \\ % FIXME: isso atualmente usa o quadwhack hack.
0 & i \end{bmatrix} \end{Equation}

#### <a name="rotations"></a>Escalas ####

Além das operações Pauli e Clifford acima, o Q# prelúdio fornece uma variedade de formas de expressar rotações.
Conforme descrito em [operações de qubit único](xref:microsoft.quantum.concepts.qubit#single-qubit-operations), a capacidade de girar é essencial para algoritmos Quantum.

Começamos recuperando que podemos expressar qualquer operação de qubit único usando o $H $ e $T $ Gates, em que $H $ é a operação Hadamard e em que \begin{Equation} T \mathrel{: =} \begin{bmatrix} 1 & 0 \\ \\ % FIXME: atualmente, isso usa os de quatro de hack-back.
0 & e ^ {i \pi/4} \end{bmatrix} \end{Equation} esta é a raiz quadrada da <xref:Microsoft.Quantum.Intrinsic.S> operação, de modo que $T ^ 2 = S $.
A Gate $T $ é, por sua vez, implementada pela <xref:Microsoft.Quantum.Intrinsic.T> operação e tem assinatura `(Qubit => Unit is Adj + Ctl)` , indicando que se trata de uma operação unitário em um único qubit.

Embora isso seja, de princípio, suficiente para descrever qualquer operação arbitrária de qubit único, diferentes computadores de destino podem ter representações mais eficientes para rotações sobre operadores Pauli, de modo que o prelúdio inclui várias maneiras de convienently essas rotações.
O mais básico deles é a <xref:Microsoft.Quantum.Intrinsic.r> operação, que implementa uma rotação em torno de um eixo Pauli especificado, \Begin{Equation} R (\sigma, \phi) \mathrel{: =} \exp (-i \phi \sigma/2), \end{Equation}, em que $ \sigma $ é um operador Pauli, $ \phi $ é um ângulo e em que $ \exp $ representa o exponencial de matriz.
Ele tem assinatura `((Pauli, Double, Qubit) => Unit is Adj + Ctl)` , em que as duas primeiras partes da entrada representam os argumentos clássicos $ \sigma $ e $ \phi $ necessários para especificar o operador unitário $R (\sigma, \phi) $.
Podemos aplicar parcialmente $ \sigma $ e $ \phi $ para obter uma operação cujo tipo é o de um único qubit unitário.
Por exemplo, `R(PauliZ, PI() / 4, _)` tem tipo `(Qubit => Unit is Adj + Ctl)` .

> [!NOTE]
> A <xref:Microsoft.Quantum.Intrinsic.r> operação divide o ângulo de entrada por 2 e o multiplica por-1.
> Para $Z $ rotações, isso significa que $ \ket {0} $ eigenstate é girado por $-\phi/$2 e $ \ket {1} $ eigenstate é girado por $ \phi/$2, para que $ \ket {1} $ eigenstate seja girado por $ \phi $ em relação ao $ \ket {0} $ eigenstate.
>
> Em particular, isso significa que `T` e `R(PauliZ, PI() / 8, _)` difere apenas por uma [fase global](xref:microsoft.quantum.glossary#global-phase)irrelevante.
> Por esse motivo, $T $ às vezes é conhecido como a porta $ \frac{\pi} {8} $.
>
> Observe também que girar em volta `PauliI` simplesmente aplica uma fase global de $ \phi/$2. Embora essas fases sejam irrelevantes, como argumentadas nos [documentos conceituais](xref:microsoft.quantum.concepts.qubit), elas são relevantes para `PauliI` rotações controladas.

Em algoritmos Quantum, geralmente é útil expressar rotações como frações dyadic, de modo que $ \phi = \pi k/2 ^ n $ para algumas $k na \mathbb{Z} $ e $n na \mathbb{N} $.
A <xref:Microsoft.Quantum.Intrinsic.RFrac> operação implementa uma rotação em um eixo de Pauli especificado usando essa convenção.
Ele difere de <xref:Microsoft.Quantum.Intrinsic.R> quando o ângulo de rotação é especificado como duas entradas do tipo `Int` , interpretado como uma fração dyadic.
Portanto, o `RFrac` tem assinatura `((Pauli, Int, Int, Qubit) => Unit is Adj + Ctl)` .
Ele implementa o único qubit unitário $ \exp (i \pi k \sigma/2 ^ n) $, em que $ \sigma $ é a matriz Pauli correspondente ao primeiro argumento, $k $ é o segundo argumento e $n $ é o terceiro argumento.
`RFrac(_,k,n,_)` é o mesmo que `R(_,-πk/2^n,_)` ; Observe que o ângulo é o *negativo* da fração.

A <xref:Microsoft.Quantum.Intrinsic.Rx> operação implementa uma rotação em volta do eixo Pauli $X $.
Ele tem assinatura `((Double, Qubit) => Unit is Adj + Ctl)` .
`Rx(_, _)` é o mesmo que `R(PauliX, _, _)`.

A <xref:Microsoft.Quantum.Intrinsic.Ry> operação implementa uma rotação em volta do eixo Pauli $Y $.
Ele tem assinatura `((Double, Qubit) => Unit is Adj + Ctl)` .
`Ry(_, _)` é o mesmo que `R(PauliY,_ , _)`.

A <xref:Microsoft.Quantum.Intrinsic.Rz> operação implementa uma rotação em volta do eixo Pauli $Z $.
Ele tem assinatura `((Double, Qubit) => Unit is Adj + Ctl)` .
`Rz(_, _)` é o mesmo que `R(PauliZ, _, _)`.

A <xref:Microsoft.Quantum.Intrinsic.R1> operação implementa uma rotação pelo valor determinado em relação a $ \ket {1} $, a eigenstate $-$1 de $Z $.
Ele tem assinatura `((Double, Qubit) => Unit is Adj + Ctl)` .
`R1(phi,_)` é o mesmo que o `R(PauliZ,phi,_)` seguido por `R(PauliI,-phi,_)` .

A <xref:Microsoft.Quantum.Intrinsic.R1Frac> operação implementa uma rotação fracionária pelo valor determinado em volta do Z = 1 eigenstate.
Ele tem assinatura `((Int,Int, Qubit) => Unit is Adj + Ctl)` .
`R1Frac(k,n,_)` é o mesmo que o `RFrac(PauliZ,-k.n+1,_)` seguido por `RFrac(PauliI,k,n+1,_)` .

Um exemplo de uma operação de rotação (em Pauli $Z $ Axis, nessa instância) mapeada para o Bloch Sphere é mostrado abaixo:

![Operação de rotação mapeada na esfera Bloch](~/media/prelude_rotationBloch.png)

#### <a name="multi-qubit-operations"></a>Operações qubit ####

Além das operações de qubit único acima, o prelúdio também define várias operações qubit.

Primeiro, a <xref:Microsoft.Quantum.Intrinsic.CNOT> operação executa uma porta controlada padrão `NOT` , \begin{Equation} \operatorname{CNOT} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \end{bmatrix}.
\end{Equation} tem assinatura `((Qubit, Qubit) => Unit is Adj + Ctl)` , representando que $ \operatorname{CNOT} $ atua unitarily em dois qubits individuais.
`CNOT(q1, q2)` é o mesmo que `(Controlled X)([q1], q2)`.
Como o `Controlled` functor permite controlar em um registro, usamos o literal de matriz `[q1]` para indicar que queremos apenas um controle.

A <xref:Microsoft.Quantum.Intrinsic.CCNOT> operação executa a porta não controlada de forma dupla, às vezes também conhecida como portão Toffoli.
Ele tem assinatura `((Qubit, Qubit, Qubit) => Unit is Adj + Ctl)` .
`CCNOT(q1, q2, q3)` é o mesmo que `(Controlled X)([q1, q2], q3)`.

A <xref:Microsoft.Quantum.Intrinsic.SWAP> operação troca os Estados de Quantum de dois qubits.
Ou seja, ele implementa a matriz unitário \begin{Equation} \operatorname{SWAP} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \end{bmatrix}.
\end{Equation} ele tem assinatura `((Qubit, Qubit) => Unit is Adj + Ctl)` .
`SWAP(q1,q2)` é equivalente a `CNOT(q1, q2)` seguido de `CNOT(q2, q1)` e depois `CNOT(q1, q2)` .

> [!NOTE]
> O portão de permuta *não* é o mesmo que reorganizar os elementos de uma variável com o tipo `Qubit[]` .
> A aplicação `SWAP(q1, q2)` de causa uma alteração no estado do qubits referenciado por `q1` e `q2` , enquanto `let swappedRegister = [q2, q1];` afeta apenas a forma como nos referimos a esses qubits.
> Além disso, `(Controlled SWAP)([q0], (q1, q2))` permite que `SWAP` o seja condicionado no estado de um terceiro qubit, que não podemos representar pela reorganização dos elementos.
> A porta de troca controlada, também conhecida como portão Fredkin, é eficiente o suficiente para incluir toda a computação clássica.

Por fim, o prelúdio fornece duas operações para representar exponencials de operadores de Pauli de vários qubit.
A <xref:Microsoft.Quantum.Intrinsic.Exp> operação executa uma rotação com base em um produto tensor de matrizes Pauli, conforme representado pelo qubit unitário \Begin{Equation} \operatorname{exp} (\vec{\sigma}, \phi) \mathrel{: =} \exp\left (i \phi \ sigma_0 \otimes \ sigma_1 \otimes \cdots \otimes \ sigma_n \right), \end{Equation}, em que $ \vec{\sigma} = (\ sigma_0, \ sigma_1, \dots, \ sigma_n) $ é uma sequência de operadores de qubit de Pauli único e em que $ \phi $ é um ângulo.
A `Exp` rotação representa $ \vec{\sigma} $ como uma matriz de `Pauli` elementos, de modo que ele tem assinatura `((Pauli[], Double, Qubit[]) => Unit is Adj + Ctl)` .

A <xref:Microsoft.Quantum.Intrinsic.ExpFrac> operação executa a mesma rotação, usando a notação de fração dyadic discutida acima.
Ele tem assinatura `((Pauli[], Int, Int, Qubit[]) => Unit is Adj + Ctl)` .

> [!WARNING]
> Os exponencials do produto tensor dos operadores Pauli não são os mesmos que os produtos tensor dos operadores de Pauli.
> Ou seja, $e ^ {i (Z \otimes Z) \phi} \ne e ^ {i Z \phi} \otimes e ^ {i Z \phi} $.

### <a name="measurements"></a>Medidas ###

Ao medir, a eigenvalue + 1 do operador que está sendo medido corresponde a um `Zero` resultado e-1 eigenvalue a um `One` resultado.

> [!NOTE]
> Embora essa Convenção possa parecer estranha, ela tem duas vantagens muito interessantes.
> Primeiro, observar o resultado $ \ket {0} $ é representado pelo `Result` valor `Zero` , enquanto que a observação $ \ket {1} $ corresponde a `One` .
> Em segundo lugar, podemos anotar que o eigenvalue $ \lambda $ corresponde a um resultado $r $ é $ \lambda = (-1) ^ r $.

As operações de medição não dão suporte nem a `Adjoint` nem a `Controlled` functor.

A <xref:Microsoft.Quantum.Intrinsic.Measure> operação executa uma medida conjunta de um ou mais qubits no produto especificado dos operadores Pauli.
Se a matriz Pauli e a matriz qubit tiverem comprimentos diferentes, a operação falhará.
`Measure` tem assinatura `((Pauli[], Qubit[]) => Result)` .

Observe que uma medida conjunta não é a mesma de medir cada qubit individualmente.
Por exemplo, considere o estado $ \ket {11} = \ket {1} \otimes \Ket {1} = X\otimes X \ket {00} $.
Medindo $Z _0 $ e $Z _1 $ individualmente, obtemos os resultados $r _0 = $1 e $r _1 = $1.
Medindo $Z _0 Z_1 $, no entanto, obtemos o único resultado $r _ {\textrm{Joint}} = $0, representando que a emparelhação de $ \ket {11} $ é positiva.
Put de forma diferente, $ (-1) ^ {r_0 + r_1} = (-1) ^ r_ {\textrm{joint}}) $.
Criticamente, como aprendemos *apenas* a paridade dessa medição, todas as informações de Quantum representadas na superposição entre os Estados 2 2-qubit de paridade positiva, $ \ket {00} $ e $ \ket {11} $, são preservadas.
Essa propriedade será essencial posteriormente, à medida que discutiremos a correção de erro.

Para sua conveniência, o prelúdio também fornece duas outras operações para medir o qubits.
Primeiro, como a execução de medidas de qubit único é bastante comum, o prelúdio define uma abreviação para esse caso.
A <xref:Microsoft.Quantum.Intrinsic.M> operação mede o operador Pauli $Z $ em um único qubit e tem assinatura `(Qubit => Result)` .
`M(q)` é equivalente a `Measure([PauliZ], [q])`.

O <xref:microsoft.quantum.measurement.MultiM> mede o operador Pauli $Z $ *separadamente* em cada uma das matrizes de qubits, retornando a *matriz* de `Result` valores obtidos para cada qubit.
Em alguns casos, isso pode ser otimizado. Ele tem assinatura ( `Qubit[] => Result[])` .
`MultiM(qs)` é equivalente a:

```qsharp
mutable rs = new Result[Length(qs)];
for (index in 0..Length(qs)-1)
{
    set rs[index] = M(qs[index]);
}
return rs;
```

## <a name="extension-functions-and-operations"></a>Funções e operações de extensão ##

Além disso, o prelúdio define um conjunto avançado de funções matemáticas e de conversão de tipo no nível do .NET para uso no Q# código.
Por exemplo, o <xref:Microsoft.Quantum.Math> namespace define operações úteis, como <xref:Microsoft.Quantum.Math.Sin> e <xref:Microsoft.Quantum.Math.Log> .
A implementação fornecida pelo kit de desenvolvimento Quantum usa a base class library clássica do .NET e, portanto, pode envolver uma viagem de ida e volta de comunicação adicional entre os programas Quantum e seus drivers clássicos.
Embora isso não apresente um problema para um simulador local, isso pode ser um problema de desempenho ao usar um simulador remoto ou hardware real como um computador de destino.
Dito isso, um computador de destino individual pode mitigar esse impacto no desempenho substituindo essas operações por versões mais eficientes para esse sistema específico.

### <a name="math"></a>Matemática ###

O <xref:Microsoft.Quantum.Math> namespace fornece muitas funções úteis da [ `System.Math` classe](https://docs.microsoft.com/dotnet/api/system.math?view=netframework-4.7.1&preserve-view=true)da biblioteca de classes base do .net.
Essas funções podem ser usadas da mesma maneira que qualquer outra Q# função:

```qsharp
open Microsoft.Quantum.Math;
// ...
let y = Sin(theta);
```

Onde um método estático do .NET foi sobrecarregado com base no tipo de seus argumentos, a Q# função correspondente é anotada com um sufixo que indica o tipo de sua entrada:

```qsharp
let x = AbsI(-3); // x : Int = 3
let y = AbsD(-PI()); // y : Double = 3.1415...
```


### <a name="bitwise-operations"></a>Operações bits ###

Por fim, o <xref:Microsoft.Quantum.Bitwise> namespace fornece várias funções úteis para manipular inteiros por meio de operadores bit a bit.
Por exemplo, <xref:Microsoft.Quantum.Bitwise.Parity> retorna a paridade de um número de bits para um inteiro como outro inteiro.
