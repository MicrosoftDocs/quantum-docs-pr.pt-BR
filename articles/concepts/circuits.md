---
Título: descrição dos circuitos do Quantum: saiba como representar visualmente operações Quantum simples e complexas com diagramas de circuito Quantum.
Autor: QuantumWriter UID: Microsoft. Quantum. Concepts. circuits MS. Author: v-benbra MS. Date: 12/11/2017 MS. tópico: conceptual no-loc:
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

# <a name="quantum-circuits"></a>Circuitos Quantum
Considere por um momento a transformação unitário $ \text { CNOT } _ { 01 } (H \otimes 1) $ .
Essa sequência de portão é de importância fundamental para a computação Quantum porque ela cria um estado confusas de duas qubit de maneira máxima:

$$\mathrm{CNOT } _ { 01 } (H \otimes 1) \ket { 00 } = \frac { 1 } { \sqrt { 2 } } \left ( \ket { 00 }  +  \ket { 11 } \right ),$$

As operações com essa ou mais complexidade são onipresentes em algoritmos Quantum e correção de erro Quantum, portanto, deve ser um grande alívio de que há um método simples para sua visualização chamada de *diagrama de circuito Quantum*.
O diagrama de circuito para preparar esse estado de Quantum de confusas máximo é:

<!--- ![](.\media\1.svg) --->
<!--Não pode encontrar uma maneira de centralizar facilmente isso... Provavelmente uma extensão necessária:-->
![Diagrama de circuito para um estado confusas de duas qubit](~/media/1.svg)

## <a name="quantum-circuit-diagram-conventions"></a>Convenções de diagrama de circuito Quantum
Essa linguagem visual para operações Quantum pode ser mais prontamente fácil do que escrever sua matriz equivalente quando você entende as convenções para expressar um circuito Quantum.
Analisamos essas convenções abaixo.

Em um diagrama de circuito, cada linha sólida representa um qubit ou mais geralmente um registro de qubit.
Por convenção, a linha superior é qubit registro $ 0 $ e o restante é rotulado em sequência. O circuito de exemplo acima é representado como agindo em dois qubits (ou dois registros equivalentes que consistem em um qubit).
As Gates que atuam em um ou mais registros de qubit são indicadas como uma caixa.
Por exemplo, o símbolo

<!--- ![](.\media\2.svg) --->
<!--Não pode encontrar uma maneira de centralizar facilmente isso... Provavelmente uma extensão necessária:-->
![Símbolo para uma operação Hadamard agindo em um registro de qubit único](~/media/2.svg)

é uma operação [Hadamard](xref:Microsoft.Quantum.Intrinsic.H) que atua em um registro de qubit único.

As Gates da Quantum são ordenadas em ordem cronológica com a porta mais à esquerda como a portão aplicada pela primeira vez ao qubits.
Em outras palavras, se você modelar os fios como tendo o estado Quantum, os fios trazem o estado da Quantum por meio de cada um dos Gates no diagrama da esquerda para a direita.
Isso é para dizer 

<!--- ![](.\media\3.svg) --->
<!--Não pode encontrar uma maneira de centralizar facilmente isso... Provavelmente uma extensão necessária:-->
![Diagrama de Gates Quantum sendo aplicado da esquerda para a direita](~/media/3.svg)

é a matriz unitário $ CBA $ .
A multiplicação de matriz obedece à Convenção oposta: a matriz mais à direita é aplicada primeiro. Em diagramas de circuito Quantum, no entanto, o portão mais à esquerda é aplicado primeiro.
Essa diferença pode, às vezes, levar à confusão. portanto, é importante observar essa diferença significativa entre a notação linear algébricas e os diagramas de circuito Quantum.

## <a name="inputs-and-outputs-of-quantum-circuits"></a>Entradas e saídas de circuitos Quantum
Todos os exemplos anteriores que tinham tido exatamente o mesmo número de fios (qubits) de entrada para uma porta Quantum como o número de cabos do portão Quantum.
A princípio, pode parecer razoável que os circuitos Quantum pudessem ter mais, ou menos, saídas do que as entradas em geral.
No entanto, isso é impossível, pois todas as operações de Quantum, salvar medida, são unitários e, portanto, reversível.
Se eles não tiverem o mesmo número de saídas que não seriam reversível e, portanto, não são unitários, o que é uma contradição.
Por esse motivo, qualquer caixa desenhada em um diagrama de circuito deve ter precisamente o mesmo número de fios inserindo-o como sendo encerrado.

Os diagramas de circuito qubit seguem convenções semelhantes para os qubit únicos.
Como um exemplo de esclarecimento, podemos definir uma operação qubit unitário de dois $ $ a ser $ (H S \otimes X) $ e expressar o circuito equivalentemente como

<!--- ![](.\media\4.svg) --->
<!--Não pode encontrar uma maneira de centralizar facilmente isso... Provavelmente uma extensão necessária:-->
![Diagrama de circuito de uma operação unitário de dois qubit](~/media/4.svg)

Também podemos exibir o $ B $ como tendo uma ação em um único registro de duas qubit em vez de registros de 2 1-qubit, dependendo do contexto no qual o circuito é usado. Talvez a propriedade mais útil desses diagramas de circuito abstrato seja que eles permitam que algoritmos de Quantum complicados sejam descritos em um alto nível sem precisar compilá-los em Gates fundamentais.
Isso significa que você pode obter uma intuição sobre o fluxo de dados para um grande algoritmo Quantum sem a necessidade de entender todos os detalhes de como cada uma das sub-rotinas dentro do algoritmo funciona.

## <a name="controlled-gates"></a>Gates controlados
O outro constructo criado em diagramas de circuito Quantum qubit é Control.
A ação de um portão controlado de Quantum singular, denotado $ \Lambda (G) $ , em que um único valor de qubit controla o aplicativo de $ G $ , pode ser compreendido examinando o exemplo a seguir de uma entrada de estado do produto $ \Lambda (G) ( \alpha \ket { 0 }  +  \beta \ket { 1 } ) \ket { \psi } = \alpha \ket { 0 } \ket { \psi }  +  \beta \ket { 1 } G \ket { \psi } $ . Ou seja, o portão controlado aplica- $ se a G $ ao registro que contém $ \psi $ If e somente se o qubit de controle usar o valor $ 1 $ .
Em geral, descrevemos essas operações controladas em diagramas de circuito como

<!--- ![](.\media\5.svg) --->
<!--Não pode encontrar uma maneira de centralizar facilmente isso... Provavelmente uma extensão necessária:-->
![Diagrama de circuito de um portão controlado individualmente](~/media/5.svg)

Aqui, o círculo preto denota o bit quântico no qual o portão é controlado e uma transmissão vertical denota o unitário que é aplicado quando o qubit de controle usa o valor $ 1 $ .
Para os casos especiais em que $ g = X $ e $ g = Z $ , apresentamos a seguinte notação para descrever a versão controlada das Gates (Observe que o portão-X controlado é o [ $ $ portão CNOT](xref:Microsoft.Quantum.Intrinsic.CNOT)):

<!--- ![](.\media\6.svg) --->
<!--Não pode encontrar uma maneira de centralizar facilmente isso... Provavelmente uma extensão necessária:-->
![Diagrama de circuito para casos especiais de Gates controlados](~/media/6.svg)

Q# fornece métodos para gerar automaticamente a versão controlada de uma operação, o que evita que o programador tenha que codificar essas operações manualmente. Um exemplo disso é mostrado abaixo:

```qsharp
operation PrepareSuperposition(qubit : Qubit) : Unit
is Ctl { // Auto-generate the controlled specialization of the operation
    H(qubit);
}
```

## <a name="measurement-operator"></a>Operador de medida
A operação restante a ser visualizada em diagramas de circuito é medida.
A medição usa um registro qubit, mede-o e gera o resultado como informações clássicas.
Uma operação de medição é denotada por um símbolo de medidor e sempre usa como entrada um registro de qubit (indicado por uma linha sólida) e gera informações clássicas (indicadas por uma linha dupla).
Especificamente, esse subcircuito é semelhante a:

<!--- ![](.\media\7.svg) ---->
<!--Não pode encontrar uma maneira de centralizar facilmente isso... Provavelmente uma extensão necessária:-->
![Símbolo que representa uma operação de medição](~/media/7.svg)

Q# implementa um [operador de medida](xref:Microsoft.Quantum.Intrinsic.Measure) para essa finalidade.
Consulte a [seção sobre medições](xref:microsoft.quantum.libraries.standard.prelude#measurements) para obter mais informações.

Da mesma forma, o subcircuito

<!--- ![](.\media\8.svg) --->
<!--Não pode encontrar uma maneira de centralizar facilmente isso... Provavelmente uma extensão necessária:-->
![Diagrama de circuito que representa uma operação controlada](~/media/8.svg)

fornece um portão controlado de forma clássica, onde $ G $ é aplicado condicionalmente no bit de controle clássico sendo o valor $ 1 $ .

## <a name="teleportation-circuit-diagram"></a>Diagrama de circuito de teleportação
A porta de transporte Quantum talvez seja o melhor algoritmo Quantum para ilustrar esses componentes.
Você pode aprender a usar a teleportabilidade do Quantum [Kata](xref:microsoft.quantum.overview.katas) Quantum correspondente é um método para mover dados dentro de um computador Quantum (ou até mesmo entre computadores Quantum distantes em uma rede Quantum) por meio do uso de Entanglement e medição.
Curiosamente, é realmente capaz de mover um estado Quantum, digamos o valor em um determinado qubit, de um qubit para outro, sem nem mesmo saber qual é o valor da qubit!
Isso é necessário para que o protocolo funcione de acordo com as leis da mecânica quantum.
O circuito de teleportabilidade Quantum é fornecido abaixo; também fornecemos uma versão anotada do circuito para ilustrar como ler o circuito Quantum.

<largura de!--- ![](.\media\tp2.svg) { = 50%} --->
![Circuito de Teleportation Quantum](~/media/tp2.svg)
