---
Título: Descrição da Quantum Oracle: saiba como trabalhar com e definir Oracle Quantum, operações de caixa preta que são usadas como entrada para outro algoritmo.
Autor: cgranade UID: Microsoft. Quantum. Concepts. oraclees MS. Author: Christopher.Granade@microsoft.com MS. Data: 07/11/2018 MS. Topic: artigo no-loc:
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
# <a name="quantum-oracles"></a>Oracle Quantum

Um Oracle $ O $ é uma operação de "caixa preta" que é usada como entrada para outro algoritmo.
Muitas vezes, essas operações são definidas usando uma função clássica $ f: \\ { 0, 1 \\ } ^ n \to \\ { 0, 1 \\ } ^ m $ que usa $ uma $ entrada binária de n bits e produz $ uma $ saída binária de bit m.
Para fazer isso, considere uma entrada binária específica $ x = (x_ { 0 } , x_ { 1 } , \dots, x_ { n-1 } ) $ .
Podemos rotular Estados qubit como $ \ket { \vec { x } } = \ket { x_ { 0 } } \otimes \ket { x_ { 1 } } \otimes \cdots \otimes \ket { x_ { n-1 } } $ .

Nós podemos primeiro tentar definir $ o $ para que $ o \ket { x } = \ket { f (x) } $ , mas isso tenha alguns problemas.
Em primeiro lugar, $ f $ pode ter um tamanho diferente de entrada e saída ( $ n \ne m $ ), de modo que aplicar $ $ o seria alterar o número de qubits no registro.
Em segundo lugar, mesmo se $ n = m $ , a função pode não ser invertível: se $ f (x) = f (y) $ para alguns $ x \ne y $ , em seguida, $ o \ket { x } = o \ket { y, } $ mas $ o ^ \dagger o \ket { x } \ne o ^ \dagger o \ket { y } $ .
Isso significa que não será possível construir a operação de addefinição o $ ^ \dagger $ e os Oracle precisarão ter um adjacente definido para eles.

## <a name="defining-an-oracle-by-its-effect-on-computational-basis-states"></a>Definindo um Oracle por seu efeito nos Estados de base computacional
Podemos lidar com esses dois problemas introduzindo um segundo registro de $ m $ qubits para manter nossa resposta.
Em seguida, vamos definir o efeito do Oracle em todos os Estados de base computacional: para todos os $ x \in \\ { 0, 1 \\ } ^ n $ e $ y \in \\ { 0, 1 \\ } ^ m $ ,

$$
\begin{align}
    O ( \ket { x } \otimes \ket { y } ) = \ket { x } \otimes \ket { y \oplus f (x) } .
\end{align}
$$

Agora $ o = ^ \dagger $ por construção, portanto, resolvemos os dois problemas anteriores.

> [!TIP]
>Para ver que $ o o = ^ { \dagger } $ , observe que o $ ^ 2, = \boldone $ desde $ um \oplus b \oplus = b $ para todos $ , b \in \[ ! Parar. Não-LOC ({)] 0, 1 \[ ! Parar. Não-LOC (})] $ .
>Como resultado, $ O \ket { x } \ket { y \oplus f (x) } = \ket { x } \ket { y \oplus f (x) \oplus f (x) } = \ket { x } \ket { y } $ .

De forma importante, definir um Oracle dessa maneira para cada Estado de base computacional $ \ket { x } \ket { y } $ também define como $ O O $ age para qualquer outro Estado.
Isso é seguido imediatamente do fato de que $ O $ , como todas as operações de Quantum, é linear no estado em que ele atua.
Considere a operação Hadamard, por exemplo, que é definida por $ h \ket { 0 } = \ket { + } $ e $ h \ket { 1 } = \ket { - } $ .
Se quisermos saber como $ h $ atua $ \ket { + } $ , podemos usar que $ h $ seja linear,

$$
\begin{align}
H \ket { + } & = \frac { 1 } { \sqrt { 2 } } h ( \ket { 0 }  +  \ket { 1 } ) = \frac { 1 } { \sqrt { 2 } } (h \ket { 0 } + h \ket { 1 } )\\\\
           &= \frac{ 1 } { \sqrt { 2 } } ( \ket { + }  +  \ket { - } ) = \frac 12 ( \ket { 0 }  +  \ket { 1 }  +  \ket { 0 }  -  \ket { 1 } ) = \ket { 0 } .
\end{align}
$$

No caso de definir nosso Oracle $ O $ , podemos usar de forma semelhante que qualquer estado $ \ket { \psi } $ em $ n + m $ qubits pode ser escrito como

$$
\begin{align}
\ket{\psi}& = \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y}
\end{align}
$$

em que $ \alpha : \\ { 0, 1 \\ } ^ n \times \\ { 0, 1 \\ } ^ m \to \mathbb { C } $ representa os coeficientes do estado $ \ket { \psi } $ . Assim,

$$
\begin{align}
O \ket { \psi } & = \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y } x \\\\ 0 & , = 1 ^ n, y 0, 1 ^ m (x, y) O \sum _ { \in \\ { \\ } \in \\ { \\ } } \alpha \ket { x } \ket { y }\\\\
             &= \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y \oplus f (x) } .
\end{align}
$$

## <a name="phase-oracles"></a>Fase Oracle
Como alternativa, podemos codificar $ f $ em um Oracle $ O $ aplicando uma _fase_ com base na entrada para $ o $ . Por exemplo, poderemos definir $ O $ como$$
\begin{align}
    O \ket { x } = (-1) ^ { f (x) } \ket { x } .
\end{align}
$$
Se uma fase da Oracle age em um registro inicialmente em um estado de base computacional $ \ket { x } $ , essa fase é uma fase global e, portanto, não observável.
Mas tal Oracle pode ser um recurso muito potente se aplicado a uma superposição ou como uma operação controlada.
Por exemplo, considere uma fase de $ O_f $ da Oracle para uma função f de qubit única $ $ .
Clique$$
\begin{align}
    O_f\ket{+}
        &=O_f ( \ket { 0 }  +  \ket { 1 } )/ \sqrt { 2 }\\\\
        &=((-1) ^ { f (0) } \ket { 0 } + (-1) ^ { f (1) } \ket { 1 } )/ \sqrt { 2 }\\\\
        &=(-1) ^ { f (0) } ( \ket { 0 } + (-1) ^ { f (1)-f (0) } \ket { 1 } )/ \sqrt { 2 }\\\\
        &=(-1) ^ { f (0) } Z ^ { f (0)-f (1) } \ket { + } .
\end{align}
$$

Em geral, as duas exibições de Oracle podem ser ampliadas para representar funções clássicas que retornam números reais em vez de apenas um único bit.

Escolher a melhor maneira de implementar um Oracle depende muito da forma como esse Oracle será usado dentro de um determinado algoritmo.
Por exemplo, o [algoritmo Deutsch-Jozsa](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) depende do Oracle implementado na primeira forma, enquanto o [algoritmo de Grover](https://en.wikipedia.org/wiki/Grover's_algorithm) se baseia no Oracle implementado da segunda maneira.


Para obter mais detalhes, sugerimos a discussão em [Gilyén *et al*. 1711, 465](https://arxiv.org/abs/1711.00465).
