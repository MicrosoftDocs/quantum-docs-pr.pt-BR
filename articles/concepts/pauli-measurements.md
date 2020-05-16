---
title: Medições de Pauli
description: Saiba como trabalhar com operações de medição de Pauli de qubit única e múltipla.
author: QuantumWriter
uid: microsoft.quantum.concepts.pauli
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 3ce9c0ea13d62bd662f3ccc450c385799ddb264b
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426562"
---
# <a name="pauli-measurements"></a>Medições de Pauli

Nas discussões anteriores, concentramos-se em medidas de base computacional.
Na verdade, há outras medidas comuns que ocorrem na computação Quantum que, de uma perspectiva de notação, são convenientes para expressar em termos de medidas de base computacional.
À medida que você trabalha com o Q #, o tipo mais comum de medidas que você encontrará provavelmente será *Pauli medições*, que generalizam as medidas de base computacional para incluir medidas em outras bases e de paridade entre diferentes qubits.
Nesses casos, é comum discutir a medição de um operador Pauli, em geral, um operador como $X, Y, Z $ ou $Z \otimes Z, X\otimes X, X\otimes Y $ e assim por diante.

> [!TIP]
> Em Q #, os operadores qubit Pauli geralmente são representados por matrizes do tipo `Pauli[]` .
> Por exemplo, para representar $X \otimes Z \otimes Y $, você pode usar a matriz `[PauliX, PauliZ, PauliY]` .

Discutir a medição em termos de operadores Pauli é especialmente comum no subcampo de correção de erro Quantum.
Em Q #, seguimos uma convenção semelhante; Agora, explicamos essa exibição alternativa de medidas.

Antes de se aprofundar nos detalhes de como pensar em uma medida Pauli, é útil pensar em que a medição de um único qubit dentro de um computador Quantum faz o estado Quantum.
Imagine que tenhamos um estado de Quantum $n $-qubit; Depois, a medição de um qubit regra imediatamente a metade das possibilidades de $2 ^ n $ em que o estado pode estar.
Em outras palavras, a medida projeta o estado da Quantum em um dos dois espaços.
Podemos generalizar a maneira como pensamos na medição para refletir essa intuição.

Para identificar esses subespaços de forma concisa, precisamos de uma linguagem para descreve-los.
Uma maneira de descrever os dois subespaços é especificando-os por meio de uma matriz que tem apenas duas eigenvalues exclusivas, tomadas pela Convenção para ser $ \pm $1.
Para obter um exemplo simples de descrição de subespaços dessa forma, considere $Z $:

$ $ \begin{align} Z & = \begin{bmatrix} 1 & 0 \\ \\ 0 &-1 \end{bmatrix}.
\end{align} $ $

Lendo os elementos diagonais da matriz Pauli-$Z $, podemos ver que $Z $ tem dois eigenvectors, $ \ket {0} $ e $ \ket {1} $, com eigenvalues $ \pm $1 correspondente.
Portanto, se medirmos o qubit e obtivermos `Zero` (correspondente ao estado $ \ket {0} $), sabemos que o estado de nosso qubit é um eigenstate de $ + $1 do operador $Z $.
Da mesma forma, se obtivermos `One` , sabemos que o estado de nosso qubit é um eigenstate $-$1 de $Z $.
Esse processo é mencionado na linguagem de medidas Pauli como "medindo Pauli $Z $" e é totalmente equivalente a executar uma medição de base computacional.

Qualquer matriz de $2 \ vezes $2 que seja uma transformação unitário de $Z $ também satisfaça a esses critérios.
Ou seja, também poderíamos usar uma matriz $A = U ^ \dagger Z U $, em que $U $ é qualquer outra matriz de unitário, para fornecer uma matriz que define os dois resultados de uma medição em seu $ \pm $1 eigenvectors.
A notação das medições de Pauli faz referência a essa equivalência unitário identificando as medidas $X, Y, Z $ como medidas equivalentes que um pode fazer para obter informações de um qubit.
Essas medidas são fornecidas abaixo para sua conveniência.


|Medição de Pauli  |Transformação unitário  |
|-------------------|------------------------|
| $Z $               | US $ \boldone $             |
| $X $               | $H $                    |
| $Y $               | $HS ^ {\dagger} $         |

Ou seja, usar essa linguagem, "Measure $Y $" é equivalente a aplicar $HS ^ \dagger $ e, em seguida, medir na base computacional, em que [`S`](xref:microsoft.quantum.intrinsic.s) é uma operação de Quantum intrínseca às vezes chamada de "portão de fase" e pode ser simulada pela matriz unitário

$ $ \begin{align} S = \begin{bmatrix} 1 & 0 \\ \\ 0 & \end{bmatrix}.
\end{align} $ $

Também é equivalente a aplicar $HS ^ \dagger $ ao vetor de estado Quantum e, em seguida, medir $Z $, de modo que a seguinte operação seja equivalente a `Measure([PauliY], [q])` :

```Q#
operation MeasureY(qubit : Qubit) : Result {
    mutable result = Zero;
    within {
        H(q);
        Adjoint S(q);
    } apply {
        set result = M(q);
    }
    return result;
}
```

Em seguida, o estado correto seria encontrado transformando-o de volta para a base computacional, que resulta na aplicação de $SH $ ao vetor de estado Quantum; no trecho acima, a transformação de volta para a base computacional é manipulada automaticamente pelo uso do `within … apply` bloco.

Em Q #, dizemos que o resultado---ou seja, as informações clássicas extraídas da interação com o estado---são dadas por um `Result` valor $j na \\ {\Texttt{zero}, \texttt{One} \\ } $ indicando se o resultado está na eigenspace de $ (-1) ^ j $ do operador Pauli medido.


## <a name="multiple-qubit-measurements"></a>Medições de várias qubit

As medições de operadores qubit Pauli são definidas da mesma forma, como visto em:

$ $ Z\otimes Z = \begin{bmatrix}1 &0 &0&0 \\ \\ 0&-1&0&0 \\ \\ 0&0&-1&0 \\ \\ 0&0&0&1 \ fim {bmatrix}.
$$

Assim, os produtos tensor de dois operadores Pauli $ $Z $ formam uma matriz composta de dois espaços consistindo em US $ + $1 e $-$1 eigenvalues.
Assim como no caso de qubit único, ambos constituem um meio-espaço que significa que metade do espaço de vetor acessível pertence ao eigenspace $ + $1 e à metade restante para o $-$1 eigenspace.
Em geral, é fácil ver a definição do produto tensor de que qualquer produto tensor de operadores Pauli $ $Z $ e a identidade também obedece a isso.
Por exemplo,

$ $ \begin{align} Z \otimes \boldone = \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 &-1 & 0 \\ \\ 0 & 0 & 0 &-1 \end{bmatrix}.
\end{align} $ $

Como antes, qualquer transformação unitário dessas matrizes também descreve dois semestres rotulados por $ \pm $1 eigenvalues.
Por exemplo, $X \otimes X = H\otimes H (Z\otimes Z) H\otimes H $ da identidade que $Z = HXH $.
Semelhante ao caso qubit, todas as medidas de Pauli de duas qubit podem ser escritas como $U ^ \dagger (Z\otimes \id) U $ para $4 \ vezes $4 matrizes unitários $U $. Enumeramos as transformações na tabela a seguir.

> [!NOTE]
> Na tabela a seguir, usamos $ \operatorname{SWAP} $ para indicar a matriz $ $ \begin{align} \operatorname{SWAP} & = \left (\begin{Matrix} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \end{Matrix}\right) \end{align} $ $ usado para simular a operação intrínseca [`SWAP`](xref:microsoft.quantum.intrinsic) .

|Medição de Pauli     |Transformação unitário  |
|----------------------|------------------------|
| $Z \otimes \boldone $ | US $ \boldone \otimes \boldone $ |
| $Z \otimes \boldone $ | US $ \boldone\otimes \boldone $ |
| $X \otimes \boldone $ | $H \otimes \boldone $ |
| $Y \otimes \boldone $ | $HS ^ \dagger\otimes \boldone $ |
| US $ \boldone \otimes Z $ | US $ \operatorname{SWAP} $ |
| US $ \boldone \otimes X $ | $ (H\otimes \boldone) \operatorname{SWAP} $ |
| US $ \boldone \otimes Y $ | $ (HS ^ \dagger\otimes \boldone) \operatorname{SWAP} $ |
| $Z \otimes Z $ | US $ \operatorname{CNOT} \_ {10} $ |
| $X \otimes Z $ | $ \operatorname{CNOT} \_ {10} (H\otimes \boldone) $ |
| $Y \otimes Z $ | $ \operatorname{CNOT} \_ {10} (HS ^ \dagger\otimes \boldone) $ |
| $Z \otimes X $ | $ \operatorname{CNOT} \_ {10} (\boldone\otimes H) $ |
| $X \otimes X $ | $ \operatorname{CNOT} \_ {10} (H\otimes H) $ |
| $Y \otimes X $ | $ \operatorname{CNOT} \_ {10} (HS ^ \dagger\otimes H) $ |
| $Z \otimes Y $ | $ \operatorname{CNOT} \_ {10} (\BOLDONE \otimes HS ^ \dagger) $ |
| $X \otimes Y $ | $ \operatorname{CNOT} \_ {10} (H\otimes HS ^ \dagger) $ |
| $Y \otimes Y $ | $ \operatorname{CNOT} \_ {10} (HS ^ \dagger\otimes HS ^ \dagger) $ |

Aqui, a [`CNOT`](xref:microsoft.quantum.intrinsic.cnot) operação é exibida pelo seguinte motivo.
Cada medida de Pauli que não inclui a matriz $ \boldone $ é equivalente a um unitário para $Z \otimes Z $ pelo raciocínio acima.
O eigenvalues de $Z \otimes Z $ só depende da paridade da qubits que compõe cada vetor de base computacional, e as operações controladas não servem para calcular essa paridade e armazená-las no primeiro bit.
Depois que o primeiro bit é medido, podemos recuperar a identidade do espaço resultante, que é equivalente a medir o operador Pauli.

Uma observação adicional: embora possa ser tentador pressupor que medir $Z \otimes Z $ é o mesmo que medir sequencialmente $Z \otimes \mathbb {1} $ e $ \mathbb {1} \otimes Z $, essa suposição seria falsa.
O motivo é que medir $Z \otimes Z $ projeta o estado da Quantum no eigenstate de $ + $1 ou $-$1 desses operadores.
Medindo $Z \otimes \mathbb {1} $ e $ \mathbb {1} \otimes Z $ projeta o vetor de estado Quantum primeiro em um semestre de $Z \otimes \mathbb {1} $ e, em seguida, em um semestre de $ \mathbb {1} \otimes Z $.
Como há quatro vetores de base computacional, a execução de ambas as medidas reduz o estado para um quarto de espaço e, portanto, reduz-a para um único vetor de computação.

## <a name="correlations-between-qubits"></a>Correlações entre qubits
Outra maneira de observar a medição de produtos tensor de matrizes Pauli como $X \otimes X $ ou $Z \otimes Z $ é que essas medições permitem que você examine as informações armazenadas nas correlações entre os dois qubits.
Medir $X \otimes \id $ permite que você examine as informações armazenadas localmente no primeiro qubit.
Embora os dois tipos de medidas sejam igualmente valiosos na computação Quantum, o primeiro ilumina o poder da computação Quantum.
Ele revela que, na computação Quantum, geralmente as informações que você deseja aprender não são armazenadas em nenhum único qubit, mas armazenadas não localmente em todas as qubits de uma vez e, portanto, apenas examinando-as por meio de uma medida conjunta (por exemplo, $Z \otimes Z $), essas informações se tornam manifesto.

Por exemplo, na correção de erros, muitas vezes desejamos saber qual erro ocorreu ao aprender nada sobre o estado que estamos tentando proteger.
O [exemplo de código de inversão de bits](https://github.com/microsoft/Quantum/tree/master/samples/error-correction/bit-flip-code) mostra um exemplo de como você pode fazer isso usando medidas como $Z \otimes Z \otimes \id $ e $ \Id \otimes Z \otimes z $.
<!-- TODO: change this to a link to the samples browser as soon as the bit-flip code sample is on-boarded. -->

Operadores Pauli arbitrários, como $X \otimes Y \otimes Z \otimes \boldone $, também podem ser medidos.
Todos esses produtos tensor de Pauli Operators têm apenas duas eigenvalues $ \pm $1 e ambas as eigenspaces constituem metade de espaços de todo o espaço de vetor.
Portanto, eles coincidem com os requisitos declarados acima.

Em Q #, essas medidas retornam $j $ se a medida produz um resultado no eigenspace de sinal $ (-1) ^ j $.
Ter medidas Pauli como um recurso interno em Q # é útil porque a medição desses operadores requer cadeias longas de Gates e transformações de base controladas para descrever a diagonal $U $ Gate necessário para expressar a operação como um produto tensor de $Z $ e $ \id $.
Ao ser capaz de especificar que você deseja realizar uma dessas medidas predefinidas, você não precisa se preocupar em como transformar sua base de forma que uma medida de base computacional forneça as informações necessárias.
O Q # trata todas as transformações de base necessárias para você automaticamente.
Para obter mais informações, consulte [`Measure`](xref:microsoft.quantum.intrinsic.measure) as [`MeasurePaulis`](xref:microsoft.quantum.measurement.measurepaulis) operações e.

## <a name="the-no-cloning-theorem"></a>O teorema no-Cloning

As informações da Quantum são poderosas.
Ele nos permite fazer coisas incríveis, como números de fator exponencialmente mais rápidos do que os melhores algoritmos clássicos conhecidos, ou simular com eficiência sistemas de informações de alta correlação que exigem, de modo clássico, o custo exponencial para simular com precisão.
No entanto, há limitações no poder da computação Quantum.
Uma dessas limitações é fornecida pelo *teorema no-Cloning*.

O teorema no-Cloning é adequadamente nomeado.
Ele não permite a clonagem de Estados de Quantum genérico por um computador Quantum.
A prova do teorema é bastante simples.
Embora uma prova completa do teorema sem clonagem seja um pouco técnica para nossa discussão aqui, a prova no caso de nenhum qubits auxiliar adicional está dentro de nosso escopo (auxiliares qubits são qubits usados para espaço transitório durante uma computação e são facilmente usados e gerenciados em Q #, consulte [qubits emprestados](xref:microsoft.quantum.guide.qubits#borrowed-qubits)).

Para esse computador Quantum, a operação de clonagem deve ser descrita por uma matriz unitário.
Não permitimos a medição, já que corromperia o estado Quantum que estamos tentando clonar.
Para simular a operação de clonagem, queremos que a matriz unitário usada tenha a propriedade que $ $ U \ket{\psi} \ket {0} = \ket{\psi} \ket{\psi} $ $ para qualquer estado $ \ket{\psi} $.
Em seguida, a propriedade linear da multiplicação de matriz implica que, para qualquer segundo estado Quantum $ \ket{\phi} $,

$ $ \begin{align} U \left [\frac {1} {\sqrt {2} } \left (\ket{\phi} + \ket{\psi} \right) \right] \ket {0} & = \frac {1} {\sqrt {2} } U\ket {\ Phi} \ ket {0} + \frac {1} {\sqrt {2} } U\ket {\ psi} \ ket {0} \\ \\ & = \frac {1} {\sqrt {2} } \left (\ket{\phi} \ket{\phi} + \ket{\psi} \ket{\psi} \right) \\ \\ & \ne \left (\frac {1} {\sqrt {2} } \left (\ket{\phi} + \ket{\psi} \right) \right) \otimes \left (\frac {1} {\sqrt {2} } \left (\ket{\phi} + \ket{\psi} \right) \right).
\end{align} $ $

Isso fornece a intuição fundamental por trás do teorema sem clonagem: qualquer dispositivo que copia um estado de Quantum desconhecido deve induzir erros em pelo menos alguns dos Estados que ele copia.
Embora a principal suposição de que o Cloner atue linearmente no estado de entrada possa ser violada por meio da adição e da medição do qubits auxiliar, essas interações também vazam informações sobre o sistema por meio de estatísticas de medição e impedem a clonagem exata nesses casos.
Para obter uma prova mais completa dos teorema sem clonagem, consulte [para obter mais informações](xref:microsoft.quantum.more-information).

O teorema no-Cloning é importante para uma compreensão qualitativa da computação Quantum porque, se você puder clonar os Estados da Quantum de forma incara, terá uma capacidade quase mágico de aprender com os Estados da Quantum.
Na verdade, você poderia violar o princípio de incerteza de vaunted da Heisenberg.
Como alternativa, você pode usar um Cloner ideal para pegar um único exemplo de uma distribuição de Quantum complexa e aprender tudo o que poderia ser possível saber sobre essa distribuição de apenas uma amostra.
Isso seria como você invertendo uma moeda e observando a cabeça e, depois, ao informar a um amigo sobre o resultado que eles respondem "Ah, a distribuição dessa moeda deve ser Bernoulli com $p = 0.512643 \ ldots $!"  Essa instrução seria não sensical porque um pouco de informação (o resultado dos cabeçotes) simplesmente não pode fornecer muitas informações necessárias para codificar a distribuição sem informações substanciais anteriores.
Da mesma forma, sem informações anteriores, não podemos clonar perfeitamente um estado Quantum da mesma forma que não podemos preparar uma Ensemble dessas moedas sem saber $p $.

As informações não são gratuitas na computação Quantum.
Cada qubit medido fornece uma única informação, e o teorema no-Cloning mostra que não há nenhum backdoor que possa ser explorado para contornar a compensação fundamental entre as informações obtidas sobre o sistema e o distúrbios invocado sobre ele.
