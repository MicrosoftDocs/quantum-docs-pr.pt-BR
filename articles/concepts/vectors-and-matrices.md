---
Título: vetores e matrizes na descrição da computação Quantum: Aprenda as noções básicas de como trabalhar com vetores e matrizes.
Autor: QuantumWriter UID: Microsoft. Quantum. Concepts. vetores MS. Author: nawiebe@microsoft.com MS. Data: 12/11/2017 MS. Topic: artigo no-loc:
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

# <a name="vectors-and-matrices"></a>Vetores e matrizes

Alguma familiaridade com vetores e matrizes é essencial para entender a computação Quantum. Fornecemos uma breve introdução abaixo e os leitores interessados são recomendados para ler uma referência padrão em Algebra linear, como *Strang, G. (1993). Introdução à algebra linear (Vol. 3). Wellesley, MA: Wellesley-Cambridge, Press* ou uma referência online, como [Algebra linear](http://joshua.smcvt.edu/linearalgebra/).

Um vetor de coluna (ou simplesmente [*vetor*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $ v $ de Dimension (ou tamanho) $ n $ é uma coleção de $ n $ números complexos $ (v_1, v_2, \ldots, v_n) $ organizados como uma coluna:

$$v =\begin{bmatrix}
v_1\\\\
v_2\\\\
\vdots\\\\
v_n\end{bmatrix}$$

A norma de um vetor $ v $ é definida como $ \sqrt { \sum \_ i | v \_ | ^ 2 } $ . Um vetor é considerado como sendo a norma da unidade (ou, como alternativa, é chamado de [*vetor de unidade*](https://en.wikipedia.org/wiki/Unit_vector)) se a sua norma for $ 1 $ . O [*adjoin de um vetor*](https://en.wikipedia.org/wiki/Adjoint_matrix) $ v $ é indicado $ como v ^ \dagger $ e é definido para ser o seguinte vetor de linha, em que $ \* $ denota o conjugado complexo,

$$\begin{bmatrix}v_1 \\\\ \vdots \\\\ v_n \end{bmatrix} ^ \dagger = \begin{bmatrix} v_1 ^ * & \cdots & v_n ^ *\end{bmatrix}$$

A maneira mais comum de multiplicar dois vetores juntos é por meio do [*produto interno*](https://en.wikipedia.org/wiki/Inner_product_space), também conhecido como produto de ponto.  O produto interno fornece a projeção de um vetor para outro e é inestimável na descrição de como expressar um vetor como uma soma de outros vetores mais simples.  O produto interno entre $ u $ e $ v $ , denotado $ \left \langle u, v \right \rangle $ é definido como

$$
\langleu, v \rangle = u ^ \dagger v = u \_ 1 ^ { \* } v_1 + \cdots + u \_ n ^ { \* } v \_ n.
$$

Essa notação também permite que a norma de um vetor $ v $ seja escrita como $ \sqrt { \langle v, v \rangle } $ .

Podemos multiplicar um vetor com um número $ c $ para formar um novo vetor cujas entradas são multiplicadas por $ c $ . Também podemos adicionar dois vetores $ u $ e $ v $ para formar um novo vetor cujas entradas são a soma das entradas de $ u $ e $ v $ . Essas operações são descritas abaixo:

$$\mathrm{Se } ~ u=\begin{bmatrix}
u_1\\\\
u_2\\\\
\vdots\\\\
u_n \end{bmatrix} ~ \mathrm { e}~
l=\begin{bmatrix}
    v_1\\\\
    v_2\\\\
    \vdots\\\\
    v_n \end{bmatrix} , ~ \mathrm { em seguida,}~
au + BV=\begin{bmatrix}
au_1 + bv_1\\\\
au_2 + bv_2\\\\
\vdots\\\\
au_n + bv_n \end{bmatrix} .
$$

Uma [*matriz*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) de tamanho $ m \times n $ é uma coleção de $ $ números complexos de MN organizadas nas $ $ linhas m e $ n $ colunas, conforme mostrado abaixo:

$$D= 
\begin{bmatrix}
M_ { 11 } ~~ M_ { 12 } ~~ \cdots ~~ M_ { 1N}\\\\
M_ { 21 } ~~ M_ { 22 } ~~ \cdots ~~ M_ { 2n}\\\\
\ddots\\\\
M_ { M1 } ~~ M_ { m2 } ~~ \cdots ~~ M_ { MN}\\\\
\end{bmatrix}.$$

Observe que um vetor de dimensão $ n $ é simplesmente uma matriz de tamanho $ n \times 1 $ . Assim como acontece com os vetores, podemos multiplicar uma matriz com um número $ c $ para obter uma nova matriz em que cada entrada é multiplicada por $ c $ , e podemos adicionar duas matrizes do mesmo tamanho para produzir uma nova matriz cujas entradas são a soma das respectivas entradas das duas matrizes. 

## <a name="matrix-multiplication-and-tensor-products"></a>Multiplicação de matriz e produtos tensor

Também podemos multiplicar duas matrizes $ m $ da dimensão $ m \times n $ e $ n $ da dimensão $ n \times p $ para obter uma nova matriz $ p $ da dimensão $ m p da \times $ seguinte maneira:

\begin{align}
&\begin{bmatrix}
    M_ { 11 } ~~ M_ { 12 } ~~ \cdots ~~ M_ { 1N}\\\\
    M_ { 21 } ~~ M_ { 22 } ~~ \cdots ~~ M_ { 2n}\\\\
    \ddots\\\\
    M_ { M1 } ~~ M_ { m2 } ~~ \cdots ~~ M_ { MN}
\end{bmatrix}
\begin{bmatrix}
N_ { 11 } ~~ N_ { 12 } ~~ \cdots ~~ N_ { 1P}\\\\
N_ { 21 } ~~ N_ { 22 } ~~ \cdots ~~ N_ { 2P}\\\\
\ddots\\\\
N_ { N1 } ~~ N_ { N2 } ~~ \cdots ~~ N_ { NP}
\end{bmatrix}=\begin{bmatrix}
P_ { 11 } ~~ P_ { 12 } ~~ \cdots ~~ P_ { 1P}\\\\
P_ { 21 } ~~ P_ { 22 } ~~ \cdots ~~ P_ { 2P}\\\\
\ddots\\\\
P_ { M1 } ~~ P_ { m2 } ~~ \cdots ~~ P_ { MP}
\end{bmatrix}
\end{align}

onde as entradas de $ P $ são $ P_ { IK } = \sum _j M_ { IJ } N_ { JK } $ . Por exemplo, a entrada $ P_ { 11 } $ é o produto interno da primeira linha de $ M $ com a primeira coluna de $ N $ . Observe que, como um vetor é simplesmente um caso especial de uma matriz, essa definição se estende à multiplicação do vetor de matriz. 

Todas as matrizes que consideramos serão matrizes quadradas, em que o número de linhas e colunas são iguais, ou vetores, que correspondem a apenas $ uma $ coluna. Uma matriz quadrada especial é a [*matriz de identidade*](https://en.wikipedia.org/wiki/Identity_matrix), denotada $ \boldone $ , que tem todos os elementos diagonais iguais a $ 1 $ e os elementos restantes iguais a $ 0 $ :

$$\boldone=\begin{bmatrix}
1 ~~ 0 ~~ \cdots ~~ 0\\\\
0 ~~ 1 ~~ \cdots ~~ 0\\\\
~~ \ddots\\\\
0 ~~ 0 ~~ \cdots ~~ 1 \end{bmatrix} .$$

Para uma matriz quadrada $ $ , dizemos que uma matriz $ B $ é seu [*inverso*](https://en.wikipedia.org/wiki/Invertible_matrix) se a $ = BA = \boldone $ . O inverso de uma matriz não precisa existir, mas quando ela existe, ela é exclusiva e denotamos $ um ^ { -1 } $ . 

Para qualquer matriz $ m $ , a transpoção adjacente ou conjugada de $ M $ é uma matriz $ N $ , de modo que $ N_ { IJ } = M_ { ji } ^ \* $ . O adjoin of $ m $ é geralmente indicado $ m ^ \dagger $ . Dizemos que uma matriz $ U $ é [*unitário*](https://en.wikipedia.org/wiki/Unitary_matrix) se $ uu ^ \dagger = u ^ \dagger u = \boldone $ ou equivalente, $ u ^ { -1 } = U ^ \dagger $ .  Talvez a propriedade mais importante das matrizes de unitários seja que elas preservam a norma de um vetor.  Isso acontece porque 

$$\langlev, v \rangle = v ^ v v ^ u ^-1 U v v ^ u ^ u v s v \dagger = \dagger { } = \dagger \dagger = \langle , u v \rangle .$$  

Uma matriz $ M $ é considerada [*Hermitian*](https://en.wikipedia.org/wiki/Hermitian_matrix) se m $ = m ^ \dagger $ .

Por fim, o [*produto tensor*](https://en.wikipedia.org/wiki/Tensor_product) (ou o produto Kronecker) de duas matrizes $ $ de tamanho $ m \times n $ e $ n $ de tamanho $ p \times q $ é uma matriz maior $ p = m \otimes n $ de tamanho $ MP \times NQ $ e é obtido de $ M $ e n da $ $ seguinte maneira:

\begin{align}
    M \otimes N&=
    \begin{bmatrix}
        M_ { 11 } ~~ \cdots ~~ M_ { 1N }\\\\
        \ddots\\\\
        M_ { M1 } ~~ \cdots ~~ M_ { MN  }
    \end{bmatrix}
    \otimes
    \begin{bmatrix}
        N_ { 11 } ~~ \cdots ~~ N_ { 1Q  }\\\\
        \ddots\\\\
        N_ { P1 } ~~ \cdots ~~ N_ { pq}
    \end{bmatrix}\\\\
    &=
    \begin{bmatrix}
        M_ { 11 } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1Q } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { pq } \end{bmatrix} ~~ \cdots  ~~ 
        M_ { 1N } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1Q } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { pq }  \end{bmatrix}\\\\
        \ddots\\\\
        M_ { M1 } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1Q } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { pq } \end{bmatrix} ~~ \cdots  ~~ 
        M_ { Mn } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1Q } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { pq }  \end{bmatrix}
    \end{bmatrix}.
\end{align}

Isso é melhor demonstrado com alguns exemplos:

$$
    \begin{bmatrix}
        a \\\\ b \end{bmatrix} \otimes \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix}=
    \begin{bmatrix}
        a \begin{bmatrix} c \\\\ d \\\\ e\end{bmatrix}
        \\\\[1,5 em] b \begin{bmatrix} c \\\\ d \\\\ e\end{bmatrix}
    \end{bmatrix}
    =r a \begin{bmatrix} \\\\ d \\\\ a e \\\\ b c \\\\ b d \\\\\end{bmatrix}
$$

e

$$
    \begin{bmatrix}
        a \ b \\\\ c \ d\end{bmatrix}
    \otimes 
    \begin{bmatrix}
        e \ f \\\\ g \ h\end{bmatrix}
     =
    \begin{bmatrix}
    um\begin{bmatrix}
    e \ f \\\\ g \ h\end{bmatrix}
    b\begin{bmatrix}
    e \ f \\\\ g \ h\end{bmatrix}
    \\\\[1em] c\begin{bmatrix}
    e \ f \\\\ g \ h\end{bmatrix}
    3D\begin{bmatrix}
    e \ f \\\\ g \ h\end{bmatrix}
    \end{bmatrix}
    =
    \begin{bmatrix}
    AE \ AF \ ser \ BF\\\\
    AG \ Ah \ BG \ BH\\\\
    CE \ CF \ de \ DF\\\\
    CG \ ch \ DG \ DH \end{bmatrix} .
$$

Uma Convenção de notação útil final ao redor dos produtos tensor é que, para qualquer vetor $ $ ou matriz $ M $ , $ v ^ { \otimes n } $ ou $ m ^ { \otimes n } $ é curto para $ um $ produto tensor repetido n-fold.  Por exemplo:

\begin{align}
&\begin{bmatrix}1 \\\\ 0 1 \end{bmatrix} ^ { \otimes } = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} , \qquad \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} ^ { \otimes 2 } = \begin{bmatrix} 1 \\\\ 0 \\\\ 0 \\\\ 0 \end{bmatrix} , \qquad \begin{bmatrix} 1 \\\\ -1 \end{bmatrix} ^ { \otimes 2 } = \begin{bmatrix} 1 \\\\ -1 \\\\ -1 \\\\ 1 \end{bmatrix} ,\\\\
  &\begin{bmatrix}0 & 1 \\\\ 1 & 0 \end{bmatrix} ^ { \otimes 1 } = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} , \qquad \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} ^ { \otimes 2 } = \begin{bmatrix} 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 1 & 0 & & \end{bmatrix} 0 0.
\end{align}
