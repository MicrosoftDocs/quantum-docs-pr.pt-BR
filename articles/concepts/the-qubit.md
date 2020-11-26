---
Título: o qubit na descrição da computação Quantum: Saiba mais sobre o qubits, a unidade fundamental de informações na computação Quantum.
Autor: QuantumWriter UID: Microsoft. Quantum. Concepts. qubit MS. Author: v-benbra MS. Date: 12/11/2017 MS. tópico: article no-loc:
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
# <a name="the-qubit"></a>O qubit

Assim como os bits são o objeto fundamental das informações na computação clássica, [*qubits*](https://en.wikipedia.org/wiki/Qubit) (bits Quantum) são o objeto fundamental das informações na computação Quantum.  Para entender essa correspondência, vamos examinar o exemplo mais simples: um único qubit.

## <a name="representing-a-qubit"></a>Representando um qubit

Embora um bit, ou dígito binário, possa ter valor $ 0 $ ou $ 1 $ , um qubit pode ter um valor que seja um destes ou uma superposição Quantum de $ 0 $ e $ 1 $ .

O estado de um único qubit pode ser descrito por um vetor de coluna bidimensional da norma de unidade, ou seja, a magnitude quadrada de suas entradas deve somar $ 1 $ . Esse vetor, chamado de vetor de estado Quantum, contém todas as informações necessárias para descrever o sistema Quantum qubit, assim como um único bit contém todas as informações necessárias para descrever o estado de uma variável binária.

Qualquer vetor de coluna bidimensional de números reais ou complexos com a norma $ 1 $ representa um possível estado de Quantum mantido por um qubit. Assim, $ \begin{bmatrix} \alpha \\\\ \beta \end{bmatrix} $ representa um estado qubit se $ \alpha $ e $ \beta $ são números complexos que satisfazem $ | \alpha | ^ 2 + | \beta | ^ 2 = 1 $ .   Alguns exemplos de vetores de estado de Quantum válidos que representam qubits incluem

$$\begin{bmatrix}1 \\\\ 0 \end{bmatrix} , \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} , \begin{bmatrix} \frac { 1 } { \sqrt { 2 } } \\\\ \frac { 1 } { \sqrt { 2 } } \end{bmatrix} , \begin{bmatrix} \frac { 1 } { \sqrt { 2 } } \\\\ \frac { -1 } { \sqrt { 2 } } \end{bmatrix} \text { e } \begin{bmatrix} \frac { 1 } { \sqrt { 2 } } \\\\ \frac { i } { \sqrt { 2 } } \end{bmatrix} .      $$

Os vetores de estado Quantum $ \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} $ e $ \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} $ usam uma função especial. Esses dois vetores formam uma base para o espaço vetorial que descreve o estado do qubit. Isso significa que qualquer vetor de estado de Quantum pode ser escrito como uma soma desses vetores de base. Especificamente, o vetor $ \begin{bmatrix} x \\\\ y \end{bmatrix} $ pode ser gravado como $ x \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} + y \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} $ . Embora qualquer rotação desses vetores sirva como uma base perfeitamente válida para o qubit, optamos por fazer um privilégio para esse, chamando-o na *base computacional*.

Pegamos esses dois Estados de Quantum para corresponder aos dois Estados de um bit clássico, a saber, $ 0 $ e $ 1 $ . A convenção padrão é escolher

$$0 \equiv \begin{bmatrix} 1 \\\\  0 \end{bmatrix} , \qquad 1 \equiv \begin{bmatrix} 0 \\\\  1 \end{bmatrix} ,$$

Embora a escolha oposta pudesse ser igualmente bem executada. Portanto, fora do número infinito de vetores de estado de Quantum de qubit único, apenas dois correspondem a Estados de bits clássicos; todos os outros Estados de Quantum não.

## <a name="measuring-a-qubit"></a>Medindo um qubit

Agora que sabemos como representar um qubit, podemos obter alguma intuição para o que esses Estados representam discutindo o conceito de [*medida*](https://en.wikipedia.org/wiki/Measurement_in_quantum_mechanics). Uma medida corresponde à ideia informal de "olhando" em um qubit, que recolhe imediatamente o estado do Quantum para um dos dois Estados clássicos $ \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} $ ou $ \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} $ . Quando um qubit fornecido pelo vetor de estado Quantum $ \begin{bmatrix} \alpha \\\\ \beta \end{bmatrix} $ é medido, obtemos o resultado $ 0 $ com a probabilidade $ | \alpha | ^ 2 $ e o resultado $ 1 com a $ probabilidade $ | \beta | ^ 2 $ .   No resultado $ 0 $ , o novo estado do qubit é $ \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} $ ; no resultado $ 1, $ seu estado é $ \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} $ . Observe que essas probabilidades somam até $ 1 $ devido à condição de normalização $ | \alpha | ^ 2 + | \beta | ^ 2 = 1 $ .

As propriedades de medida também significam que o sinal geral do vetor de estado do Quantum é irrelevante. Negar um vetor é equivalente a $ \alpha \right Arrow- \alpha $ e $ \beta \right Arrow- \beta $ . Como a probabilidade de medir $ 0 $ e $ 1 $ depende da magnitude quadrada dos termos, inserir tais sinais não altera as probabilidades. Essas fases costumam ser chamadas de [ `` *fases globais*' '](https://en.wikipedia.org/wiki/Phase_factor) e, mais geralmente, podem estar no formato $ e ^ { i \phi } $ em vez de apenas $ \pm 1 $ .

Uma propriedade final importante da medição é que ela não necessariamente danifica todos os vetores de estado da Quantum. Se começarmos com um qubit no estado $ \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} $ , que corresponde ao estado clássico $ 0 $ , medir esse estado sempre produzirá o resultado $ 0 $ e deixará o estado do Quantum inalterado. Nesse sentido, se tivermos apenas bits clássicos (ou seja, qubits que sejam $ \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} $ ou $ \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} $ ), a medição não danificará o sistema. Isso significa que podemos replicar dados clássicos e manipulá-los em um computador Quantum da mesma forma que um pode fazer em um computador clássico. No entanto, a capacidade de armazenar informações em ambos os Estados de uma vez é o que eleva a computação Quantum além do que é possível, de forma clássica, e mais Robs da capacidade de copiar dados Quantum indiscriminadamente, consulte também [o teorema no-Cloning](https://en.wikipedia.org/wiki/No-cloning_theorem).

## <a name="visualizing-qubits-and-transformations-using-the-bloch-sphere"></a>Visualizando qubits e transformações usando a esfera Bloch

Qubits também pode ser pictureed em $ 3 $ D usando a representação de [*esfera Bloch*](https://en.wikipedia.org/wiki/Bloch_sphere) .  A esfera Bloch fornece uma maneira de descrever um estado de Quantum de qubit único (que é um vetor complexo bidimensional) como um vetor de valor real tridimensional.  Isso é importante porque permite visualizar Estados de qubit único e, assim, desenvolver motivos que podem ser inestimávels na compreensão de Estados de qubit (onde infelizmente a representação de esfera de Bloch é interrompida).  A esfera Bloch pode ser visualizada da seguinte maneira:

<largura de!--- ![](.\media\bloch.svg) { = 50%} --->
![Esfera de Bloch](~/media/concepts_bloch.png)

As setas neste diagrama mostram a direção em que o vetor de estado do Quantum está apontando e cada transformação da seta pode ser considerada como uma rotação sobre um dos eixos cardinal.
Embora pensar em uma computação Quantum como uma sequência de rotações seja uma intuição poderosa, é desafiador usar essa intuição para projetar e descrever algoritmos. Q# alivia esse problema fornecendo uma linguagem para descrever essas rotações.

## <a name="single-qubit-operations"></a>Operações de Single-Qubit

Os computadores Quantum processam dados aplicando um conjunto universal de Gates de Quantum que podem emular qualquer rotação do vetor de estado Quantum.
Essa noção de universação é semelhante à noção de universalidade para computação tradicional (ou seja, clássica), em que um conjunto de portão é considerado universal se cada transformação dos bits de entrada puder ser executada usando um circuito de comprimento finito.
Na computação Quantum, as transformações válidas que temos permissão para executar em um qubit são transformações e medição de unitários.
A *operação de adjoin* ou a Transpose de conjugada complexa é de importância crucial para a computação Quantum porque é necessária para inverter as transformações Quantum.

Há apenas quatro funções que mapeiam um bit para um bit em um computador clássico. Por outro lado, há um número infinito de transformações de unitários em um único qubit em um computador Quantum. Portanto, nenhum conjunto finito de operações primitivas de Quantum, chamado [*Gates*](https://en.wikipedia.org/wiki/Quantum_logic_gate), pode replicar exatamente o conjunto infinito de transformações de unitários permitidas na computação Quantum. Isso significa que, diferentemente da computação clássica, é impossível para um computador Quantum implementar cada programa Quantum possível usando exatamente um número finito de Gates. Assim, os computadores Quantum não podem ser universais no mesmo sentido dos computadores clássicos. Como resultado, quando dizemos que um conjunto de Gates é *Universal* para computação Quantum, na verdade queremos dizer algo um pouco mais fraco do que queremos dizer com a computação clássica.
Para a universalidade, exigimos que um computador Quantum só se *aproxima* de cada matriz unitário dentro de um erro finito usando uma sequência de portão de comprimento finito.
Em outras palavras, um conjunto de Gates será um conjunto de portão universal se qualquer transformação unitário puder ser aproximadamente gravada como um produto de Gates desse conjunto. Exigimos que, para qualquer erro prescrito associado, exista Gates $ G_ { 1 } , G_ { 2 } , \ldots, G_N $ do conjunto de portas de modo que

$$
G_N G_ { N-1 } \cdots G_2 G_1 \approx U. $$

Observe que, como a Convenção para multiplicação de matriz é multiplicada da direita para a esquerda a primeira operação de portão nessa sequência, $ G_N $ , na verdade, é a última aplicada ao vetor de estado Quantum. Mais formalmente, dizemos que esse conjunto de portão é universal se para cada tolerância de erro $ \epsilon > 0 $ existe $ G_1, \ldots, G_N $ de modo que a distância entre $ G_N \ldots G_1 $ e $ U $ seja no máximo $ \epsilon $ . Idealmente, o valor de $ N $ necessário para alcançar essa distância de $ \epsilon $ deve dimensionar o logaritmicamente com $ 1/\ Épsilon $ .

Como funciona a aparência desse tipo de porta universal na prática?  O conjunto mais simples desse tipo de porta universal para Gates de qubit consiste em apenas dois Gates: The Hadamard Gate $ H $ e o chamado $ T $ -Gate (também conhecido como a $ porta \ PI/8 $ ):

$$
H = \frac { 1 } { \sqrt { 2 } } \begin{bmatrix} 1 & 1 \\\\ 1 & -1 \end{bmatrix} , \qquad T = \begin{bmatrix} 1 & 0 \\\\ 0 & e ^ { i \ pi/4 } \end{bmatrix} .
$$

No entanto, por motivos práticos relacionados à correção de erro Quantum, pode ser mais conveniente considerar um conjunto de portão maior, ou seja, um que pode ser gerado usando $ H $ e $ T $ . Podemos classificar os Gates da Quantum em duas categorias: Clifford Gates e o $ T $ -Gate.
Essa subdivisão é útil porque, em muitos esquemas de correção de erros Quantum, os chamados Clifford Gates são fáceis de implementar, ou seja, eles exigem muito poucos recursos em termos de operações e qubits para implementar a falha de forma tolerante, enquanto as Gates não Clifford são muito dispendiosas quando exigem tolerância a falhas. O conjunto padrão de Gates de Clifford de qubit único, [incluído por padrão Q# no ](xref:microsoft.quantum.libraries.standard.prelude), inclui

$$
H = \frac { 1 } { \sqrt { 2 } } \begin{bmatrix} 1 & 1 \\\\ 1 & -1 \end{bmatrix} , \qquad S = \begin{bmatrix} 1 & 0 \\\\ 0 & i \end{bmatrix} = T ^ 2, \qquad X = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} = HT ^ 4h,$$

$$
Y = \begin{bmatrix} 0 & -i \\\\ i & 0 \end{bmatrix} = t ^ 2HT ^ 4 HT ^ 6, \qquad Z = \begin{bmatrix} 1 & 0 \\\\ 0 & -1 \end{bmatrix} = T ^ 4.
$$

Aqui, as operações $ X $ , $ Y $ e $ Z $ são usadas especialmente frequentemente e são nomeadas como [*operadores Pauli*](https://en.wikipedia.org/wiki/Pauli_matrices) depois de seu criador Wolfgang Pauli.
Junto com o portão não Clifford (o $ T $ -Gate), essas operações podem ser compostas para aproximar qualquer transformação unitário em um único qubit.

Para obter mais informações sobre essas operações, suas representações e implementações de esfera do Bloch Q# , consulte [operações e funções intrínsecas](xref:microsoft.quantum.libraries.standard.prelude#intrinsic-operations-and-functions).

Como um exemplo de como as transformações de unitários podem ser criadas com base nesses primitivos, as três transformações modeladas nos Blochs acima correspondem à sequência de portão $ \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} \mapsto HZH \begin{bmatrix} 1 \\\\ 0,0 \end{bmatrix} = \begin{bmatrix} \\\\ 1 \end{bmatrix} $ .

Embora o anterior constitua os Gates primitivos mais populares para descrever as operações no nível lógico da pilha (Pense no nível lógico como o nível do algoritmo Quantum), geralmente é conveniente considerar menos operações básicas no nível de algoritmo, por exemplo, operações mais próximas de um nível de descrição de função. Felizmente, Q# também tem métodos disponíveis para a implementação de unidades de nível superior, que, por sua vez, permitem que algoritmos de alto nível sejam implementados sem decompor explicitamente tudo em Clifford e $ T $ -Gates.

O mais simples desses primitivos é a única rotação de qubit. Três rotações de qubit simples são normalmente consideradas: $ R_x $ , $ R_y $ e $ R_z $ . Para visualizar a ação do R_x de rotação $ (\theta) $ , por exemplo, imagine apontar o polegar direito ao longo da direção do $ $ eixo x da esfera Bloch e girar o vetor com sua mão por meio de um ângulo de $ \ teta/2 $ radianos. Esse fator confuso de $ 2 $ surge desde o fato de que os vetores ortogonal são $ 180 ^ \circs $ quando plotados na esfera de Bloch, mas são, na verdade, $ 90 ^ \circ $ graus geométricos. As matrizes de unitário correspondentes são:

\begin{align *} 
 & R_z (\theta) = e ^ { -i\theta z/2 } = \begin{bmatrix} e ^ { -i \ teta/2 } & 0 \\\\ 0 & e ^ { i \ teta/2 } \end{bmatrix} , \\\\ 
 & R_x (\theta) = e ^ { -i\theta x/2 } = HR_z (\theta) H = \begin{bmatrix} \cos (\ teta/2) & -i\sin (\ teta/2) \\\\ -i\sin (\ teta/2) & \cos (\ teta/2) \end{bmatrix} , \\\\ 
 & R_y (\theta) = e ^ { -i\theta y/2 } = SHR_z (\theta) HS ^ \dagger = \begin{bmatrix} \cos (\ teta/2) & -\sin (\ teta/2) \\\\ \sin (\ teta/2) & \cos (\ teta/2) \end{bmatrix} . \end { alinhar*}

Assim como as três rotações podem ser combinadas para executar uma rotação arbitrária em três dimensões, ela pode ser vista na representação de Sphere Bloch que qualquer matriz de unitário também pode ser gravada como uma sequência de três rotações. Especificamente, para cada matriz unitário $ u $ , existe,,, $ \alpha \beta \gamma \delta $ como $ U = e ^ { i \alpha } R_x ( \beta ) R_z () \gamma R_x \delta $ (). Portanto $ R_z (\theta) $ e $ H $ também formam um conjunto de portão universal, embora não seja um conjunto discreto, porque $ \theta $ pode usar qualquer valor. Por esse motivo, e devido a aplicativos na simulação do Quantum, esses Gates contínuos são cruciais para computação Quantum, especialmente no nível de design do algoritmo Quantum. Para obter a implementação de hardware tolerante a falhas, elas serão eventualmente compiladas em sequências de porta discretas que aproximam-se dessas rotações.
