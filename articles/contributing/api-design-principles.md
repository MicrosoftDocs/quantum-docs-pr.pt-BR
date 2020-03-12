---
title: 'Princípios de design da API Q #'
description: 'Princípios de design da API Q #'
author: cgranade
ms.author: chgranad
ms.date: 3/9/2020
ms.topic: article
uid: microsoft.quantum.contributing.api-design
ms.openlocfilehash: 03c32331f8988181ec6fedcfc207d752b4a880b2
ms.sourcegitcommit: d61b388651351e5abd4bfe7a672e88b84a6697f8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2020
ms.locfileid: "79024195"
---
# <a name="q-api-design-principles"></a>Princípios de design da API Q #

## <a name="introduction"></a>Introdução

Como uma linguagem e como uma plataforma, o Q # capacita os usuários a escrever, executar, compreender e explorar aplicativos Quantum.
Para capacitar os usuários, quando criamos as bibliotecas de Q #, seguimos um conjunto de princípios de design de API para guiar nossos designs e nos ajudar a criar bibliotecas utilizáveis para a comunidade de desenvolvimento Quantum.
Este artigo lista esses princípios e fornece exemplos para ajudar a ajudá-lo a aplicá-los ao projetar as APIs de Q #.

> [!TIP]
> Este é um documento bastante detalhado destinado a ajudar a orientar o desenvolvimento da biblioteca e as contribuições detalhadas da biblioteca.
> Você provavelmente achará mais útil se estiver escrevendo suas próprias bibliotecas em Q # ou se estiver contribuindo com recursos maiores para o repositório de [bibliotecas do Q #](https://github.com/microsoft/QuantumLibraries).
>
> Por outro lado, se você estiver procurando aprender como contribuir com o kit de desenvolvimento Quantum mais geralmente, sugerimos começar com o guia de [contribuição](xref:microsoft.quantum.contributing).
> Se você estiver procurando informações mais gerais sobre como é recomendável formatar o código de Q #, talvez esteja interessado em verificar o [Guia de estilo](xref:microsoft.quantum.contributing.style).

## <a name="general-principles"></a>Princípios gerais

Principal **princípio:** Expor APIs que colocam o foco em aplicativos Quantum.

- ✅ **escolher** os nomes de operação e de função que refletem a estrutura de alto nível de algoritmos e aplicativos.
- ⛔️ **não** expõem APIs que se concentram principalmente em detalhes de implementação de nível baixo.

Principal **princípio:** Inicie cada design de API com casos de uso de exemplo para garantir que as APIs sejam intuitivas de uso.

- ✅ **garantir** que cada componente de uma API pública tenha um caso de uso correspondente, em vez de tentar projetar para todos os usos possíveis desde o início.
    Em outras palavras, não introduza APIs públicas caso elas sejam úteis, mas certifique-se de que cada parte de uma API tenha um exemplo *concreto* no qual será útil.

  *Exemplos:*
  - @"microsoft.quantum.canon.applytoeachca" pode ser usado como `ApplyToEachCA(H, _)` para preparar os registros em um estado de superposição uniforme, uma tarefa comum em muitos algoritmos de Quantum. A mesma operação também pode ser usada para muitas outras tarefas nos algoritmos de preparação, numéricos e baseados em Oracle.

- ✅ **o** debate e o workshop novos designs de API para verificar se eles são intuitivos e atendem aos casos de uso propostos.

  *Exemplos:*
  - Inspecione o código de Q\# atual para ver como os novos designs de API podem simplificar e esclarecer as implementações existentes.
  - Examine os designs de API propostos com os representantes de públicos principais.

Principal **princípio:** Crie APIs para dar suporte e incentivar o código legível.

- ✅ **garantir** que o código seja legível por especialistas de domínio e não por especialistas.
- ✅ **fazer** o foco nos efeitos de cada operação e função dentro do algoritmo de alto nível, usando a documentação para se aprofundar nos detalhes da implementação, conforme apropriado.
- ✅ **siga** o guia de [estilo comum de Q\#](xref:microsoft.quantum.contributing.style) sempre que aplicável.

Principal **princípio:** Crie APIs para serem estáveis e forneça compatibilidade com o futuro.

- ✅ **substituir** APIs antigas normalmente quando alterações significativas forem necessárias.

- ✅ **fornecem** operações e funções de "Shim" que permitem que o código de usuário existente opere corretamente durante a substituição.

  *Exemplos:*
  - Ao renomear uma operação chamada `EstimateExpectation` para `EstimateAverage`, introduza uma nova operação chamada `EstimateExpectation` que chama a operação original em seu novo nome, para que o código existente possa continuar funcionando corretamente.

- ✅ **use** o atributo @"microsoft.quantum.core.deprecated" para comunicar as reprovações ao usuário.

- ✅ ao renomear uma operação ou função **, forneça** o novo nome como uma entrada de cadeia de caracteres para `@Deprecated`.

- ⛔️ **não** remover funções ou operações existentes sem um período de substituição de pelo menos seis meses para versões de visualização ou pelo menos dois anos para versões com suporte.

## <a name="functions-and-operations"></a>Funções e operações

Principal **princípio:** Verifique se cada função e operação tem uma única finalidade bem definida dentro da API.

- ⛔️ **não** expõem funções e operações que executam várias tarefas não relacionadas.

Principal **princípio:** projetar funções e operações para ser o mais reutilizável possível e prever necessidades futuras.

- ✅ **funções** e operações de design para compor bem com outras funções e operações, na mesma API e em bibliotecas existentes anteriormente.

  *Exemplos:*
  - A operação de @"microsoft.quantum.canon.delay" faz suposições mínimas sobre sua entrada e, portanto, pode ser usada para atrasar aplicativos de operações em toda a biblioteca padrão do Q # ou conforme definido pelos usuários.
    <!-- TODO: define bad example. -->

- ✅ **DO** expõem lógica clássica puramente determinística como funções em vez de operações.

  *Exemplos:*
  - Uma sub-rotina que quadrados sua entrada de ponto flutuante pode ser escrita de forma determinística e, portanto, deve ser exposta ao usuário como `Squared : Double -> Double` em vez de como uma operação `Square : Double => Double`. Isso permite que a sub-rotina seja chamada em mais lugares (por exemplo: dentro de outras funções) e fornece informações de otimização úteis para o compilador que podem afetar o desempenho e as otimizações.
  - `ForEach<'TInput, 'TOutput>('TInput => 'TOutput, 'TInput[]) => 'TOutput[]` e `Mapped<'TInput, 'TOutput>('TInput -> 'TOutput, 'TInput[]) -> 'TOutput[]` diferem nas garantias feitas em relação ao determinante; Ambos são úteis em diferentes circunstâncias.
  - Rotinas de API que transformam o aplicativo de operações Quantum geralmente podem ser executadas de maneira determinística e, portanto, podem ser disponibilizadas como funções como `CControlled<'T>(op : 'T => Unit) => ((Bool, 'T) => Unit)`.

- ✅ **DO** generalizar o tipo de entrada tanto quanto razoável para cada função e operação, usando parâmetros de tipo conforme necessário.

  *Exemplos:*
  - `ApplyToEach` tem o tipo `<'T>(('T => Unit), 'T[]) => Unit` em vez do tipo específico de seu aplicativo mais comum, `((Qubit => Unit), Qubit[]) => Unit`.

> [!TIP]
> É importante antecipar as necessidades futuras, mas também é importante resolver problemas concretos para seus usuários.
> Agir nesse princípio fundamental, portanto, sempre requer uma consideração cuidadosa e balanceamento para evitar o desenvolvimento de APIs "apenas no caso".

Principal **princípio:** escolha os tipos de entrada e saída para funções e operações que são previsíveis e que se comunicam com a finalidade de um callable.

- ✅ **usar** tipos de tupla para agrupar logicamente entradas e saídas que são significativas apenas quando consideradas juntas. Considere o uso de um tipo definido pelo usuário nesses casos.

  *Exemplos:*
  - Uma função para produzir a mínimo local de outra função pode precisar fazer limites de um intervalo de pesquisa como entrada, de modo que `LocalMinima(fn : (Double -> Double), (left : Double, right : Double)) : Double` pode ser uma assinatura apropriada.
  - Uma operação para estimar uma derivada de um classificador de aprendizado de máquina usando a técnica Shift de parâmetro pode precisar usar os vetores de parâmetro deslocados e não deslocados como entradas. Uma entrada semelhante à `(unshifted : Double[], shifted : Double[])` pode ser apropriada nesse caso.

- ✅ **DO** ordenar itens em tuplas de entrada e saída de forma consistente em diferentes funções e operações.

  *Exemplos:*
  - Se estiver considerando duas ou funções ou operações que cada uma pega um ângulo de rotação e um qubit de destino como entradas, certifique-se de que elas sejam ordenadas da mesma forma em cada tupla de entrada. Ou seja, prefira `ApplyRotation(angle : Double, target : Qubit) : Unit is Adj + Ctl` e `DelayedRotation(angle : Double, target : Qubit) : (Unit => Unit is Adj + Ctl)` a `ApplyRotation(target : Qubit, angle : Double) : Unit is Adj + Ctl` e `DelayedRotation(angle : Double, target : Qubit) : (Unit => Unit is Adj + Ctl)`.

Principal **princípio:** projetar funções e operações para funcionar bem com recursos de linguagem Q\# como aplicativos parciais.

- ✅ **os** itens de pedidos nas tuplas de entrada, de modo que as entradas mais aplicadas ocorrem primeiro (ou seja, para que o aplicativo parcial atue de forma semelhante ao currying).

  *Exemplos:*
  - Uma operação `ApplyRotation` que usa um número de ponto flutuante e um qubit como entradas geralmente pode ser parcialmente aplicada com a entrada de ponto flutuante primeiro para uso com operações que esperam uma entrada do tipo `Qubit => Unit`. Portanto, uma assinatura do `operation ApplyRotation(angle : Double, target : Qubit) : Unit is Adj + Ctl`
      funcionaria de forma mais consistente com o aplicativo parcial.
  - Normalmente, essas diretrizes significam colocar todos os dados clássicos antes de todos os qubits nas tuplas de entrada, mas usam bom julgamento e examinam como sua API é chamada na prática.

## <a name="user-defined-types"></a>Tipos definidos pelo usuário

Principal **princípio:** use tipos definidos pelo usuário para ajudar a tornar as APIs mais expressivas e convenientes de usar.

- ✅ **apresentar** novos tipos definidos pelo usuário para fornecer uma abreviação útil para tipos longos e/ou complicados.

  *Exemplos:*
  - Em casos em que um tipo de operação com três entradas de matriz qubit é normalmente usado como uma entrada ou retornado como uma saída, fornecendo um UDT como `newtype TimeDependentBlockEncoding = ((Qubit[], Qubit[], Qubit[]) => Unit is Adj + Ctl)`
      pode ajudar a fornecer uma abreviação útil.

- ✅ **apresentam** novos tipos definidos pelo usuário para indicar que um determinado tipo base deve ser usado apenas em um sentido muito específico.

  *Exemplos:*
  - Uma operação que deve ser interpretada especificamente como uma operação que codifica dados clássicos em um registro do Quantum pode ser apropriada para rotular com um tipo definido pelo usuário `newtype InputEncoder = (Apply : (Qubit[] => Unit))`.

- ✅ **apresentar** novos tipos definidos pelo usuário com itens nomeados que permitem a extensibilidade futura (por exemplo: uma estrutura de resultados que pode conter itens nomeados adicionais no futuro).

  *Exemplos:*
  - Quando uma operação `TrainModel` expõe um grande número de opções de configuração, expondo essas opções como um novo `TrainingOptions` UDT e fornecendo uma nova função `DefaultTrainingOptions : Unit -> TrainingOptions` permite que os usuários substituam itens nomeados específicos nos valores UDT de Trainoptions, enquanto ainda permite que os desenvolvedores de biblioteca adicionem novos itens UDT conforme apropriado.

- ✅ **declare** itens nomeados para novos tipos definidos pelo usuário em preferência para exigir que os usuários saibam a desconstrução correta da tupla.

  *Exemplos:*
  - Ao representar um número complexo em sua decomposição polar, prefira `newtype ComplexPolar = (Magnitude: Double, Argument: Double)` a `newtype ComplexPolar = (Double, Double)`.

Principal **princípio:** use tipos definidos pelo usuário de maneira a reduzir a carga cognitiva e que não exigem que o usuário Aprenda conceitos e nomenclatura adicionais.

- ⛔️ **não** Introduza tipos definidos pelo usuário que exijam que o usuário faça uso frequente do operador de desencapsulamento (`!`) ou que normalmente exijam vários níveis de desencapsulamento. As estratégias de mitigação possíveis incluem:

  - Ao expor um tipo definido pelo usuário com um único item, considere definir um nome para esse item. Por exemplo, considere `newtype Encoder = (Apply : (Qubit[] => Unit is Adj + Ctl))` preferencialmente para `newtype Encoder = (Qubit[] => Unit is Adj + Ctl)`.

  - Garantir que outras funções e operações possam aceitar as instâncias UDT "encapsuladas" diretamente.

- ⛔️ **não** Introduza novos tipos definidos pelo usuário que dupliquem tipos internos sem fornecer uma expressividade adicional.

  *Exemplos:*
  - Um `newtype QubitRegister = Qubit[]` UDT não fornece mais expressividade sobre `Qubit[]`e, portanto, é mais difícil de usar sem nenhum benefício discernido.
  - Um `newtype LittleEndian = Qubit[]` UDT documenta como o registro subjacente deve ser usado e interpretado e, portanto, fornece uma expressividade adicional sobre seu tipo base.

- ⛔️ **não** Introduza funções de acessador, a menos que seja estritamente necessário;   prefira fortemente os itens nomeados nesse caso.

  *Exemplos:*
  - Ao introduzir um `newtype Complex = (Double, Double)`UDT, prefira modificar a definição para `newtype Complex = (Real : Double, Imag : Double)` a fim de introduzir funções `GetReal : Complex -> Double` e `GetImag : Complex -> Double`.

## <a name="namespaces-and-organization"></a>Namespaces e organização

Principal **princípio:** escolha os nomes de namespace que são previsíveis e que informam claramente a finalidade de funções, operações e tipos definidos pelo usuário em cada namespace.

- ✅ **DO** namespaces de nome como `Publisher.Product.DomainArea`.

  *Exemplos:*
  - As funções, as operações e os UDTs publicados pela Microsoft como parte do recurso de simulação do quantum do kit de desenvolvimento do Quantum são colocados no namespace `Microsoft.Quantum.Simulation`.
  - `Microsoft.Quantum.Math` representa um namespace publicado pela Microsoft como parte do kit de desenvolvimento Quantum pertencente à área de domínio matemática.

- ✅ **fazer** operações, funções e tipos definidos pelo usuário usados para funcionalidade específica em um namespace que descreve essa funcionalidade, mesmo quando essa funcionalidade é usada em diferentes domínios de problema.

  *Exemplos:*
  - As APIs de preparação de estado publicadas pela Microsoft como parte do kit de desenvolvimento Quantum seriam colocadas em `Microsoft.Quantum.Preparation`.
  - As APIs de simulação do Quantum publicadas pela Microsoft como parte do kit de desenvolvimento Quantum seriam colocadas em `Microsoft.Quantum.Simulation`.

- ✅ **fazer** operações, funções e tipos definidos pelo usuário usados somente dentro de domínios específicos em namespaces que indicam seu domínio do utilitário. Se necessário, use subnamespaces para indicar tarefas focadas em cada namespace específico de domínio.

  *Exemplos:*
  - A biblioteca de Machine Learning da Quantum publicada pela Microsoft é amplamente colocada no namespace @"microsoft.quantum.machinelearning", mas os conjuntos de informações de exemplo são fornecidos pelo namespace @"microsoft.quantum.machinelearning.datasets".
  - As APIs de química do Quantum publicadas pela Microsoft como parte do kit de desenvolvimento Quantum devem ser colocadas em `Microsoft.Quantum.Chemistry`. A funcionalidade específica para implementar a Wigner da Jordânia pode ser colocada em `Microsoft.Quantum.Chemistry.JordanWigner`, de modo que a interface primária para a área de domínio do quantum química não se preocupa com as implementações.

Principal **princípio:** Use namespaces e modificadores de acesso juntos para ser intencional sobre a superfície de API exposta aos usuários e para ocultar detalhes internos relacionados à implementação e ao teste de suas APIs.

- ✅ sempre **que for razoável, coloque** todas as funções e operações necessárias para implementar uma API no mesmo namespace que a API que está sendo implementada, mas marcada com as palavras-chave "Private" ou "Internal" para indicar que elas não fazem parte da superfície da API pública para uma biblioteca. Use um nome que comece com um sublinhado (`_`) para distinguir visualmente operações e funções particulares e internas de chamadas públicas.

  *Exemplos:*
  - O nome da operação `_Features` indica uma função que é particular para um determinado namespace e assembly e deve ser acompanhado pela palavra-chave `internal`.

- ✅ **, no** caso raro, que um amplo conjunto de funções ou operações particulares seja necessário para implementar a API para um determinado namespace, coloque-as em um novo namespace correspondente ao namespace que está sendo implementado e terminando em `.Private`.

- ✅ **fazer** todos os testes de unidade em namespaces correspondentes ao namespace em teste e terminando em `.Tests`.

## <a name="naming-conventions-and-vocabulary"></a>Convenções de nomenclatura e vocabulário

Principal **princípio:** Escolha os nomes e a terminologia que são claros, acessíveis e legíveis em uma variedade diversificada de públicos, incluindo iniciantes e especialistas.

- ⛔️ **não** use nomes de identificador discriminados ou de exclusão, nem terminologia em comentários de documentação da API.

- ✅ **usar** comentários de documentação da API para fornecer contexto, exemplos e referências relevantes, especialmente para conceitos mais difíceis.

- ⛔️ **não** usam nomes de identificador desnecessariamente herméticos ou que exigem um conhecimento significativo de algoritmos Quantum para leitura.

  *Exemplos:*
  - Prefira "iteração de amplificação de amplitude" para "iteração Grover".

- ✅ **escolher** as operações e os nomes de função que comunicam claramente o efeito pretendido de uma callable, e não sua implementação. Observe que a implementação pode e deve ser

  *Exemplos:*
  - Prefira "estimar sobreposição" para "Hadamard Test", como a última se comunica como a primeira é implementada.

- ✅ **usar** palavras de maneira consistente em todas as APIs do p\#:

  - **Verbos**

    - **Assert**: Verifique se uma suposição sobre o estado de um computador de destino e seu qubits contém, possivelmente usando recursos não físicos. As operações que usam esse verbo devem ser sempre removíveis com segurança sem afetar a funcionalidade de bibliotecas e programas executáveis. Observe que, ao contrário dos fatos, as asserções podem, em geral, depender do estado externo, como o estado de um registro qubit, o ambiente de execução ou assim por diante. Como a dependência no estado externo é um tipo de efeito colateral, as asserções devem ser expostas como operações em vez de funções.

    - **Estimativa**: usando uma ou mais medidas possivelmente repetidas, estimar uma quantidade clássica dos resultados da medição.

      *Exemplos:*
      - @"microsoft.quantum.characterization.estimatefrequency"
      - @"microsoft.quantum.characterization.estimateoverlapbetweenstates"

    - **Prepare**: aplicar uma operação Quantum ou sequência de operações a um ou mais qubits presumidos para iniciar em um estado inicial específico (normalmente $ \ket{00\cdots 0} $), fazendo com que o estado dessas qubits seja evoluir para um estado final desejado. Em geral, agir em outros Estados que não seja o estado inicial especificado **pode** resultar em uma transformação unitário indefinida, mas ainda **deve** preservar essa operação e seu "cancelamento" adjacente e aplicar um não op.

      *Exemplos:*
      - @"microsoft.quantum.preparation.preparearbitrarystate"
      - @"microsoft.quantum.preparation.prepareuniformsuperposition"

    - **Medida**: aplique uma operação Quantum ou uma sequência de operações a um ou mais qubits, lendo os dados clássicos de volta.

      *Exemplos:*
      - @"microsoft.quantum.intrinsic.measure"
      - @"microsoft.quantum.arithmetic.measurefxp"
      - @"microsoft.quantum.arithmetic.measureinteger"

    - **Aplicar**: aplicar uma operação Quantum ou sequência de operações a um ou mais qubits, fazendo com que o estado dessas qubits seja alterado de maneira coerente. Esse verbo é o verbo mais geral em Q\# nomenclatura e **não deve ser** usado quando um verbo mais específico é mais diretamente relevante.

  - **Substantivos**:

    - **Fato**: uma condição booliana que depende apenas de suas entradas e não do estado de um computador de destino, seu ambiente ou o estado do qubits da máquina. Ao contrário de uma asserção, um fato só é sensível aos *valores* fornecidos a esse fato. Por exemplo:

      *Exemplos:*
      - @"microsoft.quantum.diagnostics.equalityfacti": representa um fato de igualdade sobre duas entradas de inteiro; os inteiros fornecidos como entrada são iguais, ou não são, independentemente de qualquer outro Estado de programa.

    - **Opções:** Um UDT que contém vários itens nomeados que podem atuar como "argumentos opcionais" para uma função ou operação. Por exemplo:

      *Exemplos:*
      - O @"microsoft.quantum.machinelearning.trainingoptions" UDT inclui itens nomeados para taxa de aprendizado, tamanho de minilote e outros parâmetros configuráveis para treinamento de ML.

  - **Adjetivos**:

    - ⛔️ **novo**: Esse adjetivo **não deve** ser usado, a fim de evitar confusão com seu uso como um verbo em muitas linguagens de programação ( C++por C#exemplo:,, Java, TypeScript, PowerShell).

  - **Preposições:** Em alguns casos, as preposições podem ser usadas para desambiguar ainda mais ou esclarecer as funções de substantivos e verbos em nomes de função e de operação. Deve-se ter cuidado para fazer isso de forma moderada e consistente.

    - **Como:** Representa que a entrada e a saída de uma função representam as mesmas informações, mas que a saída representa essas informações **como** um *X* em vez de sua representação original. Isso é especialmente comum para funções de conversão de tipo.

      *Exemplos:*
      - `IntAsDouble(2)` indica que a entrada (`2`) e a saída (`2.0`) representam qualitativomente as mesmas informações, mas usando diferentes tipos de dados de p\# para fazer isso.

    - **De:** Para garantir a consistência, essa preposição **não deve** ser usada para indicar funções de conversão de tipo ou qualquer outro **caso em que** for apropriado.

    - ⛔️ **para:** essa preposição **não deve** ser usada, a fim de evitar confusão com seu uso como um verbo em muitas linguagens de programação.
