---
Título: conceitos de matriz avançada Descrição: Saiba mais sobre os exponenciais eigenvectors, eigenvalues e Matrix, as ferramentas fundamentais usadas para descrever e simular os algoritmos Quantum.
Autor: QuantumWriter UID: Microsoft. Quantum. Concepts. Matrix-avançado MS. Author: nawiebe@microsoft.com MS. Data: 12/11/2017 MS. Topic: artigo no-loc:
- "$$"
- "$$"
- "$"
- "$"
- "$"
- "$$"
- "$$$"
- "$$$"
- "$$$"
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
# <a name="advanced-matrix-concepts"></a>Conceitos de matriz avançada #

Agora, estendemos nossa manipulação de matrizes para [*eigenvalues, eigenvectors*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) e [*exponencials*](https://en.wikipedia.org/wiki/Matrix_exponential) que formam um conjunto fundamental de ferramentas que precisamos para descrever e implementar os algoritmos Quantum.

## <a name="eigenvalues-and-eigenvectors"></a>Eigenvalues e eigenvectors ##

Deixe que $ M $ seja uma matriz quadrada e $ v $ seja um vetor que não seja o vetor de todos os zeros (ou seja, o vetor com todas as entradas iguais a $ 0 $ ).

Dizemos que $ v $ é um [*eigenvector*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) de $ M se o $ $ MV = vc $ de algum número $ c $ . Dizemos que $ c $ é o [*eigenvalue*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) correspondente ao eigenvector $ v $ . Em geral, uma matriz $ M $ pode transformar um vetor em qualquer outro vetor, mas um eigenvector é especial porque permanece inalterado, exceto por ser multiplicado por um número. Observe que se $ v $ for um eigenvector com eigenvalue $ c $ , $ o AV $ também será um eigenvector (para qualquer outro diferente de zero $ $ ) com o mesmo eigenvalue.

Por exemplo, para a matriz de identidade, cada vetor $ v $ é um eigenvector com eigenvalue $ 1 $ .

Como outro exemplo, considere uma [*matriz diagonal*](https://en.wikipedia.org/wiki/Diagonal_matrix) $ D $ que tem apenas entradas diferentes de zero na diagonal:

$$
\begin{bmatrix}
d_1 & 0 0 0 & \\\\ & d_2 & 0 \\\\ 0 & 0 & d_3 \end{bmatrix} .
$$

Os vetores

$$\begin{bmatrix}1 \\\\ 0 \\\\ 0 \end{bmatrix} , \begin{bmatrix} 0 \\\\ 1 \\\\ 0 \end{bmatrix} e \begin{bmatrix} 0 \\\\ 0 \\\\ 1\end{bmatrix}$$

são eigenvectors dessa matriz com eigenvalues $ d_1 $ , $ d_2 $ e $ d_3 $ , respectivamente. Se $ d_1 $ , $ d_2 $ e $ d_3 $ forem números distintos, esses vetores (e seus múltiplos) serão os únicos eigenvectors da matriz $ d $ . Em geral, para uma matriz diagonal, é fácil ler eigenvalues e eigenvectors. Eigenvalues são todos os números que aparecem na diagonal e seus respectivos eigenvectors são os vetores de unidade com uma entrada igual a $ 1 $ e as entradas restantes iguais a $ 0 $ .

Observe no exemplo acima que a eigenvectors de $ D $ formam uma base para $ $ vetores tridimensionais. Uma base é um conjunto de vetores, de modo que qualquer vetor pode ser escrito como uma combinação linear deles. Mais explicitamente, $ v_1 $ , $ v_2 $ e $ v_3 $ formam uma base se qualquer tipo $ de vetor v $ puder ser escrito como $ v = a_1 v_1 + a_2 v_2 + a_3 v_3 $ para alguns números $ a_1 $ , $ a_2 $ e $ a_3 $ .

Lembre-se de que uma matriz Hermitian (também chamada de auto-adjacente) é uma matriz quadrada complexa igual à sua própria transpoção conjugada complexa, enquanto uma matriz unitário é uma matriz quadrada complexa cujo inverso é igual à sua Transpose de conjugado ou complexa.
Para matrizes Hermitian e unitários, que são essencialmente as únicas matrizes encontradas na computação Quantum, há um resultado geral conhecido como [*Spectral teorema*](https://en.wikipedia.org/wiki/Spectral_theorem), que declara o seguinte: para qualquer matriz Hermitian ou unitário $ $ 2, existe um U unitário $ $ como $ m = u ^ \dagger D u $ para alguma matriz diagonal $ d $ . Além disso, as entradas diagonais de $ D $ serão o eigenvalues de $ M $ .

Já sabemos como calcular o eigenvalues e o eigenvectors de uma matriz diagonal $ D $ . Usando este teorema, sabemos que, se $ v $ for um eigenvector de $ D $ com eigenvalue $ c $ , ou seja, $ o DV = CV $ , $ U ^ \dagger v $ será um eigenvector de $ M $ com eigenvalue $ c $ . Isso ocorre porque

$$M (U ^ \dagger v) = u ^ \dagger d u (u ^ \dagger v) = U ^ \dagger d (u u ^ \dagger ) v = u ^ \dagger D v = c u ^ \dagger v.$$

## <a name="matrix-exponentials"></a>Exponenciais de matriz
Um [*exponencial de matriz*](https://en.wikipedia.org/wiki/Matrix_exponential) também pode ser definido de acordo com a analogia exata com a função exponencial.  O exponencial de matriz de uma matriz $ a $ pode ser expresso como

$$
e ^ A = \boldone + a + \frac { a ^ 2 } { 2! } + \frac { Um ^ 3 3 } { !}+\cdots
$$

Isso é importante porque a evolução do tempo mecânico da Quantum é descrita por uma matriz unitário do formato $ e ^ { IB } $ para a matriz Hermitian $ B $ .  Por esse motivo, a execução de exponencials de matriz é uma parte fundamental da computação Quantum e, como tal, Q # oferece rotinas intrínsecas para descrever essas operações.
Há muitas maneiras de fazer a computação de um exponencial de matriz em um computador clássico e, em geral, o aproximar de forma numérica como tal exponencial é muito perigoso com Peril.  Confira [*Cleve Moler e Charles Van empréstimo. "Dezenove duvidosa maneiras de computar o exponencial de uma matriz". SIAM revisar 20,4 (1978): 801-836*](https://doi.org/10.1137/S00361445024180) para obter mais informações sobre os desafios envolvidos.

A maneira mais fácil de entender como computar o exponencial de uma matriz é por meio de eigenvalues e eigenvectors dessa matriz.  Especificamente, o Spectral teorema discutido acima diz que para cada matriz Hermitian ou unitário $ a $ existe uma matriz unitário $ u $ e uma matriz diagonal $ d, de $ modo que u $ = ^ \dagger d u $ .  Devido às propriedades de unitarity, temos esse $ ^ 2 = u ^ \dagger d ^ 2 u $ e, da mesma forma, para qualquer Power $ p $ $ A ^ p = u ^ \dagger d ^ p u $ .  Se substituímos isso na definição de operador do exponencial de operador, obtemos:

$$
e ^ A = U ^ \dagger \left ( \boldone + d + \frac { d ^ 2 } { 2! } + \cdots \right ) U = u ^ \dagger \begin{bmatrix} \exp (D_ { 11 } ) & 0 & \cdots & 0 \\\\ 0 & \exp (D_ { 22 } ) & \cdots & 0 \\\\ \vdots & \vdots & \ddots & \vdots \\\\ 0 & 0 & \cdots & \exp (D_ { NN } ) \end{bmatrix} U.$$

Em outras palavras, se você transformar para o eigenbasis da matriz $ a $ , a computação do exponencial de matriz será equivalente a computar o exponencial comum do eigenvalues da matriz.  Como muitas operações na computação Quantum envolvem a execução de exponenciais de matriz, esse truque de transformar em eigenbasis de uma matriz para simplificar a execução do operador exponencial é exibido com frequência e é a base por trás de muitos algoritmos Quantum, como os métodos de simulação de Quantum Trotter – Suzuki-Style discutidos posteriormente neste guia.

Outra propriedade útil é se $ B $ for unitário e Hermitian, ou seja, $ b = b ^ { -1 } = b ^ \dagger $ e $ B ^ 2 = \boldone $ . Ao aplicar essa regra à expansão acima do exponencial de matriz e agrupar os $ \boldone $ e os $ $ termos B juntos, ele pode ver que, para qualquer valor real $ x $ a identidade

$$e ^ { iBx } = \boldone \cos (x) + iB\sin (x)$$


realiza. Esse truque é especialmente útil, pois ele permite que o motivo dos exponencials de matriz de ações tenha, mesmo se a dimensão de $ B $ for exponencialmente grande, para o caso especial quando $ B $ for unitário e Hermitian.
