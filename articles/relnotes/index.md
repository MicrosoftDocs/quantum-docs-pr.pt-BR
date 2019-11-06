---
title: Notas sobre a versão prévia do Quantum Development Kit
description: Notas sobre a versão prévia do Quantum Development Kit
author: natke
ms.author: nakersha
ms.date: 09/30/2019
ms.topic: article
uid: microsoft.quantum.relnotes
ms.openlocfilehash: 868d256270516cf99c228a757a11c6dc1a6319df
ms.sourcegitcommit: c93fea5980d1d46fbda1e7c7153831b9337134bf
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2019
ms.locfileid: "73463327"
---
# <a name="microsoft-quantum-development-kit-release-notes"></a>Notas sobre a versão do Microsoft Quantum Development Kit

Este artigo contém informações sobre cada versão do Quantum Development Kit.

Para obter instruções de instalação, consulte o [guia de instalação](xref:microsoft.quantum.install).

Para obter instruções de atualização, consulte o [guia de atualização](xref:microsoft.quantum.update).

## <a name="version-0101911307"></a>Versão 0.10.1911.307

*Data de lançamento: 1º de novembro de 2019*

Esta versão contém o seguinte:

- Atualizações para Visual Studio Code e extensões do Visual Studio para implantar o servidor de linguagem como um executável independente, eliminando a dependência de versão do SDK do .NET Core  
- Migração para o .NET Core 3.0
- Alteração significativa em Microsoft.Quantum.Simulation.Core.IOperationFactory com a introdução do novo método `Fail`. Ele afeta apenas simuladores personalizados que não estendem o SimulatorBase. Para obter mais detalhes, [exiba a solicitação de pull no GitHub](https://github.com/microsoft/qsharp-runtime/pull/59).
- Novo suporte para atributos preteridos

Consulte a lista completa de PRs encerrados para [bibliotecas](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compilado](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [tempo de execução](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [amostras](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) e [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-0919093002"></a>Versão 0.9.1909.3002

*Data de lançamento: 30 de setembro de 2019*

Esta versão contém o seguinte:

- Novo suporte para preenchimento de código Q# no Visual Studio 2019 (versões 16.3 e posteriores) e no Visual Studio Code
- Novo [Quantum Kata](https://github.com/Microsoft/QuantumKatas) para somadores de quantum

Consulte a lista completa de PRs encerrados para [bibliotecas](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compilado](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [tempo de execução](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [amostras](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) e [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-09-packagereference-0919082902"></a>Versão 0.9 (*PackageReference 0.9.1908.2902*)

*Data de lançamento: 29 de agosto de 2019*

Esta versão contém o seguinte:

- Novo suporte para [instruções de conjugação](xref:microsoft.quantum.language.statements#conjugations) em Q#
- Novas ações de código no compilador, como: "substituir por", "adicionar documentação" e uma atualização simples de item de matriz
- Adicionados modelo de instalação e novos comandos de projeto para a extensão do Visual Studio Code
- Adicionadas novas variantes do combinador ApplyIf, como [Microsoft.Quantum.Canon.ApplyIfOne](xref:microsoft.quantum.canon.applyifone)
- [Quantum Katas](https://github.com/Microsoft/QuantumKatas) adicional convertidos em Jupyter Notebooks
- A Extensão do Visual Studio agora requer o Visual Studio 2019

Consulte a lista completa de PRs encerrados para [bibliotecas](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compilado](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [tempo de execução](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [amostras](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) e [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

As alterações estão resumidas aqui, bem como instruções para atualizar seus programas existentes.  Leia mais sobre essas alterações no [blog de desenvolvimento de Q#](https://devblogs.microsoft.com/qsharp).

## <a name="version-08-packagereference-0819071701"></a>Versão 0.8 (*PackageReference 0.8.1907.1701*)

*Data de lançamento: 12 de julho de 2019*

Esta versão contém o seguinte:

- Novos locais de indexação para divisão de matrizes; [consulte a referência da linguagem](xref:microsoft.quantum.language.expressions#array-slices) para obter mais informações.
- Adicionado Dockerfile hospedado no [Registro de Contêiner da Microsoft](https://github.com/microsoft/ContainerRegistry); consulte o [repositório IQ# para obter mais informações](https://github.com/microsoft/iqsharp/blob/master/README.md)
- Alteração da falha no [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro), atualização das definições de configuração, alterações de nome; consulte o [Navegador da API .NET para obter os nomes atualizados](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulatorconfiguration).

Consulte a lista de PRs encerrados para [bibliotecas](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) e [amostras](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-07-packagereference-0719053109"></a>Versão 0.7 (*PackageReference 0.7.1905.3109*)

*Data de lançamento: 31 de maio de 2019*

Esta versão contém o seguinte:
- adições à linguagem Q#, 
- atualizações da biblioteca de química, 
- uma nova biblioteca de numéricos.

Consulte a lista de PRs encerrados para [bibliotecas](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) e [amostras](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed).  

As alterações estão resumidas aqui, bem como instruções para atualizar seus programas existentes.  Leia mais sobre essas alterações no [blog de desenvolvimento de Q#](https://devblogs.microsoft.com/qsharp).

### <a name="q-language-syntax"></a>Sintaxe da linguagem Q#
Esta versão adiciona a nova sintaxe da linguagem Q#:
* Adição de itens nomeados para [tipos definidos pelo usuário](xref:microsoft.quantum.language.type-model#user-defined-types).  
* Agora, os construtores de tipos definidos pelo usuário podem ser usados como funções.
* Adição de suporte para [copy-and-update](xref:microsoft.quantum.language.expressions#copy-and-update-expressions) e [apply-and-reassign]((xref:microsoft.quantum.language.statements#rebinding-of-mutable-symbols)) em tipos definidos pelo usuário.
* Agora, o bloco de correção para loops de [repeat-until-success](xref:microsoft.quantum.language.statements#repeat-until-success-loop) é opcional.
* Agora, há suporte para loops em funções (não em operações).

### <a name="library"></a>Biblioteca 

Esta versão adiciona uma biblioteca numérica: Saiba mais sobre como [usar a nova biblioteca de numéricos](xref:microsoft.quantum.numerics.usage) e experimente os [novos exemplos](https://github.com/microsoft/quantum/tree/master/Numerics).  [PR #102](https://github.com/Microsoft/QuantumLibraries/pull/102).  

Essa versão reorganiza as extensões e atualizações da biblioteca de química:
* Melhora a modularidade de componentes, extensibilidade, limpeza de código geral.  [PR #58](https://github.com/microsoft/QuantumLibraries/pull/58).
* Adicionado suporte para [wavefunctions com várias referências](xref:microsoft.quantum.chemistry.concepts.multireference); wavefunctions com várias referências esparsas e cluster acoplado unitário.  [PR #110](https://github.com/Microsoft/QuantumLibraries/pull/110).
* (Obrigado!) [Colaborador de 1QBit](https://1qbit.com) ([@valentinS4t1qbit](https://github.com/ValentinS4t1qbit)): Avaliação de energia usando ansatz de variação. [PR #120](https://github.com/Microsoft/QuantumLibraries/pull/120).
* Atualizando o esquema [Broombridge](xref:microsoft.quantum.libraries.chemistry.schema.broombridge) para a nova [versão 0.2](xref:microsoft.quantum.libraries.chemistry.schema.spec_v_0_2), adicionando a especificação de cluster acoplado unitário. [Problema #65](https://github.com/microsoft/QuantumLibraries/issues/65).
* Adicionando interoperabilidade de Python a funções da biblioteca de química. Experimente esta [amostra](https://github.com/microsoft/Quantum/tree/master/Chemistry/PythonIntegration). [Problema #53](https://github.com/microsoft/QuantumLibraries/issues/53) [PR #110](https://github.com/Microsoft/QuantumLibraries/pull/110).

## <a name="version-061905"></a>Versão 0.6.1905

*Data de lançamento: 3 de maio de 2019*

Esta versão contém o seguinte:
- faz alterações na linguagem Q#, 
- reestrutura as bibliotecas do Quantum Development Kit, 
- adiciona novas amostras e 
- corrige bugs.  Vários PRs encerrados para [bibliotecas](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) e [amostras](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed).  

As alterações estão resumidas aqui, bem como instruções para atualizar seus programas existentes.  Leia mais sobre essas alterações em devblogs.microsoft.com/qsharp.

### <a name="q-language-syntax"></a>Sintaxe da linguagem Q#
Esta versão adiciona a nova sintaxe da linguagem Q#:
* Adicionar uma [maneira abreviada de expressar especializações de operações quânticas](xref:microsoft.quantum.language.type-model#functors) (control e adjoints) com operadores `+`.  A sintaxe antiga foi preterida.  Os programas que usam a sintaxe antiga (por exemplo, `: adjoint`) continuarão funcionando, mas um aviso de tempo de compilação será gerado.  
* Adicionar um novo operador para [copy-and-update](xref:microsoft.quantum.language.expressions#copy-and-update-expressions); `w/` pode ser usado para expressar a criação da matriz como uma modificação de uma matriz existente.
* Adicionar a instrução comum [apply-and-upate](xref:microsoft.quantum.language.statements#rebinding-of-mutable-symbols), por exemplo, `+=`, `w/=`.
* Adicionar uma maneira de especificar um nome curto para namespaces em [diretivas abertas](xref:microsoft.quantum.language.file-structure#open-directives).

Com esta versão, não permitimos mais que um elemento de matriz seja especificado no lado esquerdo de uma instrução SET.  Isso ocorre porque essa sintaxe implica que as matrizes são mutáveis quando, na verdade, o resultado da operação sempre foi a criação de uma nova matriz com a modificação.  Em vez disso, um erro do compilador será gerado com uma sugestão para usar o novo operador copy-and-update, `w/`, para chegar ao mesmo resultado.  

### <a name="library-restructuring"></a>Reestruturação de biblioteca
Esta versão reorganiza as bibliotecas para possibilitar seu crescimento de forma consistente:
* Renomeia o namespace Microsoft.Quantum.Primitive para Microsoft.Quantum.Intrinsic.  Essas operações são implementadas pelo computador de destino.  O namespace Microsoft.Quantum.Primitive foi preterido.  Um aviso de tempo de execução informará quando os programas chamarem operações e funções usando nomes preteridos.

* Renomeia o pacote Microsoft.Quantum.Canon para Microsoft.Quantum.Standard.  Este pacote contém namespaces comuns à maioria dos programas em Q#.  Isso inclui:  
    - Microsoft.Quantum.Canon para operações comuns
    - Microsoft. Quantum.Arithmetic para operações aritméticas de uso geral
    - Microsoft.Quantum.Preparation para operações usadas para preparar o estado do qubit
    - Microsoft.Quantum.Simulation para a funcionalidade de simulação

Com essa alteração, os programas que incluem uma única instrução "aberta" para o namespace Microsoft.Quatum.Canon poderão encontrar erros de build se o programa fizer referência a operações que foram movidas para os outros três novos namespaces.  Adicionar instruções abertas adicionais aos três novos namespaces é uma maneira simples de resolver esse problema.  

* Vários namespaces foram preteridos, pois as operações neles foram reorganizadas para outros namespaces. Os programas que usam esses namespaces continuarão funcionando e um aviso de tempo de compilação informará o namespace em que a operação está definida.  

* O namespace Microsoft.Quantum.Arithmetic foi normalizado para usar o tipo definido pelo usuário <xref:microsoft.quantum.arithmetic.littleendian>. Use a função [BigEndianAsLittleEndian](xref:microsoft.quantum.arithmetic.bigendianaslittleendian) quando necessário para converter para little endian.  

* Os nomes de vários chamadores (funções e operações) foram alterados para manter a conformidade com o [Guia de Estilo de Q#](xref:microsoft.quantum.contributing.style).  Os nomes que podem ser chamados antigos foram preteridos.  Os programas que usam nomes que podem ser chamados antigos continuarão funcionando com um aviso de tempo de compilação. 

### <a name="new-samples"></a>Novas amostras

Adicionamos uma [amostra de uso de Q$ com o driver de F#](https://github.com/Microsoft/Quantum/pull/164).  

**Obrigado!** ao seguinte colaborador com nossa base de código aberto em http://github.com/Microsoft/Quantum. Essas contribuições complementam significativamente os exemplos avançados de código Q#:

* Mathias Soeken ([@msoeken](https://github.com/msoeken)): Síntese de função do Oracle. [PR #135](https://github.com/Microsoft/Quantum/pull/135).

### <a name="migrating-existing-projects-to-061905"></a>Migração de projetos existentes para 0.6.1905.

Consulte o [guia de instalação](xref:microsoft.quantum.install) para atualizar o QDK.
  
Se você tiver projetos em Q# existentes na versão 0.5 do Quantum Development Kit, veja a seguir as etapas para migrar esses projetos para a versão mais recente.

    1. Os projetos precisam ser atualizados na ordem.  Se você tiver uma solução com vários projetos, atualize cada projeto na ordem em que eles são referenciados.
    2. Em uma linha de comando, execute `dotnet clean` para remover todos os arquivos intermediários e binários existentes.
    3. Em um editor de texto, edite o arquivo. csproj para alterar a versão de todos os `PackageReference` "Microsoft.Quantum" para a versão 0.6.1904 e altere o nome do pacote "Microsoft.Quantum.Canon" para "Microsoft.Quantum.Standard"; por exemplo:

         ```xml
        <PackageReference Include="Microsoft.Quantum.Standard" Version="0.6.1905.301" />
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.6.1905.301" />
        ```
    4. Na linha de comando, execute este comando: `dotnet msbuild`  
    5. Depois de executá-lo, talvez você ainda precise resolver os erros manualmente devido às alterações listadas acima.  Em muitos casos, esses erros também serão relatados pelo IntelliSense no Visual Studio ou Visual Studio Code.
        - Abra a pasta raiz do projeto ou a solução que o contém no Visual Studio 2019 ou o Visual Studio Code.
        - Depois de abrir um arquivo .qs no editor, você deverá ver a saída da extensão da linguagem Q# na janela de saída.
        - Depois que o projeto for carregado com êxito (indicado na janela de saída), abra cada arquivo manualmente para resolver todos os problemas restantes.

> [!NOTE]
> * Para a versão 0.6, o servidor de idiomas incluído com o Quantum Development Kit não dá suporte a vários workspaces.
> * Para trabalhar com um projeto no Visual Studio Code, abra a pasta raiz que contém o projeto em si e todos os projetos referenciados.   
> * Para trabalhar com uma solução no Visual Studio, todos os projetos contidos na solução precisam estar na mesma pasta que a solução ou em uma de suas subpastas.  
> * As referências entre projetos migrados para o 0.6 e superior e os projetos que usam versões mais antigas do pacote **não** têm suporte.

## <a name="version-051904"></a>Versão 0.5.1904

*Data de lançamento: 15 de abril de 2019*

Esta versão contém correções de bugs.


## <a name="version-051903"></a>Versão 0.5.1903

*Data de lançamento: 27 de março de 2019*

Esta versão contém o seguinte:

- Adiciona suporte para Jupyter Notebook, o que oferece uma ótima maneira de aprender sobre Q#.  [Confira as novas amostras de Jupyter Notebook e saiba como escrever seus próprios Notebooks](xref:microsoft.quantum.install). 

- Adiciona aritmética de somador de inteiros à biblioteca Quantum Canon.  Consulte também um Jupyter Notebook que [descreve como usar os novos somadores de inteiros](https://github.com/Microsoft/Quantum/blob/master/Samples/src/Arithmetic/Adder%20Example.ipynb).

- Correção de bug para o problema com DumpRegister relatado pela Comunidade ([#148](https://github.com/Microsoft/Quantum/issues/148)).

- Adicionada a capacidade de retornar de dentro de uma [instrução using](xref:microsoft.quantum.language.statements).

- Remodelado o [guia de introdução](xref:microsoft.quantum.install).


## <a name="version-051902"></a>Versão 0.5.1902

*Data de lançamento: 27 de fevereiro de 2019*

Esta versão contém o seguinte:

- Adiciona suporte para um host Python de plataforma cruzada.  O pacote `qsharp` para Python facilita a simulação de operações e funções de Q# em Python. Saiba mais sobre a [interoperabilidade de Python](xref:microsoft.quantum.install). 

- As extensões do Visual Studio e do Visual Studio Code agora dão suporte à renomeação de símbolos (por exemplo, funções e operações).

- A extensão do Visual Studio agora pode ser instalada no Visual Studio 2019.

## <a name="version-041901"></a>Versão 0.4.1901

*Data de lançamento: 30 de janeiro de 2019*

Esta versão contém o seguinte:

- adiciona suporte para um novo tipo primitivo, BigInt, que representa um inteiro com sinal de tamanho arbitrário.  Saiba mais sobre o [tipo Bigint](xref:microsoft.quantum.language.type-model).
- adicionar o novo simulador Toffoli, um simulador rápido com finalidade especial que pode simular operações quânticas X, CNOT e X com vários controlados com números muito grandes de qubits.  Saiba mais sobre o [simulador Toffoli](xref:microsoft.quantum.machines.toffoli-simulator).
- adiciona um estimador de recursos simples que estima os recursos necessários para executar uma determinada instância de uma operação em Q# em um computador quântico.  Saiba mais sobre o [Estimador de recursos](xref:microsoft.quantum.machines.resources-estimator).


## <a name="version-0318112802"></a>Versão 0.3.1811.2802

*Data de lançamento: 28 de novembro de 2018*

Embora nossa extensão do VS Code não tenha sido usada, ela foi sinalizada e removida do marketplace durante [a limpeza de extensões](https://code.visualstudio.com/blogs/2018/11/26/event-stream) relacionada ao pacote `event-stream` do NPM. Essa versão remove todas as dependências de tempo de execução que podem fazer com que a extensão dispare qualquer sinalizador vermelho.

Se já tiver instalado a extensão, você precisará instalá-la novamente visitando a extensão do [Microsoft Quantum Development Kit para Visual Studio Code](vscode:extension/quantum.quantum-devkit-vscode) no Visual Studio Marketplace e pressionando instalar. Lamentamos pelo inconveniente.


## <a name="version-0318111511"></a>Versão 0.3.1811.1511

*Data de lançamento: 20 de novembro de 2018*

Esta versão corrige um bug que impedia alguns usuários de carregar com êxito a extensão do Visual Studio.

Se estiver atualizando de uma versão 0.2 do Quantum Development Kit, saiba mais sobre as [alterações na linguagem Q# e sobre a migração de seu programa em Q#](xref:microsoft.quantum.relnotes.migration-0-3).

## <a name="version-031811203"></a>Versão 0.3.1811.203

*Data de lançamento: 2 de novembro de 2018*

Esta versão inclui algumas correções de bugs, incluindo:

* Invocar `DumpMachine` podia alterar o estado do simulador em determinadas situações.
* Avisos de compilação removidos ao compilar projetos usando uma versão do .NET Core anterior ao 2.1.403.
* Limpar a documentação, especialmente as dicas de ferramenta mostradas com o deslocamento do ponteiro do mouse no VS Code ou no Visual Studio.

Se estiver atualizando de uma versão 0.2 do Quantum Development Kit, saiba mais sobre as [alterações na linguagem Q# e sobre a migração de seu programa em Q#](xref:microsoft.quantum.relnotes.migration-0-3).

## <a name="version-0318102508"></a>Versão 0.3.1810.2508

*Data de lançamento: 29 de outubro de 2018*

Esta versão inclui novos recursos de linguagem e uma experiência de desenvolvedor aprimorada:

* Esta versão inclui um servidor de linguagem para Q#, bem como as integrações de cliente para o Visual Studio e o Visual Studio Code. Isso habilita um novo conjunto de recursos do IntelliSense, juntamente com feedback dinâmico no formato de sublinhados ondulados de erros e avisos. 
* Essa atualização melhora muito as mensagens de diagnóstico em geral, com navegação fácil e intervalos precisos de diagnósticos, e detalhes adicionais nas informações exibidas em foco.
* A linguagem Q# foi estendida de maneira a unificar as formas como os desenvolvedores podem realizar operações comuns e com novos aprimoramentos nos recursos de linguagem para expressar de forma eficiente a computação quântica.  Há algumas alterações de falha na linguagem Q# com esta versão.   

Saiba mais sobre as [alterações na linguagem Q# e a migração de seu programa em Q#](xref:microsoft.quantum.relnotes.migration-0-3).

Esta versão também inclui uma nova biblioteca de química quântica:

* A biblioteca de química contém novos recursos de simulação Hamiltoniana, incluindo:
    - integradores de Trotter-Suzuki de ordem uniforme arbitrária para melhorar a precisão da simulação.
    - Técnica de simulação de qubits com otimizações específicas da química para reduzir a complexidade de $T$-Gate.
* Um novo esquema de software livre, chamado de Esquema Broombridge (em referência a um [marco](https://en.wikipedia.org/wiki/Broom_Bridge) celebrado como o local de nascimento do Hamiltonianos) foi introduzido para importar representações de moléculas e simulá-las.
* São fornecidas várias representações químicas definidas usando o Esquema Broombridge.  Esses modelos foram gerados pelo [NWChem](http://www.nwchem-sw.org/), uma ferramenta de química computacional de alto desempenho de software livre.
* Tutoriais e amostras descrevem como usar a biblioteca de química e os modelos de dados de Broombridge para:
    - Construir Hamiltonianos simples usando a biblioteca de química
    - Visualizar as energias em estado fundamental e excitado do Hidreto de lítio usando a estimativa de fase.
    - Executar estimativas de recursos da simulação de química quântica.
    - Estimar os níveis de energia das moléculas representados pelo Esquema Broombridge.
* A documentação descreve como usar o NWChem para gerar modelos químicos adicionais para simulação quântica com Q#.

Saiba mais sobre a [biblioteca de química do Quantum Development Kit](xref:microsoft.quantum.chemistry.concepts.intro).

Com a nova biblioteca de química, estamos separando as bibliotecas em um novo repositório do GitHub, [Microsoft/QuantumLibraries](https://github.com/Microsoft/QuantumLibraries).  Os exemplos permanecem no repositório [Microsoft/Quantum](https://github.com/Microsoft/Quantum).  Contribuições são bem-vindas em ambos!

Esta versão inclui correções de bugs e recursos para problemas relatados pela Comunidade:

* Intellisense para Q#? ([UserVoice](https://quantum.uservoice.com/forums/906943/suggestions/32656918)).
* Arquivos .qs ([UserVoice](https://quantum.uservoice.com/forums/906097/suggestions/32593049)).
* Melhoria da mensagem de erro quando as chaves são abreviadas na instrução if ([UserVoice](https://quantum.uservoice.com/forums/906208/suggestions/34718518)).
* Suporte à desconstrução de tupla em (re-)associação mutável ([UserVoice](https://quantum.uservoice.com/forums/906208/suggestions/35020444)).
* Erro ao executar o BitFlipCode fornecido ([UserVoice](https://quantum.uservoice.com/forums/906940/suggestions/35008546)).
* H2SimulationGUI exibe grandes picos às vezes ([UserVoice](https://quantum.uservoice.com/forums/906946/suggestions/34668370)).

### <a name="community-contributions"></a>Contribuições da Comunidade

**Obrigado!** aos seguintes colaboradores com nossa base de código aberto em http://github.com/Microsoft/Quantum. Essas contribuições complementam significativamente os exemplos avançados de código Q#:

* Rolf Huisman ([@RolfHuisman](https://github.com/RolfHuisman)): melhorou a experiência para desenvolvedores de QASM/Q# criando um tradutor de QASM para Q#. [PR #58](https://github.com/Microsoft/Quantum/pull/58).

* Andrew Helwer ([@ahelwer](https://github.com/ahelwer)):  contribuiu com um exemplo que implementa o jogo CHSH, um jogo quântico relacionado à não localidade.  [PR #84](https://github.com/Microsoft/Quantum/pull/84).

Obrigado também a Rohit Gupta ([@guptarohit](https://github.com/guptarohit),[PR #90](https://github.com/Microsoft/quantum/pull/90)), Tanaka Takayoshi ([@tanaka-takayoshi](https://github.com/tanaka-takayoshi),[PR #289](https://github.com/MicrosoftDocs/quantum-docs-pr/pull/289)) e Lee James O'Riordan ([@mlxd](https://github.com/mlxd),[PR #96](https://github.com/Microsoft/Quantum/pull/96)) por seu trabalho para melhorar o conteúdo para todos nós por meio de correções de documentação, ortografia e digitação! 

## <a name="version-021809701"></a>Versão 0.2.1809.701

*Data de lançamento: 10 de setembro de 2018*

Esta versão inclui correções de bugs para problemas relatados pela Comunidade. Incluindo:

* Não é possível usar o operador SHIFT ([GitHub](https://github.com/Microsoft/Quantum/issues/75)).
* `DumpMachine` / `DumpRegister` falha em `QCTraceSimulator` ao imprimir no console ([UserVoice](https://quantum.uservoice.com/forums/906946/suggestions/34709680)).
* Permitir a alocação de 0 qubits ([UserVoice](https://quantum.uservoice.com/forums/906208-q-language/suggestions/34768069-allow-allocating-0-qubits)).
* `AssertQubitState` requer chamada Complex() explícita ([UserVoice](https://quantum.uservoice.com/forums/906208-q-language/suggestions/34713733-assertqubitstate-requires-explicit-complex-call)).
* A operação `Measure` sempre retorna `One` no macOS ([UserVoice](https://quantum.uservoice.com/forums/906940/suggestions/35008546)).

Obrigado! 

## <a name="version-0218063001"></a>Versão 0.2.1806.3001

*Data de lançamento: 30 de junho de 2018*

Este lançamento é apenas uma correção rápida do [problema #48 relatado no GitHub](https://github.com/Microsoft/Quantum/issues/48) (a compilação de Q # falhará se o nome de usuário contiver um espaço em branco). Siga as mesmas instruções de atualização que `0.2.1806.1503` com a nova versão correspondente (`0.2.1806.3001-preview`).

## <a name="version-0218061503"></a>Versão 0.2.1806.1503

*Data de lançamento: 22 de junho de 2018*

Esta versão inclui várias contribuições da Comunidade, bem como uma experiência de depuração aprimorada e melhor desempenho.  Especificamente:

* melhorias de desempenho em simulações pequenas e grandes para o computador de destino QuantumSimulator.
* Aprimoramento da funcionalidade de depuração.
* Contribuições da Comunidade com correções de bugs, novas funções auxiliares, operações e novos exemplos.

### <a name="performance-improvements"></a>Aprimoramentos de desempenho

Essa atualização inclui melhorias significativas de desempenho para a simulação de números grandes e pequenos de qubits para todos os computadores de destino.  Essa melhoria é facilmente visível com a simulação H<sub>2</sub> que é um exemplo padrão no Quantum Development Kit.

### <a name="improved-debugging-functionality"></a>Aprimoramento da funcionalidade de depuração

Esta atualização adiciona a nova funcionalidade de depuração:
* Foram adicionadas duas novas operações, @"microsoft.quantum.extensions.diagnostics.dumpmachine" e @"microsoft.quantum.extensions.diagnostics.dumpregister", que geram informações de função wave sobre o computador quântico de destino em um momento determinado.  
* No Visual Studio, a probabilidade de medir um $\ket{1}$ em um único qubit agora é mostrada automaticamente na janela de depuração do computador de destino de QuantumSimulator.
* No Visual Studio, melhorou a exibição de propriedades variáveis nas janelas de depuração **Automáticos** e **Locais**. 

Saiba mais sobre como [Testar e depurar](xref:microsoft.quantum.techniques.testing-and-debugging).

### <a name="community-contributions"></a>Contribuições da Comunidade

A Comunidade de codificação em Q# está crescendo e estamos muito felizes ao ver as primeiras bibliotecas e os exemplos contribuídos pelo usuário que foram enviados à nossa base de código aberto em http://github.com/Microsoft/quantum.  **Muito obrigado!** aos seguintes colaboradores:
* Mathias Soeken ([@msoeken](https://github.com/msoeken)): contribuiu com um exemplo que define um método de síntese lógica baseado em transformação que constrói redes Toffoli para implementar uma determinada permutação. O código é totalmente escrito em funções e operações de Q#.  [PR #41](https://github.com/Microsoft/Quantum/pull/41).
* RolfHuisman ([@RolfHuisman](https://github.com/RolfHuisman)): o Microsoft MVP Rolf Huisman contribuiu com um exemplo que gera código de QASM simples do código Q# para uma classe restrita de programas que não têm fluxo de controle clássico e operações quânticas restritas. [PR #59](https://github.com/Microsoft/Quantum/pull/59)
* Sarah Kasier ([@crazy4pi314](https://github.com/crazy4pi314)): ajudou a melhorar nossa base de código enviando uma função de biblioteca para operações controladas. [PR #53](https://github.com/Microsoft/Quantum/pull/53)
* Jessica Lemieux ([@Lemj3111](https://github.com/Lemj3111)): correção de @"microsoft.quantum.canon.quantumphaseestimation" e criação de novos testes de unidade.  [PR #54](https://github.com/Microsoft/Quantum/pull/54)
* Tama McGlinn ([@TamaHobbit](https://github.com/TamaHobbit)): limpou a amostra de Teleportação, certificando-se de que a instância de QuantumSimulator seja descartada. [PR #20](https://github.com/Microsoft/Quantum/pull/20)

Além disso, um grande **Obrigado!** a estes engenheiros de software da Microsoft da equipe de Serviços de Engenharia Comercial, que fizeram alterações valiosas em nossa documentação durante seu Hackathon.  Suas alterações aumentaram imensamente a clareza e melhoraram a experiência de integração para todos nós:
* Sascha Corti
* Mihaela Curmei
* John Donnelly
* Kirill Logachev
* Jan Pospisil
* Anita Ramanan
* Frances Tibble
* Alessandro Vozza

### <a name="update-existing-projects"></a>Atualizar projetos existentes

Esta versão é totalmente compatível com versões anteriores. Basta atualizar o pacotes do NuGet em seus projetos para a versão `0.2.1806.1503-preview` e fazer uma **recompilação completa** para garantir que todos os arquivos intermediários sejam regenerados.

No Visual Studio, siga as instruções normais sobre como [atualizar um pacote](https://docs.microsoft.com/nuget/tools/package-manager-ui#updating-a-package).

Para atualizar modelos de projeto para a linha de comando, execute o seguinte comando:
```
dotnet new -i "Microsoft.Quantum.ProjectTemplates::0.2.1806.1503-preview"
```

Depois de executar esse comando, todos os novos projetos criados usando `dotnet new <project-type> -lang Q#` usarão automaticamente esta versão do Quantum Development Kit.

Para atualizar um projeto existente para usar a versão mais recente, execute o seguinte comando de dentro do diretório para cada projeto:

```
dotnet add package Microsoft.Quantum.Development.Kit -v "0.2.1806.1503-preview"
dotnet add package Microsoft.Quantum.Canon -v "0.2.1806.1503-preview"
```

Se um projeto existente também usar a integração de XUnit para testes de unidade, um comando semelhante poderá ser usado para atualizar esse pacote também:
```
dotnet add package Microsoft.Quantum.Xunit -v "0.2.1806.1503-preview"
```

Dependendo da versão do XUnit que seu projeto de teste usa, talvez você também precise atualizar o XUnit para 2.3.1:
```
dotnet add package xunit -v "2.3.1" 
```

Após a atualização, certifique-se de remover todos os arquivos temporários gerados pela versão anterior, fazendo o seguinte:
```
dotnet clean 
```

### <a name="known-issues"></a>Problemas conhecidos

Não há problemas conhecidos adicionais a relatar.


## <a name="version-0218022202"></a>Versão 0.2.1802.2202

*Data de lançamento: 26 de fevereiro de 2018*

Esta versão dá suporte para desenvolvimento em mais plataformas, interoperabilidade de linguagem e aprimoramentos de desempenho. Especificamente:

- Suporte para desenvolvimento baseado em macOS e Linux. 
- Compatibilidade com o .NET Core, incluindo suporte para Visual Studio Code entre plataformas.
- Uma licença de software livre completa para as bibliotecas do Quantum Development Kit.
- Melhoria do desempenho do simulador em projetos que exigem 20 ou mais qubits.
- Interoperabilidade com a linguagem Python (versão prévia disponível no Windows).

### <a name="net-editions"></a>Edições de .NET

A plataforma .NET está disponível por meio de duas edições diferentes, o .NET Framework fornecido com o Windows e o .NET Core de software livre disponível no Windows, no macOS e no Linux.
Com esta versão, a maior parte do Quantum Development Kit é fornecida como bibliotecas para .NET Standard, o conjunto de classes comuns tanto à estrutura quanto ao núcleo.
Portanto, essas bibliotecas são compatíveis com as versões recentes do .NET Framework ou do .NET Core.

Sendo assim, para ajudar a garantir que os projetos escritos usando o Quantum Development Kit sejam os mais portáteis possíveis, recomendamos que os projetos de biblioteca escritos usando o Quantum Development Kit tenham como destino o .NET Standard, enquanto os aplicativos de console tenham como destino o .NET Core.
Como versões anteriores do Quantum Development Kit davam suporte apenas ao .NET Framework, talvez seja necessário migrar seus projetos existentes; consulte abaixo para obter detalhes de como fazer isso.

### <a name="project-migration"></a>Migração do projeto

Projetos criados com versões anteriores do Quantum Development Kit ainda funcionarão, desde que você não atualize os pacotes NuGet usados neles. Para migrar o código existente para a nova versão, execute as seguintes etapas:
1. Crie um novo projeto .NET Core usando o tipo correto de modelo de projeto Q# (Aplicativo, Biblioteca ou Projeto de Teste).
2. Copie os arquivos .qs e .cs/.fs existentes do projeto antigo para o novo projeto (usando Adicionar > Item Existente). Não copie o arquivo AssemblyInfo.cs.
3. Compile e execute o novo projeto.

Observe que a operação RandomWalkPhaseEstimation do namespace Microsoft.Quantum.Canon foi movida para o namespace Microsoft.Research.Quantum.RandomWalkPhaseEstimation no repositório [Microsoft/Quantum-NC](https://github.com/microsoft/quantum-nc).

### <a name="known-issues"></a>Problemas conhecidos

- A opção `--filter` para `dotnet test` não funciona corretamente para testes escritos em Q#.
  Como resultado, testes de unidade individuais não podem ser executados no Visual Studio Code; é recomendável usar `dotnet test` na linha de comando para executar novamente todos os testes.

## <a name="version-0118011707"></a>Versão 0.1.1801.1707

*Data de lançamento: 18 de janeiro de 2018*

Esta versão corrige alguns problemas relatados pela Comunidade. Especificamente:

- O simulador agora funciona com CPUs antigas não habilitadas para AVX.
- As configurações regionais de decimais não farão com que o analisador de Q# falhe.
- A operação primitiva `SignD` agora retorna `Int` em vez de `Double`.


## <a name="version-011712901"></a>Versão 0.1.1712.901

*Data de lançamento: 11 de dezembro de 2017*

### <a name="known-issues"></a>Problemas conhecidos

#### <a name="hardware-and-software-requirements"></a>Requisitos de hardware e software

- O simulador incluído no Quantum Development Kit requer uma instalação de 64 bits do Microsoft Windows para ser executado.
- O simulador quântico da Microsoft, instalado com o Quantum Development Kit, utiliza AVX (Advanced Vector Extensions) e requer uma CPU habilitada para AVX. Os processadores Intel fornecidos no primeiro trimestre de 2011 (Sandy Bridge) ou posteriores dão suporte a AVX. Estamos avaliando o suporte para CPUs anteriores e poderemos anunciar detalhes em um momento posterior.

#### <a name="project-creation"></a>Criação do projeto

- Ao criar uma solução (.sln) que usará Q#, a solução deve estar um diretório acima de cada projeto (.csproj) na solução. Ao criar uma nova solução, isso pode ser feito certificando-se de que a caixa de seleção "Criar diretório para a solução" esteja marcada na caixa de diálogo "Novo projeto". Se isso não for feito, os pacotes NuGet do Quantum Development Kit NuGet precisarão ser instalados manualmente.

#### <a name="q"></a>Q#

- O IntelliSense não exibe erros adequados para o código em Q#. Verifique se você está exibindo erros de build no Lista de Erros do Visual Studio para ver os erros corretos de Q#. Observe também que os erros de Q# não aparecerão até que você tenha feito um build.
- Usar uma matriz mutável em um aplicativo parcial pode levar a um comportamento inesperado.
- Associar uma matriz imutável a uma matriz mutável (let a = b, em que b é uma matriz mutável) pode levar a um comportamento inesperado.
- A criação de perfil, a cobertura de código e outros plug-ins do VS nem sempre podem contar as linhas e os blocos de Q# com precisão.
- O compilador de Q# não valida cadeias de caracteres interpoladas. É possível criar erros de compilação de C# digitando incorretamente nomes de variáveis ou usando expressões em cadeias de caracteres interpoladas em Q#.

#### <a name="simulation"></a>Simulação

- O Simulador de Quantum usa OpenMP para paralelizar a álgebra linear necessária. Por padrão, o OpenMP usa todos os threads de hardware disponíveis, o que significa que programas com pequenos números de qubits geralmente serão executados lentamente, pois a coordenação necessária reduzirá o trabalho real. Isso pode ser corrigido definindo a variável de ambiente OMP_NUM_THREADS como um número pequeno. Como uma regra prática muito ampla, 1 thread é adequado para até cerca de 4 qubits e, em seguida, 1 thread adicional por qubit é adequado, embora isso seja altamente dependente de seu algoritmo.

#### <a name="debugging"></a>Depurando

- F11 (step in) não funciona no código Q#.
- O realce de código em Q# em um ponto de interrupção ou pausa em uma única etapa é, às vezes, impreciso. A linha correta será realçada, mas às vezes o realce será iniciado e terminará em colunas incorretas na linha.

#### <a name="testing"></a>Testando

- Os testes devem ser executados no modo de 64 bits. Se os testes estiverem falhando com uma BadImageFormatException, vá para o menu de teste e selecione Configurações do Teste > Arquitetura do Processador Padrão > x64.
- Alguns testes levam muito tempo (possivelmente até 5 minutos, dependendo do seu computador) para serem executados. Isso é normal, pois alguns usam mais de 20 qubits; nosso maior teste é executado atualmente em 23 qubits.

#### <a name="samples"></a>Exemplos

- Em alguns computadores, algumas amostras pequenas podem ser executadas lentamente, a menos que a variável de ambiente OMP_NUM_THREADS esteja definida como "1". Consulte também a nota de versão em "Simulação".

#### <a name="libraries"></a>Bibliotecas

- Há uma suposição implícita de que qubits passados para uma operação em argumentos diferentes são todos distintos. Por exemplo, todas as operações de biblioteca (e todos os simuladores) pressupõem que os dois qubits passados para um NOT controlado sejam qubits diferentes. Violar essa pressuposição pode levar a resultados imprevisíveis. É possível testar isso usando o simulador de rastreamento de computação quântica.
- A função Microsoft.Quantum.Bind pode não funcionar conforme o esperado em todos os casos.
- No namespace Microsoft.Quantum.Extensions.Math, a função SignD retorna um Double em vez de um Int, embora a função System.Math.Sign subjacente sempre retorne um inteiro. É seguro comparar o resultado com relação a 1,0,-1,0 e 0,0, pois todos esses doubles têm representações binárias exatas.
