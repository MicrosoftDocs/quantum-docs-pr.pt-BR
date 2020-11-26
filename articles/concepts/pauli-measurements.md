---
Título: Descrição de medidas de Pauli: saiba como trabalhar com operações de medição de Pauli única e qubit.
Autor: bradben UID: Microsoft. Quantum. Concepts. Pauli MS. Author: v-benbra MS. Date: 12/11/2017 MS. tópico: article no-loc:
- "Q#"
- "$$v"
- "$$"
- "$$"
- "$"
- "$"
- "$"
- "$$"
- "\cdots"
- "bmatrix"
- "\ddots"
- "\equiv"
- "\sum"
- "\begin"
- "\end"
- "\sqrt"
- "\otimes"
- "{"
- "}"
- "\text"
- "\phi"
- "\kappa"
- "\psi"
- "\alpha"
- "\beta"
- "\gamma"
- "\delta"
- "\omega"
- "\bra"
- "\ket"
- "\boldone"
- "\\\\"
- "\\"
- "="
- "\frac"
- "\text"
- "\mapsto"
- "\dagger"
- "\to"
- "\begin{cases}"
- "\end{cases}"
- "\operatorname"
- "\braket"
- "\id"
- "\expect"
- "\defeq"
- "\variance"
- "\dd"
- "&"
- "\begin{align}"
- "\end{align}"
- "\Lambda"
- "\lambda"
- "\Omega"
- "\mathrm"
- "\left"
- "\right"
- "\qquad"
- "\times"
- "\big"
- "\langle"
- "\rangle"
- "\bigg"
- "\Big"
- "|"
- "\mathbb"
- "\vec"
- "\in"
- "\texttt"
- "\ne"
- "<"
- ">"
- "\leq"
- "\geq"
- "~~"
- "~"
- "\begin{bmatrix}"
- "\end{bmatrix}"
- "\_"

---

# <a name="pauli-measurements"></a>Medições de Pauli

Nas discussões anteriores, concentramos-se em medidas de base computacional.
Na verdade, há outras medidas comuns que ocorrem na computação Quantum que, de uma perspectiva de notação, são convenientes para expressar em termos de medidas de base computacional.
À medida que você trabalha com Q# o, o tipo mais comum de medidas que você encontrará provavelmente serão as *medidas Paulis*, que generalizam as medidas de base computacional para incluir medidas em outras bases e de paridade entre diferentes qubits.
Nesses casos, é comum discutir a medição de um operador Pauli, em geral, um operador como $ X, Y, z $ ou $ z \otimes z, x \otimes x, x \otimes Y $ e assim por diante. 

> [!TIP]
> No Q# , os operadores qubit Pauli geralmente são representados por matrizes do tipo `Pauli[]` .
> Por exemplo, para representar $ X \otimes Z \otimes Y $ , você pode usar a matriz `[PauliX, PauliZ, PauliY]` .

Discutir a medição em termos de operadores Pauli é especialmente comum no subcampo de correção de erro Quantum.
No Q# , seguimos uma convenção semelhante; agora, explicamos essa exibição alternativa de medidas.

Antes de se aprofundar nos detalhes de como pensar em uma medida Pauli, é útil pensar em que a medição de um único qubit dentro de um computador Quantum faz o estado Quantum.
Imagine que tenhamos um $ $ estado Quantum de n-qubit; então, medindo uma qubit imediatamente, as regras de metade das $ duas possibilidades de 2 ^ n $ em que o Estado poderia estar.
Em outras palavras, a medida projeta o estado da Quantum em um dos dois espaços.
Podemos generalizar a maneira como pensamos na medição para refletir essa intuição.

Para identificar esses subespaços de forma concisa, precisamos de uma linguagem para descreve-los.
Uma maneira de descrever os dois subespaços é especificando-os por meio de uma matriz que tem apenas duas eigenvalues exclusivas, tomadas pela Convenção para ser $ \pm 1 $ .
Para obter um exemplo simples de descrição de subespaços dessa forma, considere $ Z $ :

$$
\begin{align}
  Z & = \begin{bmatrix} 1 & 0 \\\\ 0 & -1 \end{bmatrix} .
\end{align}
$$

Lendo os elementos diagonais da matriz Pauli- $ Z $ , podemos ver que $ Z $ tem dois eigenvectors, $ \ket { 0 } $ e $ \ket { 1 } $ , com eigenvalues correspondente $ \pm 1 $ .
Portanto, se medirmos o qubit e obtivermos `Zero` (correspondente ao estado $ \ket { 0 } $ ), sabemos que o estado de nosso qubit é um $ eigenstate + 1 $ do $ $ operador Z.
Da mesma forma, se obtivermos `One` , sabemos que o estado de nosso qubit é um $ -1 $ eigenstate de $ Z $ . Esse processo é mencionado na linguagem de medidas Pauli como "medindo Pauli $ Z $ " e é totalmente equivalente a executar uma medição de base computacional.

Qualquer $ \times matriz 2 2 $ que seja uma transformação unitário de $ Z $ também atende a esses critérios.
Ou seja, também poderíamos usar uma matriz $ a = u ^ \dagger Z u $ , em que $ U $ é qualquer outra matriz de unitário, para dar uma matriz que define os dois resultados de uma medida em seu $ \pm 1 $ eigenvectors.
A notação de medidas Pauli faz referência a essa equivalência unitário identificando $ as medidas X, Y, Z $ como medidas equivalentes que uma delas pode fazer para obter informações de um qubit.
Essas medidas são fornecidas abaixo para sua conveniência.


|Transformação unitário de medição Pauli ||
|-------------------|------------------------|
|$ $ Z |               $\boldone$             |
|$ $ X | $H               $                    |
|$ $ S | $HS ^               {\dagger}$         |

Ou seja, usar esse idioma, "Measure $ Y $ " é equivalente a aplicar $ HS ^ \dagger $ e, em seguida, medir na base computacional, em que [`S`](xref:Microsoft.Quantum.Intrinsic.S) é uma operação Quantum intrínseca às vezes chamada de "portão de fase" e pode ser simulada pela matriz unitário

$$
\begin{align}
    S =\begin{bmatrix}
        1 & 0 \\\\ 0 & i \end{bmatrix} .
\end{align}
$$

Também é equivalente a aplicar $ HS ^ \dagger $ ao vetor de estado Quantum e, em seguida, medir $ Z $ , de modo que a seguinte operação seja equivalente a `Measure([PauliY], [q])` :

```Q#
operation MeasureY(qubit : Qubit) : Result {
    mutable result = Zero;
    within {
        Adjoint S(q);
        H(q);
    } apply {
        set result = M(q);
    }
    return result;
}
```

O estado correto seria então encontrado transformando de volta para a base computacional, que valores para aplicar $ sh $ ao vetor de estado Quantum; no trecho acima, a transformação de volta para a base computacional é manipulada automaticamente pelo uso do `within … apply` bloco.

No Q# , dizemos que o resultado---ou seja, as informações clássicas extraídas da interação com o estado---são dadas por um `Result` valor $ j \in \\ { \texttt { zero } , \texttt { um } \\ } $ que indica se o resultado está no $ (-1) ^ j $ eigenspace do operador Pauli medido.


## <a name="multiple-qubit-measurements"></a>Medições de várias qubit

As medições de operadores qubit Pauli são definidas da mesma forma, como visto em:

$$
Z \otimes z 1 0 0 0 0 = \begin{bmatrix} & & -1 0 0 0 0 & \\\\ & & & \\\\ & & -1 & 0 \\\\ & & & \end{bmatrix} 0 0 0 1.
$$

Assim, os produtos tensor de dois operadores Pauli- $ Z $ formam uma matriz composta de dois espaços que consistem em $ + 1 $ e $ -1 $ eigenvalues.
Assim como no caso de qubit único, ambos constituem um meio-espaço que significa que metade do espaço de vetor acessível pertence ao $ + 1 $ eigenspace e à metade restante para $ -1 $ eigenspace.
Em geral, é fácil ver a definição do produto tensor que qualquer produto tensor de operadores Pauli- $ Z $ e a identidade também obedece a isso.
Por exemplo,

$$
\begin{align}
    \otimes \boldone Z =\begin{bmatrix}
        1 & 0 & 0 0 &\\\\
        0 &  1 &  0 &  0 \\\\
        0 &  0 & -1 &  0 \\\\
        0 &  0 &  0 & -1 \end{bmatrix} .
\end{align}
$$

Como antes, qualquer transformação unitário dessas matrizes também descreve dois espaços de meia rotulados por $ \pm 1 $ eigenvalues.
Por exemplo, $ x \otimes x = h \otimes h (z \otimes z) h \otimes h $  da identidade que $ Z = HxH $ .
Semelhante ao caso qubit, todas as medidas de Pauli qubit podem ser escritas como $ u ^ \dagger (Z \otimes \id ) u $ para $ 4 matrizes de 2 \times $ $ unidades $ . Enumeramos as transformações na tabela a seguir.

> [!NOTE]
>Na tabela a seguir, usamos $ \operatorname { swap } $ para indicar a matriz >$$
> \begin{align}
>     \operatorname{TROCAR } &=
>     \left( \begin { matriz}
>1 & 0 & 0 0 &\\\\
>         0 & 0 & 1 & 0 \\\\
>         0 & 1 & 0 & 0 \\\\
>0 & 0 & 0 & 1 > \end { matriz } \right ) >     \end{align}
> $$
> usado para simular a operação intrínseca [`SWAP`](xref:Microsoft.Quantum.Intrinsic) .

|Transformação unitário de medição Pauli ||
|----------------------|------------------------|
|$ \otimes \boldone Z $ | $\boldone\otimes \boldone$|
|$ \otimes \boldone X $ | $ \otimes \boldone H $|
|$ \otimes \boldone S $ | $ HS \dagger \otimes \boldone ^ $|
|$\boldone \otimes $ | $ \operatorname { permuta } Z $|
|$\boldone \otimes $ | $ \otimes \boldone \operatorname { permuta } X (H $ )|
|$\boldone \otimes s $ | $ (HS ^ \dagger \otimes \boldone ) \operatorname { permuta } $|
|$Z \otimes Z $ | $ \operatorname { CNOT } \_ { 10 } $|
|$X \otimes Z $ | $ \operatorname { CNOT } \_ { 10 } (H \otimes \boldone ) $|
|$S \otimes Z $ | $ \operatorname { CNOT } \_ { 10 } (HS ^ \dagger \otimes \boldone ) $|
|$Z \otimes X $ | $ \operatorname { CNOT } \_ { 10 } ( \boldone \otimes H) $|
|$X \otimes X $ | $ \operatorname { CNOT } \_ { 10 } (h \otimes h) $|
|$S \otimes X $ | $ \operatorname { CNOT } \_ { 10 } (HS ^ \dagger \otimes H) $|
|$Z \otimes Y $ | $ \operatorname { CNOT } \_ { 10 } ( \boldone \otimes HS ^ \dagger ) $|
|$X \otimes Y $ | $ \operatorname { CNOT } \_ { 10 } (H \otimes HS ^ \dagger ) $|
|$S \otimes Y $ | $ \operatorname { CNOT } \_ { 10 } (HS ^ \dagger \otimes HS ^ \dagger ) $|

Aqui, a [`CNOT`](xref:Microsoft.Quantum.Intrinsic.CNOT) operação é exibida pelo seguinte motivo.
Cada medida de Pauli que não inclui a $ \boldone $ matriz é equivalente a um unitário de $ z \otimes z $ pelo raciocínio acima.
O eigenvalues de $ z \otimes z $ depende apenas da paridade do qubits que compõe cada vetor base computacional, e as operações controladas não servem para computar essa paridade e armazená-las no primeiro bit.
Depois que o primeiro bit é medido, podemos recuperar a identidade do espaço resultante, que é equivalente a medir o operador Pauli.

Uma observação adicional: embora possa ser tentador pressupor que medir $ z \otimes z $ é o mesmo que medir sequencialmente $ Z \otimes \mathbb { 1 } $ e, em seguida $ \mathbb { , 1 } \otimes Z $ , essa suposição seria falsa.
O motivo é que a medição de $ \otimes projetos z z é $ o estado da Quantum na $ eigenstate + 1 $ ou $ -1 $ desses operadores.
Medindo $ \otimes \mathbb { o z 1 } $ e, em seguida, $ \mathbb { 1 } \otimes $ a z projeta o vetor de estado da Quantum primeiro em um semestre de $ Z \otimes \mathbb { 1 } $ e, em seguida, em um semestre de $ \mathbb { 1 a } \otimes z $ . Como há quatro vetores de base computacional, a execução de ambas as medidas reduz o estado para um quarto de espaço e, portanto, reduz-a para um único vetor de computação.

## <a name="correlations-between-qubits"></a>Correlações entre qubits
Outra maneira de observar a medição de produtos tensor de matrizes Pauli como $ x \otimes x $ ou $ z \otimes z $ é que essas medidas permitem que você examine as informações armazenadas nas correlações entre os dois qubits.
A medição de $ X \otimes \id $ permite que você examine as informações armazenadas localmente no primeiro qubit.
Embora os dois tipos de medidas sejam igualmente valiosos na computação Quantum, o primeiro ilumina o poder da computação Quantum.
Ele revela que, na computação Quantum, geralmente as informações que você deseja aprender não são armazenadas em nenhum único qubit, mas armazenadas não localmente em todas as qubits de uma vez e, portanto, apenas examinando-as por meio de uma medida conjunta (por exemplo, $ z \otimes z $ ), essas informações se tornam manifestos.

Por exemplo, na correção de erros, muitas vezes desejamos saber qual erro ocorreu ao aprender nada sobre o estado que estamos tentando proteger.
O [exemplo de código de inversão de bits](https://github.com/microsoft/Quantum/tree/main/samples/error-correction/bit-flip-code) mostra um exemplo de como você pode fazer isso usando medidas como $ z \otimes z \otimes \id $ e $ \id \otimes z z \otimes $ . < ! --TODO: altere isso para um link para o navegador de exemplos assim que o exemplo de código de inversão de bits estiver integrado. -->

Operadores Pauli arbitrários, como $ X \otimes Y Z, \otimes \otimes \boldone $ também podem ser medidos.
Todos esses produtos tensor de operadores Pauli têm apenas dois eigenvalues $ \pm 1 $ e ambos eigenspaces constituem metades do espaço de vetor inteiro.
Portanto, eles coincidem com os requisitos declarados acima.

No Q# , essas medidas retornam $ j $ se a medida produz um resultado no eigenspace de sinal $ (-1) ^ j $ .
Ter medidas de Pauli como um recurso interno no Q# é útil porque a medição desses operadores requer cadeias longas de Gates e transformações de base controladas para descrever a diagonal de $ U $ portão necessário para expressar a operação como um produto tensor de $ Z $ e $ \id $ .
Ao ser capaz de especificar que você deseja realizar uma dessas medidas predefinidas, você não precisa se preocupar em como transformar sua base de forma que uma medida de base computacional forneça as informações necessárias.
Q# manipula todas as transformações de base necessárias automaticamente para você.
Para obter mais informações, consulte [`Measure`](xref:Microsoft.Quantum.Intrinsic.Measure) as [`MeasurePaulis`](xref:Microsoft.Quantum.Measurement.MeasurePaulis) operações e.

## <a name="the-no-cloning-theorem"></a>O No-Cloning teorema

As informações da Quantum são poderosas.
Ele nos permite fazer coisas incríveis, como números de fator exponencialmente mais rápidos do que os melhores algoritmos clássicos conhecidos, ou simular com eficiência sistemas de informações de alta correlação que exigem, de modo clássico, o custo exponencial para simular com precisão.
No entanto, há limitações no poder da computação Quantum.
Uma dessas limitações é fornecida pelo *teorema no-Cloning*.

O No-Cloning teorema é adequadamente nomeado.
Ele não permite a clonagem de Estados de Quantum genérico por um computador Quantum.
A prova do teorema é bastante simples.
Embora uma prova completa do teorema sem clonagem seja um pouco técnica para nossa discussão aqui, a prova no caso de nenhum qubits auxiliar adicional está dentro de nosso escopo.

Para esse computador Quantum, a operação de clonagem deve ser descrita por uma matriz unitário.
Não permitimos a medição, já que corromperia o estado Quantum que estamos tentando clonar.
Para simular a operação de clonagem, queremos que a matriz unitário usada tenha a propriedade que $$
  U \ket { \psi } \ket { 0 } = \ket { \psi }\ket{\psi}
$$
para qualquer estado $ \ket { \psi } $ .
Em seguida, a propriedade linear da multiplicação de matriz implica que, para qualquer segundo estado Quantum $ \ket { \phi } $ ,

$$
\begin{align}
    U \left [ \frac { 1 } { \sqrt { 2 } } \left ( \ket { \phi } + \ket { \psi } \right ) \right ] \ket { 0}
    &= \frac{ 1 } { \sqrt { 2 } } U \ket { \phi } \ket { 0}
      + \frac{1 } { \sqrt { 2 } } U \ket { \psi } \ket { 0 }\\\\
    &= \frac{ 1 } { \sqrt { 2 } } \left ( \ket { \phi } \ket { \phi }  +  \ket { \psi }\ket{\psi}
        \right) \\\\
    &\ne \left ( \frac { 1 } { \sqrt { 2 } } \left ( \ket { \phi } + \ket { \psi } \right ) \right ) \otimes \left ( \frac { 1 } { \sqrt { 2 } } \left ( \ket { \phi } + \ket { \psi } \right ) \right ).
\end{align}
$$

Isso fornece a intuição fundamental por trás do No-Cloning teorema: qualquer dispositivo que copia um estado de Quantum desconhecido deve induzir erros em pelo menos alguns dos Estados que ele copia.
Embora a principal suposição de que o Cloner atue linearmente no estado de entrada possa ser violada por meio da adição e da medição do qubits auxiliar, essas interações também vazam informações sobre o sistema por meio de estatísticas de medição e impedem a clonagem exata nesses casos.
Para obter uma prova mais completa do No-Cloning teorema, consulte [para obter mais informações](xref:microsoft.quantum.more-information).

A No-Cloning teorema é importante para uma compreensão qualitativa da computação Quantum porque, se você puder clonar os Estados da Quantum de forma incara, terá uma capacidade quase mágico de aprender com os Estados da Quantum.
Na verdade, você poderia violar o princípio de incerteza de vaunted da Heisenberg.
Como alternativa, você pode usar um Cloner ideal para pegar um único exemplo de uma distribuição de Quantum complexa e aprender tudo o que poderia ser possível saber sobre essa distribuição de apenas uma amostra.
Isso seria como você invertendo uma moeda e observando a cabeça e, depois, ao informar a um amigo sobre o resultado que eles respondem "Ah, a distribuição dessa moeda deve ser Bernoulli com $ p = 0.512643 \ ldots $ !"  Essa instrução seria não sensical porque um pouco de informação (o resultado dos cabeçotes) simplesmente não pode fornecer muitas informações necessárias para codificar a distribuição sem informações substanciais anteriores.
Da mesma forma, sem informações anteriores, não podemos clonar perfeitamente um estado Quantum da mesma forma que não podemos preparar uma Ensemble dessas moedas sem saber $ p $ .

As informações não são gratuitas na computação Quantum.
Cada qubit medido fornece uma única informação e o No-Cloning teorema mostra que não há nenhum backdoor que possa ser explorado para contornar a compensação fundamental entre as informações obtidas sobre o sistema e o distúrbios invocado sobre ele.
