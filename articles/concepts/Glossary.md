---
title: Glossário da computação Quantum
description: Um glossário de termos, ações e objetos comuns usados na computação Quantum.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.glossary
ms.openlocfilehash: cbc473eb14d8afd255a7072475dc054e18b98e3e
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426697"
---
# <a name="quantum-computing-glossary"></a>Glossário da computação Quantum

## <a name="adjoint"></a>Adjacente

A transpoção conjugada complexa de uma [operação](xref:microsoft.quantum.glossary#operation). Para operações que implementam um operador [unitário](xref:microsoft.quantum.glossary#unitary-operator) , o adjacente é o inverso da operação e é indicado por um símbolo de Dagger. Por exemplo, se a operação `U` representa o operador unitário $U $, `Adjoint U` representa $U ^ \dagger $. Para obter mais informações, consulte [Adjoinout](xref:microsoft.quantum.guide.operationsfunctions#controlled-and-adjoint-operations).

## <a name="ancilla"></a>Ancilla

Um [qubit](xref:microsoft.quantum.glossary#qubit) que serve como memória temporária para um computador Quantum e é alocado e desalocado conforme necessário.  Para obter mais informações, consulte [Multiple qubits](xref:microsoft.quantum.concepts.multiple-qubits).

## <a name="bell-state"></a>Estado de sino

Um dos quatro [Estados](xref:microsoft.quantum.glossary#quantum-state) de Quantum [confusas](xref:microsoft.quantum.glossary#entanglement) de dois qubits específicos. Os quatro Estados são definidos $ \ket{\ beta_ {IJ}} = (\mathbb{I} \otimes X ^ iZ ^ j) (\ket {00} + \ket {11} )/\sqrt {2} $. Um estado de sino também é conhecido como um [par EPR](xref:microsoft.quantum.glossary#epr-pair).

## <a name="bloch-sphere"></a>Esfera de Bloch

Uma representação gráfica de um estado de[qubit](xref:microsoft.quantum.glossary#qubit) [Quantum](xref:microsoft.quantum.glossary#quantum-state) de qubit único como um ponto em uma esfera de unidade tridimensional. Para obter mais informações, consulte [visualizando qubits e transformações usando a esfera Bloch](xref:microsoft.quantum.concepts.qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere).

## <a name="callable"></a>Acessível

Uma [operação](xref:microsoft.quantum.glossary#operation) ou [função](xref:microsoft.quantum.glossary#function) na linguagem Q #. Para obter mais informações, consulte [operações e funções](xref:microsoft.quantum.guide.operationsfunctions).

## <a name="clifford-group"></a>Grupo de Clifford

O conjunto de operações que ocupam o octants da [esfera Bloch](xref:microsoft.quantum.glossary#bloch-sphere) e afetam as permutações dos [operadores Pauli](xref:microsoft.quantum.glossary#pauli-operators). Isso inclui as operações [$X $](xref:microsoft.quantum.intrinsic.x), [$Y $](xref:microsoft.quantum.intrinsic.y), [$Z $](xref:microsoft.quantum.intrinsic.z), [$H $](xref:microsoft.quantum.intrinsic.h) e [$S $](xref:microsoft.quantum.intrinsic.s).

## <a name="controlled"></a>Controlado

Uma [operação](xref:microsoft.quantum.glossary#operation) Quantum que usa um ou mais [qubits](xref:microsoft.quantum.glossary#qubit) como habilitadores para a operação de destino. Para obter mais informações, consulte [operações controladas e adjacentes](xref:microsoft.quantum.guide.operationsfunctions#controlled-and-adjoint-operations).

## <a name="dirac-notation"></a>Notação de Dirac

Uma abreviação simbólica que simplifica a representação de [Estados Quantum](xref:microsoft.quantum.glossary#quantum-state), também chamada de notação de *bra ket* .  A porção *Bra* representa um vetor de linha, por exemplo, $ \bra{A} = \begin{bmatrix} a {_1} & uma {_2} \end{bmatrix} $ e a porção *ket* representa um vetor de coluna, $ \ket{B} = \begin{bmatrix} B {_1} \\ \\ B {_2} \end{bmatrix} $. Para obter mais informações, consulte [notação de Dirac](xref:microsoft.quantum.concepts.dirac).

## <a name="eigenvalue"></a>Eigenvalue

O fator pelo qual a magnitude de uma [eigenvector](xref:microsoft.quantum.glossary#eigenvector) de uma determinada transformação é alterada pelo aplicativo da transformação.  Dada uma matriz quadrada $M $ e um eigenvector $v $, então $Mv = CV $, em que $c $ é o eigenvalue e pode ser um número complexo de qualquer argumento. Para obter mais informações, consulte [conceitos de matriz avançada](xref:microsoft.quantum.concepts.matrix-advanced).

## <a name="eigenvector"></a>Eigenvector

Um vetor cuja direção é inalterada por uma determinada transformação e cuja magnitude é alterada por um fator correspondente ao [eigenvalue](xref:microsoft.quantum.glossary#eigenvalue)do vetor. Dada uma matriz quadrada $M $ e um eigenvalue $c $, então $Mv = CV $, em que $v $ é um eigenvector da matriz e pode ser um número complexo de qualquer argumento. Para obter mais informações, consulte [conceitos de matriz avançada](xref:microsoft.quantum.concepts.matrix-advanced).

## <a name="entanglement"></a>Entanglement

As partículas de Quantum, como [qubits](xref:microsoft.quantum.glossary#qubit), podem ser conectadas ou *confusas* de modo que não possam ser descritas independentemente uma da outra. Seus resultados de medição são correlacionados mesmo quando estão separados infinitamente longe. Entanglement é essencial para [medir](xref:microsoft.quantum.glossary#measurement) o [estado](xref:microsoft.quantum.glossary#quantum-state) de um qubit.  Para obter mais informações, consulte [conceitos de matriz avançada](xref:microsoft.quantum.concepts.matrix-advanced).

## <a name="epr-pair"></a>Par de EPR

Um dos quatro [Estados de Quantum](xref:microsoft.quantum.glossary#quantum-state) confusas de dois [qubits](xref:microsoft.quantum.glossary#qubit)específicos. Os quatro Estados são definidos $ \ket{\ beta_ {IJ}} = (\mathbb {1} \Otimes X ^ Iz ^ j) (\ket {00} + \ket {11} )/\sqrt {2} $. Um par EPR também é conhecido como um [estado de sino](xref:microsoft.quantum.glossary#bell-state)

## <a name="evolution"></a>Evolucionário

Como um [estado Quantum](xref:microsoft.quantum.glossary#quantum-state) muda ao longo do tempo. Para obter mais informações, consulte [exponencials de matriz](xref:microsoft.quantum.concepts.matrix-advanced#matrix-exponentials).

## <a name="function"></a>Função
Um tipo de sub-rotina na linguagem Q # que é puramente clássico (não Quantum). Embora as funções sejam usadas em algoritmos Quantum, elas não podem agir em [operações](xref:microsoft.quantum.glossary#operation) [qubits](xref:microsoft.quantum.glossary#qubit) ou Call. Para obter mais informações, consulte [operações e funções](xref:microsoft.quantum.guide.operationsfunctions).

## <a name="gate"></a>Check

Um termo herdado para uma [operação](xref:microsoft.quantum.glossary#operation)Quantum, com base no conceito de Gates de lógica clássica. Um [circuito Quantum](xref:microsoft.quantum.glossary#quantum-circuit-diagram) é uma rede de Gates (ou operações), com base no conceito semelhante de circuitos lógicos clássicos.

## <a name="global-phase"></a>Fase global

Quando dois [Estados](xref:microsoft.quantum.glossary#quantum-state) são idênticos até um múltiplo de um número complexo $e ^ {i\phi} $, eles são considerados diferentes para uma fase global. Ao [contrário das fases locais, as fases](xref:microsoft.quantum.glossary#measurement)globais não podem ser observadas por qualquer medida. Para obter mais informações, consulte [o qubit](xref:microsoft.quantum.concepts.qubit).

## <a name="hadamard"></a>Hadamard

A operação Hadamard (também conhecida como portão ou transformação Hadamard) atua em um único [qubit](xref:microsoft.quantum.glossary#qubit) e a coloca em uma [superposição](xref:microsoft.quantum.glossary#superposition) uniforme de $ \ket {0} $ ou $ \ket {1} $ se o qubit estiver inicialmente no estado $ \ket {0} $. Em Q #, essa operação é aplicada pela operação predefinida [`H`](xref:microsoft.quantum.intrinsic.h) .

## <a name="immutable"></a>Imutável

Uma variável cujo valor não pode ser alterado. Uma variável imutável em Q # é criada usando a `let` palavra-chave. Para declarar variáveis que *podem* ser alteradas, use a palavra-chave [mutable](xref:microsoft.quantum.glossary#immutable) para declarar e a `set` palavra-chave para modificar o valor. 

## <a name="measurement"></a>Medida

Uma manipulação de um [qubit](xref:microsoft.quantum.glossary#qubit) (ou conjunto de qubits) que produz o resultado de uma observação, na verdade, obtendo um bit clássico. Para obter mais informações, consulte [o qubit](xref:microsoft.quantum.concepts.qubit#measuring-a-qubit).

## <a name="mutable"></a>Mutável

Uma variável cujo valor pode ser alterado após ser criada. Uma variável mutável em Q # é declarada usando a `mutable` palavra-chave e modificada usando a `set` palavra-chave. As variáveis criadas com a `let` palavra-chave são [imutáveis](xref:microsoft.quantum.glossary#immutable) e seu valor não pode ser alterado.

## <a name="namespace"></a>Namespace

Um rótulo para uma coleção de nomes relacionados (ou seja, [operações](xref:microsoft.quantum.glossary#operation), [funções](xref:microsoft.quantum.glossary#function)e [tipos definidos pelo usuário](xref:microsoft.quantum.glossary#user-defined-type)). Por exemplo, o namespace [Microsoft. Quantum.](xref:microsoft.quantum.preparation) Preparation rotula todos os símbolos definidos na biblioteca padrão que ajudam na preparação de Estados iniciais.

## <a name="operation"></a>Operação

A unidade básica de execução Quantum em Q #. Ele é basicamente equivalente a uma função em C, C++ ou Python, ou um método estático em C# ou Java. Para obter mais informações, consulte [operações e funções](xref:microsoft.quantum.guide.operationsfunctions).

## <a name="operator-application"></a>Aplicativo do operador

Executando uma operação Quantum. Isso normalmente aplica uma matriz unitário ao vetor de estado atual do Quantum.

## <a name="oracle"></a>Oracle

Uma sub-rotina que fornece informações dependentes de dados para um algoritmo Quantum em tempo de execução. Normalmente, o objetivo é fornecer uma [superposição](xref:microsoft.quantum.glossary#superposition) de saídas correspondentes às entradas que estão em superposição. Para obter mais informações, consulte [ORACLES](xref:microsoft.quantum.libraries.data-structures#oracles).

## <a name="partial-application"></a>Aplicativo parcial

Chamar uma [função](xref:microsoft.quantum.glossary#function) ou [operação](xref:microsoft.quantum.glossary#operation) sem todas as entradas necessárias. Isso retorna um novo [callable](xref:microsoft.quantum.glossary#callable) que precisa apenas dos parâmetros ausentes (indicados por um sublinhado) para ser fornecido durante um aplicativo futuro. Por exemplo, dada a função, `MyFunc(x : int, y : int) : int {return x + y;}` você pode aplicá-la parcialmente a uma nova função `let NewFunc = MyFunc(_, 3)` . Em seguida, você pode chamar a nova função em um momento posterior com o parâmetro Missing, `NewFunc(2)` que retorna o valor *5*.  Para obter mais informações, consulte [parcial Application](xref:microsoft.quantum.guide.operationsfunctions#partial-application).

## <a name="pauli-operators"></a>Operadores Pauli

Um conjunto de três matrizes de 2 x 2 unitários conhecidas como as `X` `Y` operações de `Z` Quantum e. A matriz de identidade, $I $, geralmente é incluída no conjunto também.  $I = \begin{bmatrix} 1 & 0 \\ \\ 0 & 1 \end{bmatrix} $, $X = \begin{bmatrix} 0 & 1 \\ \\ 1 & 0 \end{bmatrix} $, $Y = \begin{bmatrix} 0 &-i \\ \\ i & 0 \end{bmatrix} $, $Z = \begin{bmatrix} 1 & 0 \\ \\ 0 &-1 \end{bmatrix} $.   Para obter mais informações, consulte [operações de qubit único](xref:microsoft.quantum.concepts.qubit#single-qubit-operations).

## <a name="quantum-circuit-diagram"></a>Diagrama de circuito Quantum

Um método para representar graficamente a sequência de [operações](xref:microsoft.quantum.glossary#operation) (ou [Gates](xref:microsoft.quantum.glossary#gate)) para programas Quantum simples, por exemplo, ![ diagrama de circuito de amostra ](~/media/qpe.png) . Para obter mais informações, consulte [circuitos Quantum](xref:microsoft.quantum.concepts.circuits).

## <a name="quantum-libraries"></a>Bibliotecas Quantum

Coleções de [operações](xref:microsoft.quantum.glossary#operation), [funções](xref:microsoft.quantum.glossary#function) e [tipos definidos pelo usuário](xref:microsoft.quantum.glossary#user-defined-type) para a criação de programas em Q #. A [biblioteca padrão](xref:microsoft.quantum.libraries.standard.intro) é instalada por padrão. Outras bibliotecas disponíveis são a [biblioteca de química](xref:microsoft.quantum.chemistry.concepts.intro), a [biblioteca de números](xref:microsoft.quantum.numerics.intro) e a biblioteca de aprendizado de [máquina](xref:microsoft.quantum.machine-learning.concepts.intro).

## <a name="quantum-state"></a>Estado do Quantum

O estado preciso de um sistema Quantum isolado, do qual as probabilidades de [medida](xref:microsoft.quantum.glossary#measurement) podem ser extraídas. Na computação Quantum, o simulador Quantum usa essas informações para simular como qubits responder às operações. Para obter mais informações, consulte [o qubit](xref:microsoft.quantum.concepts.qubit).

## <a name="qubit"></a>Qubit

Uma unidade básica de informações de Quantum, análoga a um *pouco* na computação clássica. Para obter mais informações, consulte [o qubit](xref:microsoft.quantum.concepts.qubit).

## <a name="repeat-until-success"></a>Repetir-até-êxito

Um algoritmo Quantum que Probabilistic teve sucesso. Após a falha, a rotina tentará novamente até que tenha êxito (ou um limite tenha sido atingido). Para obter mais informações, consulte [repetir até êxito (RUS)](xref:microsoft.quantum.guide.controlflow#repeat-until-success-loop)

## <a name="standard-libraries"></a>Bibliotecas padrão

[Operações](xref:microsoft.quantum.glossary#operation), [funções](xref:microsoft.quantum.glossary#function) e [tipos definidos pelo usuário](xref:microsoft.quantum.glossary#user-defined-type) que são instalados juntamente com o compilador Q # durante a instalação. A implementação da biblioteca padrão é independente em relação aos computadores de destino. Para obter mais informações, consulte [bibliotecas padrão](xref:microsoft.quantum.libraries.standard.intro).

## <a name="superposition"></a>Superposição

O conceito na computação Quantum que um [qubit](xref:microsoft.quantum.glossary#qubit) é uma combinação linear de dois Estados, $ \ket{\0} $ e $ \ket{\1} $, até que seja [medido](xref:microsoft.quantum.glossary#measurement).  Para obter mais informações, consulte [noções básicas sobre computação Quantum](xref:microsoft.quantum.overview.understanding).

## <a name="target-machine"></a>Computador de destino

Um destino de compilação que reduz um programa Quantum abstrato em direção a hardware ou simulação. Isso normalmente inclui regravações para muitas finalidades, incluindo substituição de portão, codificação para correção de erros, layout geométrico e outros. Para obter mais informações, consulte [simuladores do Quantum e aplicativos de host](xref:microsoft.quantum.machines).

## <a name="teleportation"></a>Portabilidade

Um método para regenerar dados ou o [estado Quantum](xref:microsoft.quantum.glossary#quantum-state)de um [qubit](xref:microsoft.quantum.glossary#qubit) de um lugar para outro sem mover fisicamente o qubit, usando [Entanglement](xref:microsoft.quantum.glossary#entanglement) e [medição](xref:microsoft.quantum.glossary#measurement).  Para obter mais informações, consulte [circuitos Quantum](xref:microsoft.quantum.concepts.circuits) e o respectivo Kata no [Quantum katas](xref:microsoft.quantum.overview.katas).

## <a name="tuple"></a>Tupla

Uma coleção de valores separados por vírgula que atua como um único valor. O *tipo* de uma tupla é definido pelos tipos de valores que ela contém. Em Q #, as tuplas são [imutáveis](xref:microsoft.quantum.glossary#immutable) e podem ser aninhadas, conter matrizes ou usadas em uma matriz. Para obter mais informações, consulte [tipos de tupla](xref:microsoft.quantum.guide.types#tuple-types).

## <a name="unitary-operator"></a>Operador unitário

Um operador cujo inverso é igual a seu [adjacente](xref:microsoft.quantum.glossary#adjoint), ou seja, $UU ^ {\dagger} = \id $.

## <a name="user-defined-type"></a>Tipo definido pelo usuário

Uma coleção de tipos internos ou definidos anteriormente que podem ser referidos como uma única unidade. Para obter mais informações, consulte [tipos definidos pelo usuário](xref:microsoft.quantum.guide.types#user-defined-types).