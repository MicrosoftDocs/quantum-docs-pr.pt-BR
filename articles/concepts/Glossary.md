---
title: Glossário de computação quântica
description: Um glossário de termos comuns, ações e objetos usados na computação quântica.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.glossary
ms.openlocfilehash: ee78515a0f47730b7d3df10da0853c5b8a7f6624
ms.sourcegitcommit: 7d350db4b5e766cd243633aee7d0a839b6274bd6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "81482218"
---
# <a name="quantum-computing-glossary"></a>Glossário de computação quântica

## <a name="adjoint"></a>Adjoint

A complexa transposição conjugada de uma [operação.](xref:microsoft.quantum.glossary#operation) Para operações que implementam um operador [unitário,](xref:microsoft.quantum.glossary#unitary-operator) a junta é o inverso da operação e é indicada por um símbolo de punhal. Por exemplo, se `U` a operação representar o operador `Adjoint U` unitário $U$, então representa $U^\dagger$. Para obter mais informações, consulte [Adjoint](xref:microsoft.quantum.language.file-structure#adjoint).

## <a name="ancilla"></a>Ancilla

Um [qubit](xref:microsoft.quantum.glossary#qubit) que serve como memória temporária para um computador quântico e é alocado e desalocado conforme necessário.  Para obter mais informações, consulte [Vários qubits](xref:microsoft.quantum.concepts.multiple-qubits).

## <a name="bell-state"></a>Estado de Bell

Um dos quatro [estados quânticos](xref:microsoft.quantum.glossary#quantum-state) específicos [emaranhados](xref:microsoft.quantum.glossary#entanglement) de dois qubits. Os quatro estados são definidos $\ket{\beta_{ij}} = (\mathbb{I} \otimes{00} X^iZ^j) (\ket + \ket{11}) / \sqrt{2}$. Um estado de Bell também é conhecido como um [par de EPR](xref:microsoft.quantum.glossary#epr-pair).

## <a name="bloch-sphere"></a>Esfera bloch

Uma representação gráfica de um [estado quântico](xref:microsoft.quantum.glossary#quantum-state) de[qubit](xref:microsoft.quantum.glossary#qubit) único como um ponto em uma esfera unitária tridimensional. Para obter mais informações, consulte [Visualizando Qubits e Transformações usando a Esfera Bloch](xref:microsoft.quantum.concepts.qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere).

## <a name="callable"></a>Callable

Uma [operação](xref:microsoft.quantum.glossary#operation) ou [função](xref:microsoft.quantum.glossary#function) na língua Q#. Para obter mais informações, consulte [Operação e tipos de função](xref:microsoft.quantum.language.type-model#operation-and-function-types).

## <a name="clifford-group"></a>Grupo Clifford

O conjunto de operações que ocupam os oitavas da [esfera bloch](xref:microsoft.quantum.glossary#bloch-sphere) e afetam as permutações dos [operadores de Pauli.](xref:microsoft.quantum.glossary#pauli-operators) Entre elas estão as operações [$X$](xref:microsoft.quantum.intrinsic.x) [$Y$](xref:microsoft.quantum.intrinsic.y) [$Z,](xref:microsoft.quantum.intrinsic.z) [$H$](xref:microsoft.quantum.intrinsic.h) e [$S$](xref:microsoft.quantum.intrinsic.s).

## <a name="controlled"></a>Controlado

Uma [operação](xref:microsoft.quantum.glossary#operation) quântica que toma um ou mais [qubits](xref:microsoft.quantum.glossary#qubit) como facilitadores para a operação alvo. Para obter mais informações, consulte [Controlado](xref:microsoft.quantum.language.type-model#controlled).

## <a name="dirac-notation"></a>Notação de Dirac

Uma abreviação simbólica que simplifica a representação dos [estados quânticos,](xref:microsoft.quantum.glossary#quantum-state)também chamada notação *bra-ket.*  A porção *do sutiã* representa um vetor de linha, por exemplo $\bra{A} = \begin{bmatrix} A{_1} & A{_2} \end{bmatrix}$ e a porção \\ \\ *ket* representa um vetor de coluna, $\ket{B} = \begin{bmatrix} B{_1} B{_2} \end{bmatrix}$. Para obter mais informações, consulte [Notação dirac](xref:microsoft.quantum.concepts.dirac).

## <a name="eigenvalue"></a>Valor eigenvalue

O fator pelo qual a magnitude de um [eigenvector de](xref:microsoft.quantum.glossary#eigenvector) uma determinada transformação é alterada pela aplicação da transformação.  Dada uma matriz quadrada $M$ e um eigenvector $v$, então $Mv = cv$, onde $c$ é o valor eigenvalue e pode ser um número complexo de qualquer argumento. Para obter mais informações, consulte [conceitos de matriz avançada](xref:microsoft.quantum.concepts.matrix-advanced).

## <a name="eigenvector"></a>Eigenvector

Um vetor cuja direção é inalterada por uma dada transformação e cuja magnitude é alterada por um fator correspondente ao [valor eigenvalue](xref:microsoft.quantum.glossary#eigenvalue)desse vetor . Dada uma matriz quadrada $M$ e um valor eigenvalue $c$, então $Mv = cv$, onde $v$ é um eigenvector da matriz e pode ser um número complexo de qualquer argumento. Para obter mais informações, consulte [conceitos de matriz avançada](xref:microsoft.quantum.concepts.matrix-advanced).

## <a name="entanglement"></a>Emaranhamento

Partículas [quânticas, como qubits,](xref:microsoft.quantum.glossary#qubit)podem ser conectadas ou *emaranhadas* de tal forma que não podem ser descritas independentemente umas das outras. Seus resultados de medição estão correlacionados mesmo quando estão separados infinitamente longe. O emaranhamento é essencial para [medir](xref:microsoft.quantum.glossary#measurement) o [estado](xref:microsoft.quantum.glossary#quantum-state) de um qubit.  Para obter mais informações, consulte [conceitos de matriz avançada](xref:microsoft.quantum.concepts.matrix-advanced).

## <a name="epr-pair"></a>Par de EPR

Um dos quatro estados [quânticos](xref:microsoft.quantum.glossary#quantum-state) específicos emaranhados de dois [qubits](xref:microsoft.quantum.glossary#qubit). Os quatro estados são definidos $\ket{\beta_{ij}}{1} = (\mathbb \otimes{00} X^iZ^j) (\ket + \ket{11}) / \sqrt{2}$. Um par de EPR também é conhecido como um [estado de Bell](xref:microsoft.quantum.glossary#bell-state)

## <a name="evolution"></a>Evolução

Como um [estado quântico](xref:microsoft.quantum.glossary#quantum-state) muda com o tempo. Para obter mais informações, consulte [Os exponenciais matrix](xref:microsoft.quantum.concepts.matrix-advanced#matrix-exponentials).

## <a name="function"></a>Função
Um tipo de subrotina na linguagem Q# que é puramente clássica (não quântica). Embora as funções sejam usadas dentro de algoritmos quânticos, elas não podem agir em [qubits](xref:microsoft.quantum.glossary#qubit) ou [operações](xref:microsoft.quantum.glossary#operation)de chamada . Para obter mais informações, consulte [Operação e tipos de função](xref:microsoft.quantum.language.type-model#operation-and-function-types).

## <a name="gate"></a>Portão

Um termo legado para uma [operação](xref:microsoft.quantum.glossary#operation)quântica, baseado no conceito de portões lógicos clássicos. Um [circuito quântico](xref:microsoft.quantum.glossary#quantum-circuit-diagram) é uma rede de portões (ou operações), baseada no conceito semelhante de circuitos lógicos clássicos.

## <a name="global-phase"></a>Fase global

Quando dois [estados](xref:microsoft.quantum.glossary#quantum-state) são idênticos a um múltiplo de um número complexo $e^{i\phi}$, dizem que eles diferem até uma fase global. Ao contrário das fases locais, as fases globais não podem ser observadas através de qualquer [medição.](xref:microsoft.quantum.glossary#measurement) Para obter mais informações, consulte [O Qubit](xref:microsoft.quantum.concepts.qubit).

## <a name="hadamard"></a>Hadamard

A operação Hadamard (também conhecida como portão ou transformação de Hadamard) atua em um único [qubit](xref:microsoft.quantum.glossary#qubit) e{1}coloca-o em uma [superposição](xref:microsoft.quantum.glossary#superposition) uniforme de $\ket{0}$ ou $\ket $ se o qubit estiver inicialmente no estado de $\ket{0}$ . Em Q#, esta operação é aplicada [`H`](xref:microsoft.quantum.intrinsic.h) pela operação pré-definida.

## <a name="immutable"></a>Imutável

Uma variável cujo valor não pode ser alterado. Uma variável imutável em Q# é `let` criada usando a palavra-chave. Para declarar variáveis que *podem* ser alteradas, use a `set` palavra-chave [mutável](xref:microsoft.quantum.glossary#immutable) para declarar e a palavra-chave para modificar o valor. 

## <a name="measurement"></a>Medida

Uma manipulação de um [qubit](xref:microsoft.quantum.glossary#qubit) (ou conjunto de qubits) que produz o resultado de uma observação, obtendo um bit clássico. Para obter mais informações, consulte [O Qubit](xref:microsoft.quantum.concepts.qubit#measuring-a-qubit).

## <a name="mutable"></a>Mutável

Uma variável cujo valor pode ser alterado após sua criação. Uma variável mutável em Q# `mutable` é declarada usando `set` a palavra-chave e modificada usando a palavra-chave. As variáveis criadas `let` com a palavra-chave são [imutáveis](xref:microsoft.quantum.glossary#immutable) e seu valor não pode ser alterado.

## <a name="namespace"></a>Namespace

Um rótulo para uma coleção de nomes relacionados (ou seja, [operações,](xref:microsoft.quantum.glossary#operation) [funções](xref:microsoft.quantum.glossary#function)e [tipos definidos pelo usuário](xref:microsoft.quantum.glossary#user-defined-type)). Por exemplo, o namespace [Microsoft.Quantum.Preparation](xref:microsoft.quantum.preparation) rotula todos os símbolos definidos na biblioteca padrão que ajudam na preparação dos estados iniciais.

## <a name="operation"></a>Operação

A unidade básica de execução quântica em Q#. É aproximadamente equivalente a uma função em C, C++ ou Python, ou um método estático em C# ou Java. Para obter mais informações, consulte [Operação e tipos de função](xref:microsoft.quantum.language.type-model#operation-and-function-types).

## <a name="operator-application"></a>Aplicação do operador

Realizando uma operação quântica. Isso normalmente aplica uma matriz unitária ao vetor de estado quântico atual.

## <a name="oracle"></a>Oracle

Uma subrotina que fornece informações dependentes de dados a um algoritmo quântico em tempo de execução. Normalmente, o objetivo é fornecer uma [superposição](xref:microsoft.quantum.glossary#superposition) de saídas correspondentes às entradas que estão em superposição. Para obter mais informações, consulte [Oracles](xref:microsoft.quantum.libraries.data-structures#oracles).

## <a name="partial-application"></a>Aplicação parcial

Chamando uma [função](xref:microsoft.quantum.glossary#function) ou [operação](xref:microsoft.quantum.glossary#operation) sem todas as entradas necessárias. Isso retorna um novo [callable](xref:microsoft.quantum.glossary#callable) que só precisa dos parâmetros faltantes (indicados por um sublinhado) para serem fornecidos durante uma aplicação futura. Por exemplo, dada a função, `MyFunc(x : int, y : int) : int {return x + y;}` você pode `let NewFunc = MyFunc(_, 3)`aplicá-la parcialmente a uma nova função. Em seguida, você pode chamar a nova função `NewFunc(2)` posteriormente com o parâmetro ausente que retorna o valor *5*.  Para obter mais informações, consulte [Aplicativo Parcial](xref:microsoft.quantum.language.expressions#partial-application).

## <a name="pauli-operators"></a>Operadores pauli

Um conjunto de três matrizes unitárias 2 `X` `Y` x `Z` 2 conhecidas como operações quânticas e 2. A matriz de identidade, $I$, é frequentemente incluída no conjunto também.  $I = \start{bmatrix} \\ \\ 1 & 0 0 & 1 \end{bmatrix}$, $X \\ \\ = \begin{bmatrix} 0 & 1 1 1 & 0 \\ \\ \end{bmatrix}$, $Y = \begin{bmatrix} 0 \\ \\ & -i i & 0 \end{bmatrix}$, $Z = \begin{bmatrix} 1 & 0 0 0 0 & -1 \end{bmatrix}$.   Para obter mais informações, consulte [operações de qubit único](xref:microsoft.quantum.concepts.qubit#single-qubit-operations).

## <a name="quantum-circuit-diagram"></a>Diagrama de circuito quântico

Um método para representar graficamente a seqüência de [operações](xref:microsoft.quantum.glossary#operation) ![(ou](~/media/qpe.png) [portões](xref:microsoft.quantum.glossary#gate)) para programas quânticos simples, por exemplo diagrama de circuito de amostra . Para obter mais informações, consulte [circuitos quânticos](xref:microsoft.quantum.concepts.circuits).

## <a name="quantum-libraries"></a>Bibliotecas quânticas

Coleções de [operações,](xref:microsoft.quantum.glossary#operation)funções e tipos [definidos](xref:microsoft.quantum.glossary#function) [pelo usuário](xref:microsoft.quantum.glossary#user-defined-type) para criar programas Q#. A [biblioteca Padrão](xref:microsoft.quantum.libraries.standard.intro) é instalada por padrão. Outras bibliotecas disponíveis são a [biblioteca química,](xref:microsoft.quantum.chemistry.concepts.intro)a [biblioteca Numérica](xref:microsoft.quantum.numerics.intro) e a biblioteca [de aprendizagem de máquina.](xref:microsoft.quantum.machine-learning.concepts.intro)

## <a name="quantum-state"></a>Estado quântico

O estado preciso de um sistema quântico isolado, do qual as probabilidades de [medição](xref:microsoft.quantum.glossary#measurement) podem ser extraídas. Na computação quântica, o simulador quântico usa essas informações para simular como os qubits respondem às operações. Para obter mais informações, consulte [O Qubit](xref:microsoft.quantum.concepts.qubit).

## <a name="qubit"></a>Qubit

Uma unidade básica de informação quântica, análoga a um *pouco* na computação clássica. Para obter mais informações, consulte [O Qubit](xref:microsoft.quantum.concepts.qubit).

## <a name="repeat-until-success"></a>Repetição até o sucesso

Um algoritmo quântico que probalistamente consegue. Após o fracasso, a rotina tentará novamente até que seja bem-sucedido (ou um limite tenha sido atingido). Para obter mais informações, consulte [Repetir até o sucesso (RUS)](xref:microsoft.quantum.techniques.qubits#measurements)

## <a name="standard-libraries"></a>Bibliotecas padrão

[Operações,](xref:microsoft.quantum.glossary#operation) [funções](xref:microsoft.quantum.glossary#function) e tipos [definidos pelo usuário](xref:microsoft.quantum.glossary#user-defined-type) que são instalados junto com o compilador Q# durante a instalação. A implementação padrão da biblioteca é agnóstica em relação às máquinas alvo. Para obter mais informações, consulte [Bibliotecas Padrão](xref:microsoft.quantum.libraries.standard.intro).

## <a name="superposition"></a>Superposição

O conceito na computação quântica de que um [qubit](xref:microsoft.quantum.glossary#qubit) é uma combinação linear de dois estados, $\ket{\0}$ e $\ket{\1}$, até que seja [medido](xref:microsoft.quantum.glossary#measurement).  Para obter mais informações, consulte [O que é computação quântica](xref:microsoft.quantum.overview.what).

## <a name="target-machine"></a>Máquina alvo

Um alvo de compilação que reduz um programa quântico abstrato para hardware ou simulação. Isso normalmente inclui regravações para muitos propósitos, incluindo substituição de portão, codificação para correção de erros, layout geométrico e outros. Para obter mais informações, consulte [simuladores quânticos e aplicativos de host](xref:microsoft.quantum.machines).

## <a name="teleportation"></a>Portabilidade

Um método para regenerar dados, ou o [estado quântico,](xref:microsoft.quantum.glossary#quantum-state)de um [qubit](xref:microsoft.quantum.glossary#qubit) de um lugar para outro sem mover fisicamente o qubit, [utilizando emaranhamento](xref:microsoft.quantum.glossary#entanglement) e [medição](xref:microsoft.quantum.glossary#measurement).  Para obter mais informações, consulte [circuitos quânticos](xref:microsoft.quantum.concepts.circuits) [e colocando tudo junto](xref:microsoft.quantum.techniques.puttingittogether).

## <a name="tuple"></a>Tupla

Uma coleção de valores separados por comma que atua como um único valor. O *tipo* de tupla é definido pelos tipos de valores que contém. Em Q#, as tuplas são [imutáveis](xref:microsoft.quantum.glossary#immutable) e podem ser aninhadas, conter matrizes ou usadas em uma matriz. Para obter mais informações, consulte [os tipos tuplos](xref:microsoft.quantum.language.type-model#tuple-types).

## <a name="unitary-operator"></a>Operador unitário

Um operador cujo inverso é igual ao seu [adjoint](xref:microsoft.quantum.glossary#adjoint), ou seja, $UU^{\dagger} = \id$.

## <a name="user-defined-type"></a>Tipo definido pelo usuário

Uma coleção de tipos incorporados ou previamente definidos que podem ser referidos como uma única unidade. Para obter mais informações, consulte [tipos definidos pelo usuário](xref:microsoft.quantum.language.type-model#user-defined-types).