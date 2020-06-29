---
title: Explorar o entrelaçamento com Q#
description: Saiba como escrever um programa quântico em Q#. Desenvolver um aplicativo de Estado de Bell usando o QDK (Quantum development kit)
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 05/29/2020
ms.topic: tutorial
uid: microsoft.quantum.write-program
ms.openlocfilehash: 16c93b3dd17363c06602529cb34e8fc84aadc7a8
ms.sourcegitcommit: af10179284967bd7a72a52ae7e1c4da65c7d128d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "85415415"
---
# <a name="tutorial-explore-entanglement-with-q"></a>Tutorial: Explorar o emaranhamento com o Q\#

Neste tutorial, mostraremos como escrever um programa Q# que processa e mede qubits e demonstra os efeitos da superposição e do emaranhamento.

Você escreverá um aplicativo chamado Bell para demonstrar o entrelaçamento quântico.
O nome Bell foi criado em referência aos estados Bell, que são estados quânticos específicos de dois qubits usados para representar os exemplos mais simples de sobreposição e entrelaçamento quântico.

## <a name="pre-requisites"></a>Pré-requisitos

Se estiver pronto para começar a codificação, siga estas etapas antes de continuar: 

* [Instale](xref:microsoft.quantum.install) o kit de desenvolvimento Quantum usando o ambiente de desenvolvimento e a linguagem preferencial.
* Caso já tenha o QDK instalado, verifique se você o [atualizou](xref:microsoft.quantum.update) para a última versão

Você também pode acompanhar a narração sem instalar o QDK, revisando as visões gerais da linguagem de programação Q # e os primeiros conceitos da computação Quantum.

## <a name="in-this-tutorial-youll-learn-how-to"></a>Neste tutorial, você aprenderá como:

> [!div class="checklist"]
> * Criar e combinar operações em p\#
> * Crie operações para colocar qubits em superposição, entangle e meça-las.
> * Demonstre o Quantum Entanglement com um programa Q # executado em um simulador. 

## <a name="demonstrating-qubit-behavior-with-the-qdk"></a>Demonstrando o comportamento do qubit com o QDK

Onde os bits clássicos contêm apenas um valor binário, como 0 ou 1, o estado de um [qubit](xref:microsoft.quantum.glossary#qubit) pode estar em uma **sobreposição** de 0 e 1.  Conceitualmente, o estado de um qubit pode ser pensado como uma direção em um espaço abstrato (também conhecido como um vetor).  Um estado qubit pode estar em qualquer uma das possíveis direções. Os dois **estados clássicos** são as duas direções, que representam 100% de chance de medir 0 e 100% de chance de medir 1.

O ato de medição produz um resultado binário e altera um estado do qubit.
A medida produz um valor binário, 0 ou 1.  O qubit passa de estar em sobreposição (qualquer direção) para um dos estados clássicos.  Depois disso, repetir a mesma medição sem nenhuma operação intermediária produz o mesmo resultado binário.  

Vários qubits podem ser [**entrelaçados**](xref:microsoft.quantum.glossary#entanglement).  Quando fazemos uma medição de um qubit entrelaçado, nosso conhecimento do estado dos outros é atualizado também.

Agora, estamos prontos para demonstrar como o Q# expressa esse comportamento.  Você começará com o programa mais simples possível e o desenvolverá para demonstrar a sobreposição quântica e o entrelaçamento quântico.

## <a name="creating-a-q-project"></a>Criando um projeto do Q #

A primeira coisa que precisamos fazer é criar um novo projeto Q #. Neste tutorial, vamos usar o ambiente baseado em [aplicativos de linha de comando com vs Code](xref:microsoft.quantum.install.standalone).

Para criar um novo projeto, no VS Code: 

1. Clique em **Exibir**  ->  **paleta de comandos** e selecione **Q #: criar novo projeto**.
2. Clique em **aplicativo de console autônomo**.
3. Navegue até o local para salvar o projeto e clique em **criar projeto**.
4. Quando o projeto for criado com êxito, clique em **abrir novo projeto...** no canto inferior direito.

Nesse caso, chamamos o projeto `Bell` . Isso gera dois arquivos: `Bell.csproj` , o arquivo de projeto e `Program.qs` um modelo de um aplicativo Q # que usaremos para escrever nosso aplicativo. O conteúdo de `Program.qs` deve ser:

```qsharp
   namespace Bell {

      open Microsoft.Quantum.Canon;
      open Microsoft.Quantum.Intrinsic;
    

      @EntryPoint()
      operation HelloQ() : Unit {
          Message("Hello quantum world!");
      }
   }
```

## <a name="write-the-q-application"></a>Escrever o \# aplicativo Q
 
Nossa meta é preparar dois qubits em um estado quântico específico, demonstrando como operar em qubits com Q# para alterar seu estado e demonstrar os efeitos da sobreposição e entrelaçamento. Criaremos essa peça por parte para apresentar os Estados, as operações e a medição do qubit.

### <a name="initialize-qubit-using-measurement"></a>Inicializar qubit usando medição

no primeiro código abaixo, mostramos como trabalhar com qubits no Q#.  Apresentaremos duas operações [`M`](xref:microsoft.quantum.intrinsic.m) e [`X`](xref:microsoft.quantum.intrinsic.x) transformaremos o estado de um qubit. Neste snippet de código, uma operação `SetQubitState` é definida que usa como parâmetro um qubit e outro parâmetro, `desired`, que representa o estado no qual gostaríamos que o qubit estivesse.  A operação `SetQubitState` executa uma medida no qubit usando a operação `M`.  Em Q #, uma medida qubit sempre retorna um `Zero` ou `One` .  Se a medida retornar um valor diferente do valor desejado, `SetQubitState` "inverte" o qubit; ou seja, ele executará uma `X` operação, que altera o estado de qubit para um novo estado no qual as probabilidades de uma medida retornam `Zero` e `One` são revertidas. Dessa forma, `SetQubitState` o sempre coloca o destino qubit no estado desejado.

Substitua o conteúdo de `Program.qs` pelo código a seguir:


```qsharp
   namespace Bell {
       open Microsoft.Quantum.Intrinsic;
       open Microsoft.Quantum.Canon;

       operation SetQubitState(desired : Result, q1 : Qubit) : Unit {
           if (desired != M(q1)) {
               X(q1);
           }
       }
   }
```

Esta operação agora pode ser chamada para definir um qubit como um estado clássico, retornando `Zero` 100% do tempo ou retornando `One` 100% do tempo.
`Zero` e `One` são constantes que representam os únicos dois possíveis resultados de uma medição de um qubit.

A operação `SetQubitState` mede o qubit. Se o qubit estiver no estado que desejamos, `SetQubitState` o deixará sozinho; caso contrário, executando a operação `X`, alteraremos o estado do qubit para o desejado.

#### <a name="about-q-operations"></a>Sobre as operações Q#

Uma operação Q# é uma sub-rotina quântica. Ou seja, é uma rotina que possa ser chamada que contém chamadas para outras operações de Quantum.

Os argumentos de uma operação são especificados como uma tupla, entre parênteses.

O tipo de retorno da operação é especificado após dois-pontos. Nesse caso, a operação `SetQubitState` não tem retorno, sendo, portanto, marcada como retornando `Unit`. Em Q#, esse é o equivalente de `unit` em F#, que é aproximadamente análogo a `void` em C# e uma tupla vazia (`Tuple[()]`) no Python.

Você usou duas operações quânticas em sua primeira operação Q#:

* A [`M`](xref:microsoft.quantum.intrinsic.m) operação, que mede o estado do qubit
* A [`X`](xref:microsoft.quantum.intrinsic.x) operação, que inverte o estado de um qubit

Uma operação quântica transforma o estado de um qubit. Algumas vezes, as pessoas falam sobre portões quânticos em vez de operações, em analogia a portões lógicos clássicos. Isso está enraizado nos primórdios da computação quântica, quando os algoritmos eram meramente um constructo teórico e eram visualizados como diagramas de forma semelhante à dos diagramas de circuito na computação clássica.

### <a name="counting-measurement-outcomes"></a>Resultados da medição de contagem

Para demonstrar o efeito da operação `SetQubitState`, uma operação `TestBellState` é adicionada. Essa operação aceita como entrada um `Zero` ou `One` e chama a operação `SetQubitState` algum número de vezes com essa entrada, além de contar o número de vezes que `Zero` foi retornado da medição do qubit e do número de vezes que `One` foi retornado. É claro que, nesta primeira simulação da operação `TestBellState`, esperamos que a saída mostre que todas as medições do conjunto de qubits com `Zero` como a entrada do parâmetro retornarão `Zero` e todas as medições de um conjunto de qubits com `One` como a entrada do parâmetro retornarão `One`. Além disso, adicionaremos o código para `TestBellState` demonstrar a superposição e Entanglement.

Adicione a seguinte operação ao arquivo `Bell.qs`, dentro do namespace, após o final da operação `SetQubitState`:

```qsharp
   operation TestBellState(count : Int, initial : Result) : (Int, Int) {

       mutable numOnes = 0;
       using (qubit = Qubit()) {

           for (test in 1..count) {
               SetQubitState(initial, qubit);
               let res = M(qubit);

               // Count the number of ones we saw:
               if (res == One) {
                   set numOnes += 1;
               }
           }
            
           SetQubitState(Zero, qubit);
       }

       // Return number of times we saw a |0> and number of times we saw a |1>
       Message("Test results (# of 0s, # of 1s): ");
       return (count - numOnes, numOnes);
   }
```
Observe que adicionamos uma linha antes do `return` para imprimir uma mensagem explicativa no console com a função ( `Message` ) [Microsoft. Quantum. intrínseca. Message]

Essa operação (`TestBellState`) executará um loop para iterações `count`, definirá um valor `initial` especificado em um qubit e, em seguida, medirá (`M`) o resultado. Ela coletará estatísticas sobre quantos zeros e aqueles medidos e os retornará ao chamador. Ela executa outra operação necessária. Ela redefine o qubit para um estado conhecido (`Zero`) antes de retorná-lo, permitindo que outras pessoas aloquem esse qubit em um estado conhecido. Isso é exigido pela instrução `using`.

#### <a name="about-variables-in-q"></a>Sobre variáveis em Q\#

Por padrão, as variáveis em Q# são imutáveis; o valor delas não pode ser alterado depois que elas são associadas. A palavra-chave `let` é usada para indicar a associação de uma variável imutável. Os argumentos da operação são sempre imutáveis.

Caso precise de uma variável cujo valor possa ser alterado, como `numOnes` no exemplo, você poderá declarar a variável com a palavra-chave `mutable`. O valor de uma variável mutável pode ser alterado usando uma instrução `setQubitState`.

Em ambos os casos, o tipo de uma variável é inferido pelo compilador. O Q# não exige nenhuma anotação de tipo para variáveis.

#### <a name="about-using-statements-in-q"></a>Sobre as `using` instruções em Q\#

A instrução `using` também é especial para o Q#. Ela é usada para alocar qubits para uso em um bloco de código. Em Q#, todos os qubits são alocados e liberados dinamicamente, em vez de serem recursos fixos que existem pelo tempo de vida inteiro de um algoritmo complexo. Uma instrução `using` aloca um conjunto de qubits no início e libera esses qubits no final do bloco.

## <a name="execute-the-code-from-the-command-line"></a>Executar o código da linha de comando

Para executar o código, precisamos especificar o compilador *que* pode ser chamado para ser executado quando fornecemos o `dotnet run` comando. Isso é feito com uma simples alteração no arquivo Q #, adicionando uma linha com `@EntryPoint()` diretamente antes do callable: a `TestBellState` operação nesse caso. O código completo deve ser:

```qsharp
namespace Bell {
    open Microsoft.Quantum.Canon;
    open Microsoft.Quantum.Intrinsic;

    operation SetQubitState(desired : Result, target : Qubit) : Unit {
        if (desired != M(target)) {
            X(target);
        }
    }

    @EntryPoint()
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using (qubit = Qubit()) {

            for (test in 1..count) {
                SetQubitState(initial, qubit);
                let res = M(qubit);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }

            SetQubitState(Zero, qubit);
        }

    // Return number of times we saw a |0> and number of times we saw a |1>
    Message("Test results (# of 0s, # of 1s): ");
    return (count - numOnes, numOnes);
    }
}
```

Para executar o programa, precisamos especificar os `count` `initial` argumentos e a partir da linha de comando. Vamos escolher por exemplo `count = 1000` e `initial = One` . Insira o seguinte comando:

```dotnetcli
dotnet run --count 1000 --initial One
```

E você deve observar a seguinte saída:

```output
Test results (# of 0s, # of 1s):
(0, 1000)
```

Se você tentar com `initial = Zero` , deverá observar:

```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s):
(1000, 0)
```

## <a name="prepare-superposition"></a>Preparar a superposição

Agora vamos ver como Q # expressa as maneiras de colocar qubits em superposição.  Lembre-se de que o estado de um qubit pode estar em uma sobreposição de 0 e 1.  Usaremos a operação `Hadamard` para fazer isso. Se o qubit estiver em qualquer um dos estados clássicos (em que uma medição retorna `Zero` sempre ou `One` sempre), a operação `Hadamard` ou `H` colocará o qubit em um estado em que uma medição do qubit retornará `Zero` 50% do tempo e retornará `One` 50% do tempo.  Conceitualmente, o qubit pode ser pensado como a metade entre o `Zero` e o `One`.  Agora, quando simularmos a operação `TestBellState`, veremos que os resultados retornarão aproximadamente um número igual de `Zero` e `One` após a medição.  

### <a name="x-flips-qubit-state"></a>`X`inverte o estado qubit

Primeiro, tentaremos inverter o qubit (se o qubit estiver no `Zero`, o estado será invertido para `One` e vice-versa). Isso é feito com a execução de uma operação `X` antes de medi-lo em `TestBellState`:

```qsharp
X(qubit);
let res = M(qubit);
```

Agora os resultados são invertidos:

```dotnetcli
dotnet run --count 1000 --initial One
```

```output
Test results (# of 0s, # of 1s):
(1000, 0)
```

```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s):
(0, 1000)
```

Agora vamos explorar as propriedades Quantum do qubits.

### <a name="h-prepares-superposition"></a>`H`Prepara a superposição

Basta substituir a operação `X` na execução anterior por uma operação `H` ou Hadamard. Em vez de inverteremos o qubit até o final de 0 a 1, só o inverteremos até a metade. As linhas substituídas em `TestBellState` agora têm a seguinte aparência:

```qsharp
H(qubit);
let res = M(qubit);
```

Agora os resultados ficam mais interessantes:

```dotnetcli
dotnet run --count 1000 --initial One
```

```output
Test results (# of 0s, # of 1s):
(496, 504)
```

```dotnetcli
dotnet run --count 1000 --initial Zero
```

```output
Test results (# of 0s, # of 1s):
(506, 494)
```

Sempre que medimos, pedimos um valor clássico, mas como o qubit está na metade entre 0 e 1, obtemos (estatisticamente) 0 na metade do tempo e 1 na metade do tempo.
Isso é conhecido como **superposição** e nos dá nossa primeira visão real de um estado quântico.

## <a name="prepare-entanglement"></a>Preparar o entrelaçamento

Agora vamos examinar como o Q# expressa maneiras de entrelaçar qubits.
Primeiro, definimos o primeiro qubit como o estado inicial e usamos a operação `H` para colocá-lo em sobreposição.  Em seguida, antes de medirmos o primeiro qubit, usamos uma nova operação ( `CNOT` ), que significa não ser controlada.  O resultado da execução dessa operação em dois qubits será inverter o segundo qubit se o primeiro qubit for `One`.  Agora, os dois qubits estão entrelaçados.  Nossas estatísticas para o primeiro qubit não mudaram (possibilidade de 50-50 de `Zero` ou `One` após a medição), mas agora, quando medimos o segundo qubit, ele é __sempre__ igual ao que medimos para o primeiro qubit. Nosso `CNOT` entrelaçou os dois qubits, de modo que o que acontecer com um deles acontecerá com o outro. Se você inverter as medidas (fizer o segundo qubit antes do primeiro), a mesma coisa acontecerá. A primeira medida será aleatória e a segunda estará na etapa de bloqueio com tudo o que foi descoberto para o primeiro.

A primeira coisa que precisaremos fazer é alocar dois qubits em vez de um em `TestBellState` :

```qsharp
using ((q0, q1) = (Qubit(), Qubit())) {
```

Isso nos permitirá adicionar uma nova operação (`CNOT`) antes de medir (`M`) em `TestBellState`:

```qsharp
SetQubitState(initial, q0);
SetQubitState(Zero, q1);

H(q0);
CNOT(q0, q1);
let res = M(q0);
```

Adicionamos outra operação `SetQubitState` para inicializar o primeiro qubit, a fim de garantir que ele esteja sempre no estado `Zero` quando começarmos.

Também precisamos redefinir o segundo qubit antes de liberá-lo.

```qsharp
SetQubitState(Zero, q0);
SetQubitState(Zero, q1);
```

A rotina completa agora tem esta aparência:

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                SetQubitState(initial, q0);
                SetQubitState(Zero, q1);

                H(q0);
                CNOT(q0,q1);
                let res = M(q0);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }

            SetQubitState(Zero, q0);
            SetQubitState(Zero, q1);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes);
    }
```

Se executarmos isso, obteremos exatamente o mesmo resultado 50-50 que obtivemos antes. No entanto, estamos interessados mesmo em como o segundo qubit reage ao primeiro que está sendo medido. Adicionaremos essa estatística com uma nova versão da operação `TestBellState`:

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int, Int) {
        mutable numOnes = 0;
        mutable agree = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                SetQubitState(initial, q0);
                SetQubitState(Zero, q1);

                H(q0);
                CNOT(q0, q1);
                let res = M(q0);

                if (M(q1) == res) {
                    set agree += 1;
                }

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            
            SetQubitState(Zero, q0);
            SetQubitState(Zero, q1);
        }

        // Return times we saw |0>, times we saw |1>, and times measurements agreed
        Message("Test results (# of 0s, # of 1s, # of agreements)");
        return (count-numOnes, numOnes, agree);
    }
```

O novo valor retornado (`agree`) faz o acompanhamento toda vez que a medida do primeiro qubit corresponde à medida do segundo qubit.

Executando o código que obtemos:

```dotnetcli
dotnet run --count 1000 --initial One
```
```output
(505, 495, 1000)
```
```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s, # of agreements)
(507, 493, 1000)
```

Conforme indicado na visão geral, nossas estatísticas para o primeiro qubit não foram alteradas (possibilidade de 50-50 de 0 ou 1), mas agora, quando medimos o segundo qubit, ele é __sempre__ igual ao que medimos para o primeiro qubit, porque eles estão entrelaçados!

## <a name="next-steps"></a>Próximas etapas

O tutorial [Pesquisa de Grover](xref:microsoft.quantum.quickstarts.search) mostrará como criar e executar a pesquisa de Grover, um dos algoritmos mais populares da computação quântica, além de apresentar um bom exemplo de programa Q# que pode ser usado para resolver problemas reais com a computação quântica.  

A [Introdução ao Quantum Development Kit](xref:microsoft.quantum.welcome) recomenda mais maneiras de aprender o Q# e a programação quântica.
