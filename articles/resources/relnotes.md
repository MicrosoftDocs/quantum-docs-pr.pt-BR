---
title: Notas sobre a versão do Quantum Development Kit
description: Saiba mais sobre as atualizações mais recentes da versão prévia do Microsoft Quantum Development Kit.
author: bradben
ms.author: v-benbra
ms.date: 8/30/2020
ms.topic: article
uid: microsoft.quantum.relnotes
no-loc:
- Q#
- $$v
ms.openlocfilehash: 5036b4d401bb775a7fee2252ca26e7725bc19004
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834135"
---
# <a name="microsoft-quantum-development-kit-release-notes"></a>Notas sobre a versão do Microsoft Quantum Development Kit

Este artigo contém informações sobre cada versão do Quantum Development Kit.

Para obter instruções de instalação, consulte o [guia de instalação](xref:microsoft.quantum.install).

Para obter instruções de atualização, consulte o [guia de atualização](xref:microsoft.quantum.update).

## <a name="version-01220082513"></a>0.12.20082513 da versão

*Data de lançamento: 25 de agosto de 2020*

Esta versão contém o seguinte:

- Novo [namespace Microsoft. Quantum. Random](xref:microsoft.quantum.random), fornecendo uma maneira mais conveniente de amostras de valores aleatórios de dentro de Q# programas. ([QuantumLibraries # 311](https://github.com/microsoft/QuantumLibraries/pull/311), [qsharp-Runtime # 328](https://github.com/microsoft/qsharp-runtime/pull/328))
- Melhor [namespace Microsoft. Quantum. Diagnostics](xref:microsoft.quantum.diagnostics) com nova [ `DumpOperation` operação](xref:microsoft.quantum.diagnostics.dumpoperation)e novas operações para restringir a alocação de qubit e as chamadas Oracle. ([QuantumLibraries # 302](https://github.com/microsoft/QuantumLibraries/pull/302))
- Novo [ `%project` comando mágico](xref:microsoft.quantum.iqsharp.magic-ref.project) em I Q# e [ `qsharp.projects` API](https://docs.microsoft.com/python/qsharp-core/qsharp.projects.projects) em Python para dar suporte a referências a Q# projetos fora da pasta do espaço de trabalho atual. Consulte [iqsharp # 277](https://github.com/microsoft/iqsharp/issues/277) para obter as limitações atuais desse recurso. 
- Suporte para carregamento automático `.csproj` de arquivos para Q# hosts/Python, que permite que referências a projetos ou pacotes externos sejam carregadas no momento da inicialização. Consulte o guia para uso [ Q# com notebooks Python e Jupyter](xref:microsoft.quantum.guide.host-programs) para obter mais detalhes.
- Exemplo adicionado ErrorCorrection. síndrome.
- Adicionado acoplamento ajustável ao SimpleIsing.
- Exemplo de HiddenShift atualizado.
- Exemplo adicionado para resolver o Sudoku com o algoritmo do Grover (contribuição externa)
- Correções de bugs gerais.

Consulte a lista completa de PRss fechadas para [bibliotecas](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compilador](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [tempo de execução](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [exemplos](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed), [I Q# ](https://github.com/microsoft/iqsharp/pulls?q=is%3Apr+is%3Aclosed) e [katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-01220072031"></a>0.12.20072031 da versão

*Data de lançamento: 21 de julho de 2020*

Esta versão contém o seguinte:

- Os namespaces abertos em Q# blocos de anotações agora estão disponíveis para todos os cálculos de células futuros. Isso permite, por exemplo, que os namespaces sejam abertos uma vez em uma célula na parte superior do notebook, em vez de precisarem abrir namespaces relevantes em cada célula de código. Um novo `%lsopen` comando mágico exibe a lista de namespaces abertos no momento.

Consulte a lista completa de PRss fechadas para [bibliotecas](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compilador](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [tempo de execução](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [exemplos](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed), [I Q# ](https://github.com/microsoft/iqsharp/pulls?q=is%3Apr+is%3Aclosed) e [katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-01220070124"></a>0.12.20070124 da versão

*Data de lançamento: 2 de julho de 2020*

Esta versão contém o seguinte:

- Nova `qdk-chem` ferramenta para converter formatos de serialização de problemas de estrutura eletrônica herdada (por exemplo: FCIDUMP) para [Broombridge](xref:microsoft.quantum.libraries.chemistry.schema.broombridge)
- Novas funções e operações no [`Microsoft.Quantum.Synthesis`](xref:microsoft.quantum.synthesis) namespace para aplicar de forma coerente as Oracle clássicas usando algoritmos de síntese baseados em transformação e descomposição.
- Agora, eu Q# permite argumentos para o `%simulate` , `%estimate` e outros comandos mágicos. Consulte a [ `%simulate` referência do comando mágico](xref:microsoft.quantum.iqsharp.magic-ref.simulate) para obter mais detalhes.
- Novas opções de exibição de fase em I Q# . Consulte a [ `%config` referência do comando mágico](xref:microsoft.quantum.iqsharp.magic-ref.config) para obter mais detalhes.
- I Q# e o `qsharp` pacote Python agora são fornecidos por meio de pacotes Conda ([qsharp](https://anaconda.org/quantum-engineering/qsharp) e [iqsharp](https://anaconda.org/quantum-engineering/iqsharp)) para simplificar a instalação local da Q# funcionalidade de Jupyter e Python em um ambiente Conda. Consulte os guias de instalação do [ Q# Jupyter notebooks](xref:microsoft.quantum.install.jupyter) e [ Q# com o Python](xref:microsoft.quantum.install.python) para obter mais detalhes.
- Ao usar o simulador, qubits não precisa mais estar no estado | 0 ⟩ na versão, mas pode ser redefinido automaticamente se eles forem medidos imediatamente antes da liberação.
- Atualizações para tornar mais fácil para Q# os usuários consumirem pacotes de biblioteca com diferentes versões de QDK, exigindo apenas os números de versão mais importantes &s correspondem, e não exatamente a mesma versão
- Namespace preterido removido `Microsoft.Quantum.Primitive.*`
- Operações movidas:
  - `Microsoft.Quantum.Intrinsic.Assert` agora é `Microsoft.Quantum.Diagnostics.AssertMeasurement`
  - `Microsoft.Quantum.Intrinsic.AssertProb` agora é `Microsoft.Quantum.Diagnostics.AssertMeasurementProbability`
- Correções de bug 

Consulte a lista completa de PRss fechadas para [bibliotecas](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compilador](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [tempo de execução](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [exemplos](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed), [I Q# ](https://github.com/microsoft/iqsharp/pulls?q=is%3Apr+is%3Aclosed) e [katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-0112006403"></a>Versão 0.11.2006.403

*Data de lançamento: 4 de junho de 2020*

Esta versão corrige um bug que afeta a compilação de Q# projetos.

## <a name="version-0112006207"></a>Versão 0.11.2006.207

*Data de lançamento: 3 de junho de 2020*

Esta versão contém o seguinte:

- Q# os notebooks e os programas de host do Python não falharão mais quando um Q# ponto de entrada estiver presente
- Atualizações para a [biblioteca padrão](xref:microsoft.quantum.libraries.standard.intro) para usar modificadores de acesso
- Agora, o compilador permite o plug-in de etapas de regravação entre as etapas de regravação internas
- Várias funções e operações preteridas foram removidas seguindo o agendamento descrito em nossos [Princípios de API](xref:microsoft.quantum.contributing.api-design). Q# os programas e as bibliotecas que criam sem avisos na versão 0.11.2004.2825 continuarão a funcionar de forma não modificada.

Consulte a lista completa de PRss fechadas para [bibliotecas](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compilador](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [tempo de execução](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [exemplos](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed), [I Q# ](https://github.com/microsoft/iqsharp/pulls?q=is%3Apr+is%3Aclosed) e [katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

> [!NOTE]
> Esta versão contém um bug que afeta a compilação de Q# projetos. É recomendável atualizar para uma versão mais recente.

## <a name="version-01120042825"></a>Versão 0.11.2004.2825

*Data de lançamento: 30 de abril de 2020*

Esta versão contém o seguinte:

- Novo suporte para Q# aplicativos, que não exigem mais um arquivo de host C# ou Python. Para obter mais informações sobre como começar a usar Q# aplicativos, consulte [aqui](xref:microsoft.quantum.install.standalone).
- Atualização do início rápido do gerador de número quântico aleatório para não exigir mais um arquivo host do C# ou Python. Confira o [Início Rápido](xref:microsoft.quantum.quickstarts.qrng) atualizado
- Melhorias de desempenho em Q# imagens do Docker

> [!NOTE]
> Q# os aplicativos que usam o novo [`@EntryPoint()`](xref:microsoft.quantum.core.entrypoint) atributo atualmente não podem ser chamados de programas de host do Python ou do .net.
> Confira os guias de [interoperabilidade do Python](xref:microsoft.quantum.install.python) e [do .NET](xref:microsoft.quantum.install.cs) para obter mais informações.

## <a name="version-01120033107"></a>Versão 0.11.2003.3107

*Data de lançamento: 31 de março de 2020*

Esta versão contém pequenas correções de bugs da versão 0.11.2003.2506.

## <a name="version-01120032506"></a>Versão 0.11.2003.2506

*Data de lançamento: 26 de março de 2020*

Esta versão contém o seguinte:

- Novo suporte para modificadores de acesso no Q# , para obter mais informações, consulte [estruturas de arquivo](xref:microsoft.quantum.guide.filestructure)
- Atualizado para SDK do .NET Core 3.1

Consulte a lista completa de PRs encerrados para [bibliotecas](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compilado](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [tempo de execução](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [amostras](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) e [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-01020022610"></a>Versão 0.10.2002.2610

*Data de lançamento: 27 de fevereiro de 2020*

Esta versão contém o seguinte:

- Nova biblioteca de Aprendizado de Máquina Quântico. Para obter mais informações, acesse nossa [página de documentos de QML](xref:microsoft.quantum.machine-learning.concepts.intro)
- Eu Q# correções de bugs, resultando em um aumento de desempenho de 10 20x ao carregar pacotes NuGet

Consulte a lista completa de PRs encerrados para [bibliotecas](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compilado](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [tempo de execução](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [amostras](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) e [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-01020012831"></a>Versão 0.10.2001.2831

*Data de lançamento: 29 de janeiro de 2020*

Esta versão contém o seguinte:

- Novo pacote NuGet Microsoft.Quantum.SDK, que substituirá o pacote Microsoft.Quantum.Development.Kit ao criar projetos. O pacote NuGet Microsoft.Quantum.Development.Kit continuará tendo suporte para projetos existentes. 
- Suporte para Q# extensões de compilador, habilitado pelo novo Microsoft. Quantum. SDK NuGet packge, para obter mais informações, consulte a [documentação no GitHub](https://github.com/microsoft/qsharp-compiler/tree/main/src/QuantumSdk#extending-the-q-compiler), o [exemplo de extensões de compilador](https://github.com/microsoft/qsharp-compiler/tree/main/examples/CompilerExtensions) e o blog de [ Q# desenvolvimento](https://devblogs.microsoft.com/qsharp/extending-the-q-compiler/)
- Suporte adicionado para o .NET Core 3.1. É altamente recomendável ter a versão 3.1.100 instalada, pois a criação com versões mais antigas do SDK do .NET Core pode causar problemas
- Novas transformações de compilador disponíveis em Microsoft.Quantum.QsCompiler.Experimental
- Nova funcionalidade para expor vetores de estado de saída como HTML em IQ#
- Adicionado suporte para EstimateFrequencyA para Microsoft.Quantum.Characterization para testes de SWAP e Hadamard
- O namespace AmplitudeAmplification agora usa o Q# Guia de estilo

Consulte a lista completa de PRs encerrados para [bibliotecas](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compilado](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [tempo de execução](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [amostras](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) e [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-01019120501"></a>Versão 0.10.1912.0501

*Data de lançamento: 5 de dezembro de 2019*

Esta versão contém o seguinte:

- Novo atributo de teste para Q# testes de unidade, consulte a documentação da API atualizada [aqui](https://docs.microsoft.com/qsharp/api/qsharp/microsoft.quantum.diagnostics.test) e os testes atualizados & guia de depuração [aqui](xref:microsoft.quantum.guide.testingdebugging)
- Rastreamento de pilha adicionado no caso de um Q# erro de execução do programa
- Compatibilidade com pontos de interrupção no Visual Studio Code devido a uma atualização na [extensão do Visual Studio Code em C# do OmniSharp](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp)

Consulte a lista completa de PRs encerrados para [bibliotecas](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compilado](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [tempo de execução](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [amostras](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) e [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-01019111607"></a>Versão 0.10.1911.1607

*Data de lançamento: 17 de novembro de 2019*

Esta versão contém o seguinte:

- Correção de desempenho para [Quantum katas](https://github.com/Microsoft/QuantumKatas) e Jupyter Notebooks

Consulte a lista completa de PRs encerrados para [bibliotecas](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compilado](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [tempo de execução](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [amostras](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) e [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  


## <a name="version-0101911307"></a>Versão 0.10.1911.307

*Data de lançamento: 1º de novembro de 2019*

Esta versão contém o seguinte:

- Atualizações para Visual Studio Code & as extensões do Visual Studio para implantar o servidor de idioma como um arquivo executável independente, eliminando a dependência de versão do SDK do .NET Core  
- Migração para o .NET Core 3.0
- Alteração significativa em Microsoft.Quantum.Simulation.Core.IOperationFactory com a introdução do novo método `Fail`. Ele afeta apenas simuladores personalizados que não estendem o SimulatorBase. Para obter mais detalhes, [exiba a solicitação de pull no GitHub](https://github.com/microsoft/qsharp-runtime/pull/59).
- Novo suporte para atributos preteridos

Consulte a lista completa de PRs encerrados para [bibliotecas](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compilado](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [tempo de execução](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [amostras](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) e [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-0919093002"></a>Versão 0.9.1909.3002

*Data de lançamento: 30 de setembro de 2019*

Esta versão contém o seguinte:

- Novo suporte para Q# conclusão de código no Visual Studio 2019 (versões 16,3 & posteriores) & Visual Studio Code
- Novo [Quantum Kata](https://github.com/Microsoft/QuantumKatas) para somadores de quantum

Consulte a lista completa de PRs encerrados para [bibliotecas](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compilado](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [tempo de execução](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [amostras](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) e [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-09-packagereference-0919082902"></a>Versão 0.9 (*PackageReference 0.9.1908.2902*)

*Data de lançamento: 29 de agosto de 2019*

Esta versão contém o seguinte:

- Novo suporte para [instruções de conjugação](xref:microsoft.quantum.guide.operationsfunctions#conjugations) em Q#
- Novas ações de código no compilador, como: "substituir por", "adicionar documentação" e uma atualização simples de item de matriz
- Adicionados modelo de instalação e novos comandos de projeto para a extensão do Visual Studio Code
- Adicionadas novas variantes do combinador ApplyIf, como [Microsoft.Quantum.Canon.ApplyIfOne](xref:microsoft.quantum.canon.applyifone)
- [Quantum Katas](https://github.com/Microsoft/QuantumKatas) adicional convertidos em Jupyter Notebooks
- A Extensão do Visual Studio agora requer o Visual Studio 2019

Consulte a lista completa de PRs encerrados para [bibliotecas](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compilado](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [tempo de execução](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [amostras](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) e [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

As alterações estão resumidas aqui, bem como instruções para atualizar seus programas existentes.  Leia mais sobre essas alterações no [ Q# blog de desenvolvimento](https://devblogs.microsoft.com/qsharp).

## <a name="version-08-packagereference-0819071701"></a>Versão 0.8 (*PackageReference 0.8.1907.1701*)

*Data de lançamento: 12 de julho de 2019*

Esta versão contém o seguinte:

- Novos locais de indexação para divisão de matrizes; [consulte a referência da linguagem](xref:microsoft.quantum.guide.expressions#array-slices) para obter mais informações.
- Adicionado Dockerfile hospedado no [registro de contêiner da Microsoft](https://github.com/microsoft/ContainerRegistry), consulte o [ Q# repositório I para obter mais informações](https://github.com/microsoft/iqsharp/blob/main/README.md)
- Alteração da falha no [simulador de rastreamento](xref:microsoft.quantum.machines.qc-trace-simulator.intro), atualização das definições de configuração, alterações de nome; consulte o [Navegador da API .NET para obter os nomes atualizados](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulatorconfiguration).

Consulte a lista de PRs encerrados para [bibliotecas](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) e [amostras](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-07-packagereference-0719053109"></a>Versão 0.7 (*PackageReference 0.7.1905.3109*)

*Data de lançamento: 31 de maio de 2019*

Esta versão contém o seguinte:
- adições ao Q# idioma, 
- atualizações da biblioteca de química, 
- uma nova biblioteca de numéricos.

Consulte a lista de PRs encerrados para [bibliotecas](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) e [amostras](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed).  

As alterações estão resumidas aqui, bem como instruções para atualizar seus programas existentes.  Leia mais sobre essas alterações no [ Q# blog de desenvolvimento](https://devblogs.microsoft.com/qsharp).

### <a name="no-locq-language-syntax"></a>Q# sintaxe da linguagem
Esta versão adiciona a nova Q# sintaxe de linguagem:
* Adição de itens nomeados para [tipos definidos pelo usuário](xref:microsoft.quantum.guide.types#user-defined-types).  
* Agora, os construtores de tipos definidos pelo usuário podem ser usados como funções.
* Adição de suporte para [copy-and-update](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) e [apply-and-reassign](xref:microsoft.quantum.guide.variables#rebinding-of-mutable-symbols) em tipos definidos pelo usuário.
* Agora, o bloco de correção para loops de [repeat-until-success](xref:microsoft.quantum.guide.controlflow#repeat-until-success-loop) é opcional.
* Agora, há suporte para loops em funções (não em operações).

### <a name="library"></a>Biblioteca 

Esta versão adiciona uma biblioteca numérica: Saiba mais sobre como [usar a nova biblioteca de numéricos](xref:microsoft.quantum.numerics.usage) e experimente os [novos exemplos](https://github.com/microsoft/quantum/tree/main/Numerics).  [PR #102](https://github.com/Microsoft/QuantumLibraries/pull/102).  

Essa versão reorganiza as extensões e atualizações da biblioteca de química:
* Melhora a modularidade de componentes, extensibilidade, limpeza de código geral.  [PR #58](https://github.com/microsoft/QuantumLibraries/pull/58).
* Adicionado suporte para [wavefunctions com várias referências](xref:microsoft.quantum.chemistry.concepts.multireference); wavefunctions com várias referências esparsas e cluster acoplado unitário.  [PR #110](https://github.com/Microsoft/QuantumLibraries/pull/110).
* (Obrigado!) [Colaborador de 1QBit](https://1qbit.com) ([@valentinS4t1qbit](https://github.com/ValentinS4t1qbit)): Avaliação de energia usando ansatz de variação. [PR #120](https://github.com/Microsoft/QuantumLibraries/pull/120).
* Atualizando o esquema [Broombridge](xref:microsoft.quantum.libraries.chemistry.schema.broombridge) para a nova [versão 0.2](xref:microsoft.quantum.libraries.chemistry.schema.spec_v_0_2), adicionando a especificação de cluster acoplado unitário. [Problema #65](https://github.com/microsoft/QuantumLibraries/issues/65).
* Adicionando interoperabilidade de Python a funções da biblioteca de química. Experimente esta [amostra](https://github.com/microsoft/Quantum/tree/main/Chemistry/PythonIntegration). [Problema #53](https://github.com/microsoft/QuantumLibraries/issues/53) [PR #110](https://github.com/Microsoft/QuantumLibraries/pull/110).

## <a name="version-061905"></a>Versão 0.6.1905

*Data de lançamento: 3 de maio de 2019*

Esta versão contém o seguinte:
- faz alterações no Q# idioma, 
- reestrutura as bibliotecas do Quantum Development Kit, 
- adiciona novas amostras e 
- corrige bugs.  Vários PRs encerrados para [bibliotecas](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) e [amostras](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed).  

As alterações estão resumidas aqui, bem como instruções para atualizar seus programas existentes.  Leia mais sobre essas alterações em devblogs.microsoft.com/qsharp.

### <a name="no-locq-language-syntax"></a>Q# sintaxe da linguagem
Esta versão adiciona a nova Q# sintaxe de linguagem:
* Adicionar uma [maneira abreviada de expressar especializações de operações quânticas](xref:microsoft.quantum.guide.operationsfunctions#controlled-and-adjoint-operations) (control e adjoints) com operadores `+`.  A sintaxe antiga foi preterida.  Os programas que usam a sintaxe antiga (por exemplo, `: adjoint`) continuarão funcionando, mas um aviso de tempo de compilação será gerado.  
* Adicionar um novo operador para [copy-and-update](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions); `w/` pode ser usado para expressar a criação da matriz como uma modificação de uma matriz existente.
* Adicionar a instrução comum [apply-and-update](xref:microsoft.quantum.guide.variables#rebinding-of-mutable-symbols), por exemplo, `+=`, `w/=`.
* Adicionar uma maneira de especificar um nome curto para namespaces em [diretivas abertas](xref:microsoft.quantum.guide.filestructure#open-directives).

Com esta versão, não permitimos mais que um elemento de matriz seja especificado no lado esquerdo de uma instrução SET.  Isso ocorre porque essa sintaxe implica que as matrizes são mutáveis quando, na verdade, o resultado da operação sempre foi a criação de uma nova matriz com a modificação.  Em vez disso, um erro do compilador será gerado com uma sugestão para usar o novo operador copy-and-update, `w/`, para chegar ao mesmo resultado.  

### <a name="library-restructuring"></a>Reestruturação de biblioteca
Esta versão reorganiza as bibliotecas para possibilitar seu crescimento de forma consistente:
* Renomeia o namespace Microsoft.Quantum.Primitive para Microsoft.Quantum.Intrinsic.  Essas operações são implementadas pelo computador de destino.  O namespace Microsoft.Quantum.Primitive foi preterido.  Um aviso de tempo de execução informará quando os programas chamarem operações e funções usando nomes preteridos.

* Renomeia o pacote Microsoft.Quantum.Canon para Microsoft.Quantum.Standard.  Esse pacote contém namespaces que são comuns à maioria dos Q# programas.  Isso inclui:  
    - Microsoft.Quantum.Canon para operações comuns
    - Microsoft. Quantum.Arithmetic para operações aritméticas de uso geral
    - Microsoft.Quantum.Preparation para operações usadas para preparar o estado do qubit
    - Microsoft.Quantum.Simulation para a funcionalidade de simulação

Com essa alteração, os programas que incluem uma única instrução "aberta" para o namespace Microsoft.Quatum.Canon poderão encontrar erros de build se o programa fizer referência a operações que foram movidas para os outros três novos namespaces.  Adicionar instruções abertas adicionais aos três novos namespaces é uma maneira simples de resolver esse problema.  

* Vários namespaces foram preteridos, pois as operações neles foram reorganizadas para outros namespaces. Os programas que usam esses namespaces continuarão funcionando e um aviso de tempo de compilação informará o namespace em que a operação está definida.  

* O namespace Microsoft.Quantum.Arithmetic foi normalizado para usar o tipo definido pelo usuário <xref:microsoft.quantum.arithmetic.littleendian>. Use a função [BigEndianAsLittleEndian](xref:microsoft.quantum.arithmetic.bigendianaslittleendian) quando necessário para converter para little endian.  

* Os nomes de vários chamadores (funções e operações) foram alterados para estar em conformidade com o [ Q# Guia de estilo](xref:microsoft.quantum.contributing.style).  Os nomes que podem ser chamados antigos foram preteridos.  Os programas que usam nomes que podem ser chamados antigos continuarão funcionando com um aviso de tempo de compilação. 

### <a name="new-samples"></a>Novas amostras

Adicionamos uma [amostra de uso do Q# com o driver F #](https://github.com/Microsoft/Quantum/pull/164).  

**Obrigado!** ao seguinte colaborador com nossa base de código aberto em http://github.com/Microsoft/Quantum. Essas contribuições são adicionadas significativamente aos avançados exemplos de Q# código:

* Mathias Soeken ([@msoeken](https://github.com/msoeken)): Síntese de função do Oracle. [PR #135](https://github.com/Microsoft/Quantum/pull/135).

### <a name="migrating-existing-projects-to-061905"></a>Migração de projetos existentes para 0.6.1905.

Consulte o [guia de instalação](xref:microsoft.quantum.install) para atualizar o QDK.
  
Se você tiver Q# projetos existentes da versão 0,5 do kit de desenvolvimento Quantum, veja a seguir as etapas para migrar esses projetos para a versão mais recente.

1. Os projetos precisam ser atualizados na ordem.  Se você tiver uma solução com vários projetos, atualize cada projeto na ordem em que eles são referenciados.
2. Em um prompt de comando, execute `dotnet clean` para remover todos os binários e arquivos intermediários existentes.
3. Em um editor de texto, edite o arquivo. csproj para alterar a versão de todos os `PackageReference` "Microsoft.Quantum" para a versão 0.6.1904 e altere o nome do pacote "Microsoft.Quantum.Canon" para "Microsoft.Quantum.Standard"; por exemplo:

    ```xml
    <PackageReference Include="Microsoft.Quantum.Standard" Version="0.6.1905.301" />
    <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.6.1905.301" />
    ```
4. No prompt de comando, execute este comando: `dotnet msbuild`  
5. Depois de executá-lo, talvez você ainda precise resolver os erros manualmente devido às alterações listadas acima.  Em muitos casos, esses erros também serão relatados pelo IntelliSense no Visual Studio ou Visual Studio Code.
    - Abra a pasta raiz do projeto ou a solução que o contém no Visual Studio 2019 ou o Visual Studio Code.
    - Depois de abrir um arquivo. QS no editor, você deverá ver a saída da Q# extensão de idioma na janela saída.
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

- Adiciona suporte para Jupyter Notebook, que oferece uma ótima maneira de aprender sobre o Q# .  [Confira as novas amostras de Jupyter Notebook e saiba como escrever seus próprios Notebooks](xref:microsoft.quantum.install). 

- Adiciona aritmética de somador de inteiros à biblioteca Quantum Canon.  Consulte também um Jupyter Notebook que [descreve como usar os novos somadores de inteiros](https://github.com/microsoft/Quantum/blob/main/samples/arithmetic/AdderExample.ipynb).

- Correção de bug para o problema com DumpRegister relatado pela Comunidade ([#148](https://github.com/Microsoft/Quantum/issues/148)).

- Adicionada a capacidade de retornar de dentro de uma [instrução using](xref:microsoft.quantum.guide.qubits#allocating-qubits).

- Remodelado o [guia de introdução](xref:microsoft.quantum.install).


## <a name="version-051902"></a>Versão 0.5.1902

*Data de lançamento: 27 de fevereiro de 2019*

Esta versão contém o seguinte:

- Adiciona suporte para um host Python de plataforma cruzada.  O `qsharp` pacote para Python torna mais fácil simular Q# operações e funções de dentro do Python. Saiba mais sobre a [interoperabilidade de Python](xref:microsoft.quantum.install). 

- As extensões do Visual Studio e do Visual Studio Code agora dão suporte à renomeação de símbolos (por exemplo, funções e operações).

- A extensão do Visual Studio agora pode ser instalada no Visual Studio 2019.

## <a name="version-041901"></a>Versão 0.4.1901

*Data de lançamento: 30 de janeiro de 2019*

Esta versão contém o seguinte:

- adiciona suporte para um novo tipo primitivo, BigInt, que representa um inteiro com sinal de tamanho arbitrário.  Saiba mais sobre o [tipo Bigint](xref:microsoft.quantum.guide.types).
- adicionar o novo simulador Toffoli, um simulador rápido com finalidade especial que pode simular operações quânticas X, CNOT e X com vários controlados com números muito grandes de qubits.  Saiba mais sobre o [simulador Toffoli](xref:microsoft.quantum.machines.toffoli-simulator).
- Adiciona um estimador de recursos simples que estima os recursos necessários para executar uma determinada instância de uma Q# operação em um computador Quantum.  Saiba mais sobre o [Estimador de recursos](xref:microsoft.quantum.machines.resources-estimator).


## <a name="version-0318112802"></a>Versão 0.3.1811.2802

*Data de lançamento: 28 de novembro de 2018*

Embora nossa extensão do VS Code não tenha sido usada, ela foi sinalizada e removida do marketplace durante [a limpeza de extensões](https://code.visualstudio.com/blogs/2018/11/26/event-stream) relacionada ao pacote `event-stream` do NPM. Essa versão remove todas as dependências de tempo de execução que podem fazer com que a extensão dispare qualquer sinalizador vermelho.

Se já tiver instalado a extensão, você precisará instalá-la novamente visitando a extensão do [Microsoft Quantum Development Kit para Visual Studio Code](vscode:extension/quantum.quantum-devkit-vscode) no Visual Studio Marketplace e pressionando instalar. Lamentamos pelo inconveniente.


## <a name="version-0318111511"></a>Versão 0.3.1811.1511

*Data de lançamento: 20 de novembro de 2018*

Esta versão corrige um bug que impedia alguns usuários de carregar com êxito a extensão do Visual Studio.

## <a name="version-031811203"></a>Versão 0.3.1811.203

*Data de lançamento: 2 de novembro de 2018*

Esta versão inclui algumas correções de bugs, incluindo:

* Invocar `DumpMachine` podia alterar o estado do simulador em determinadas situações.
* Avisos de compilação removidos ao compilar projetos usando uma versão do .NET Core anterior ao 2.1.403.
* Limpar a documentação, especialmente as dicas de ferramenta mostradas com o deslocamento do ponteiro do mouse no VS Code ou no Visual Studio.

## <a name="version-0318102508"></a>Versão 0.3.1810.2508

*Data de lançamento: 29 de outubro de 2018*

Esta versão inclui novos recursos de linguagem e uma experiência de desenvolvedor aprimorada:

* Esta versão inclui um servidor de linguagem para Q# o, bem como as integrações do cliente para Visual Studio e Visual Studio Code. Isso habilita um novo conjunto de recursos do IntelliSense, juntamente com feedback dinâmico no formato de sublinhados ondulados de erros e avisos. 
* Essa atualização melhora muito as mensagens de diagnóstico em geral, com navegação fácil e intervalos precisos de diagnósticos, e detalhes adicionais nas informações exibidas em foco.
* A Q# linguagem foi estendida de maneiras que unificam as maneiras como os desenvolvedores podem realizar operações comuns e novos aprimoramentos nos recursos de linguagem para expressar de forma eficiente a computação Quantum.  Há algumas alterações significativas no Q# idioma desta versão.   

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
* A documentação descreve como usar o NWChem para gerar modelos químicos adicionais para a simulação do Quantum com o Q# .

Saiba mais sobre a [biblioteca de química do Quantum Development Kit](xref:microsoft.quantum.chemistry.concepts.intro).

Com a nova biblioteca de química, estamos separando as bibliotecas em um novo repositório do GitHub, [Microsoft/QuantumLibraries](https://github.com/Microsoft/QuantumLibraries).  Os exemplos permanecem no repositório [Microsoft/Quantum](https://github.com/Microsoft/Quantum).  Contribuições são bem-vindas em ambos!

Esta versão inclui correções de bugs e recursos para problemas relatados pela Comunidade:

* IntelliSense para Q# ? ([UserVoice](https://quantum.uservoice.com/forums/906943/suggestions/32656918)).
* Arquivos .qs ([UserVoice](https://quantum.uservoice.com/forums/906097/suggestions/32593049)).
* Melhoria da mensagem de erro quando as chaves são abreviadas na instrução if ([UserVoice](https://quantum.uservoice.com/forums/906208/suggestions/34718518)).
* Suporte à desconstrução de tupla em (re-)associação mutável ([UserVoice](https://quantum.uservoice.com/forums/906208/suggestions/35020444)).
* Erro ao executar o BitFlipCode fornecido ([UserVoice](https://quantum.uservoice.com/forums/906940/suggestions/35008546)).
* H2SimulationGUI exibe grandes picos às vezes ([UserVoice](https://quantum.uservoice.com/forums/906946/suggestions/34668370)).

### <a name="community-contributions"></a>Contribuições da Comunidade

**Obrigado!** aos seguintes colaboradores com nossa base de código aberto em http://github.com/Microsoft/Quantum. Essas contribuições são adicionadas significativamente aos avançados exemplos de Q# código:

* Rolf Huisman ( [@RolfHuisman](https://github.com/RolfHuisman) ): melhorou a experiência para QASM/ Q# desenvolvedores criando um QASM para o Q# tradutor. [PR #58](https://github.com/Microsoft/Quantum/pull/58).

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

Esta é apenas uma correção rápida para o [problema #48 relatada no GitHub](https://github.com/Microsoft/Quantum/issues/48) ( Q# falha na compilação se o nome de usuário contiver um espaço em branco). Siga as mesmas instruções de atualização que `0.2.1806.1503` com a nova versão correspondente (`0.2.1806.3001-preview`).

## <a name="version-0218061503"></a>Versão 0.2.1806.1503

*Data de lançamento: 22 de junho de 2018*

Esta versão inclui várias contribuições da Comunidade, bem como uma experiência de depuração aprimorada e melhor desempenho.  Especificamente:

* melhorias de desempenho em simulações pequenas e grandes para o computador de destino QuantumSimulator.
* Aprimoramento da funcionalidade de depuração.
* Contribuições da Comunidade com correções de bugs, novas funções auxiliares, operações e novos exemplos.

### <a name="performance-improvements"></a>Melhorias de desempenho

Essa atualização inclui melhorias significativas de desempenho para a simulação de números grandes e pequenos de qubits para todos os computadores de destino.  Essa melhoria é facilmente visível com a simulação H<sub>2</sub> que é um exemplo padrão no Quantum Development Kit.

### <a name="improved-debugging-functionality"></a>Aprimoramento da funcionalidade de depuração

Esta atualização adiciona a nova funcionalidade de depuração:
* Foram adicionadas duas novas operações, @"microsoft.quantum.extensions.diagnostics.dumpmachine" e @"microsoft.quantum.extensions.diagnostics.dumpregister", que geram informações de função wave sobre o computador quântico de destino em um momento determinado.  
* No Visual Studio, a probabilidade de medir um $\ket{1}$ em um único qubit agora é mostrada automaticamente na janela de depuração do computador de destino de QuantumSimulator.
* No Visual Studio, melhorou a exibição de propriedades variáveis nas janelas de depuração **Automáticos** e **Locais**. 

Saiba mais sobre como [Testar e depurar](xref:microsoft.quantum.guide.testingdebugging).

### <a name="community-contributions"></a>Contribuições da Comunidade

A Q# comunidade codificadora está crescendo e estamos encantado coms a ver o primeiro usuário contribuído com as bibliotecas e exemplos que foram enviados à nossa base de código aberto em http://github.com/Microsoft/quantum .  **Muito obrigado!** aos seguintes colaboradores:
* Mathias Soeken ([@msoeken](https://github.com/msoeken)): contribuiu com um exemplo que define um método de síntese lógica baseado em transformação que constrói redes Toffoli para implementar uma determinada permutação. O código é escrito inteiramente em Q# funções e operações.  [PR #41](https://github.com/Microsoft/Quantum/pull/41).
* RolfHuisman ( [@RolfHuisman](https://github.com/RolfHuisman) ): Microsoft MVP Rolf Huisman contribuiu com um exemplo que gera código de QASM simples a partir do Q# código para uma classe restrita de programas que não têm fluxo de controle clássico e operações Quantum restritas. [PR #59](https://github.com/Microsoft/Quantum/pull/59)
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
1. Crie um novo projeto .NET Core usando o tipo correto de Q# modelo de projeto (aplicativo, biblioteca ou projeto de teste).
2. Copie os arquivos .qs e .cs/.fs existentes do projeto antigo para o novo projeto (usando Adicionar > Item Existente). Não copie o arquivo AssemblyInfo.cs.
3. Compile e execute o novo projeto.

Observe que a operação RandomWalkPhaseEstimation do namespace Microsoft.Quantum.Canon foi movida para o namespace Microsoft.Research.Quantum.RandomWalkPhaseEstimation no repositório [Microsoft/Quantum-NC](https://github.com/microsoft/quantum-nc).

### <a name="known-issues"></a>Problemas conhecidos

- A `--filter` opção para `dotnet test` não funciona corretamente para testes gravados no Q# .
  Como resultado, os testes de unidade individuais não podem ser executados no Visual Studio Code; é recomendável usar `dotnet test` no prompt de comando para executar novamente todos os testes.

## <a name="version-0118011707"></a>Versão 0.1.1801.1707

*Data de lançamento: 18 de janeiro de 2018*

Esta versão corrige alguns problemas relatados pela Comunidade. Especificamente:

- O simulador agora funciona com CPUs antigas não habilitadas para AVX.
- As configurações decimais regionais não farão com que o Q# analisador falhe.
- A operação primitiva `SignD` agora retorna `Int` em vez de `Double`.


## <a name="version-011712901"></a>Versão 0.1.1712.901

*Data de lançamento: 11 de dezembro de 2017*

### <a name="known-issues"></a>Problemas conhecidos

#### <a name="hardware-and-software-requirements"></a>Requisitos de hardware e software

- O simulador incluído no Quantum Development Kit requer uma instalação de 64 bits do Microsoft Windows para ser executado.
- O simulador quântico da Microsoft, instalado com o Quantum Development Kit, utiliza AVX (Advanced Vector Extensions) e requer uma CPU habilitada para AVX. Os processadores Intel fornecidos no primeiro trimestre de 2011 (Sandy Bridge) ou posteriores dão suporte a AVX. Estamos avaliando o suporte para CPUs anteriores e poderemos anunciar detalhes em um momento posterior.

#### <a name="project-creation"></a>Criação do projeto

- Ao criar uma solução (. sln) que será usada Q# , a solução deve ser um diretório maior do que cada projeto (. csproj) na solução. Ao criar uma nova solução, isso pode ser feito certificando-se de que a caixa de seleção "Criar diretório para a solução" esteja marcada na caixa de diálogo "Novo projeto". Se isso não for feito, os pacotes NuGet do Quantum Development Kit NuGet precisarão ser instalados manualmente.

#### Q#

- O IntelliSense não exibe erros adequados para o Q# código. Verifique se você está exibindo erros de compilação no Lista de Erros do Visual Studio para ver os erros corretos Q# . Observe também que os Q# erros não aparecerão até que você tenha feito uma compilação.
- Usar uma matriz mutável em um aplicativo parcial pode levar a um comportamento inesperado.
- Associar uma matriz imutável a uma matriz mutável (let a = b, em que b é uma matriz mutável) pode levar a um comportamento inesperado.
- A criação de perfil, a cobertura de código e outros plug-ins do VS nem sempre podem contar Q# linhas e blocos com precisão.
- O Q# compilador não valida cadeias de caracteres interpoladas. É possível criar erros de compilação em C# digitando incorretamente nomes de variáveis ou usando expressões em Q# cadeias de caracteres interpoladas.

#### <a name="simulation"></a>Simulação

- O Simulador de Quantum usa OpenMP para paralelizar a álgebra linear necessária. Por padrão, o OpenMP usa todos os threads de hardware disponíveis, o que significa que programas com pequenos números de qubits geralmente serão executados lentamente, pois a coordenação necessária reduzirá o trabalho real. Isso pode ser corrigido definindo a variável de ambiente OMP_NUM_THREADS como um número pequeno. Como uma regra prática muito ampla, 1 thread é adequado para até cerca de 4 qubits e, em seguida, 1 thread adicional por qubit é adequado, embora isso seja altamente dependente de seu algoritmo.

#### <a name="debugging"></a>Depuração

- F11 (Step in) não funciona no Q# código.
- O realce de código no Q# código em um ponto de interrupção ou uma pausa de etapa única, às vezes, é impreciso. A linha correta será realçada, mas às vezes o realce será iniciado e terminará em colunas incorretas na linha.

#### <a name="testing"></a>Testando

- Os testes devem ser executados no modo de 64 bits. Se os testes estiverem falhando com uma BadImageFormatException, vá para o menu de teste e selecione Configurações do Teste > Arquitetura do Processador Padrão > x64.
- Alguns testes levam muito tempo (possivelmente até 5 minutos, dependendo do seu computador) para serem executados. Isso é normal, pois alguns usam mais de 20 qubits; nosso maior teste é executado atualmente em 23 qubits.

#### <a name="samples"></a>Exemplos

- Em alguns computadores, algumas amostras pequenas podem ser executadas lentamente, a menos que a variável de ambiente OMP_NUM_THREADS esteja definida como "1". Consulte também a nota de versão em "Simulação".

#### <a name="libraries"></a>Bibliotecas

- Há uma suposição implícita de que qubits passados para uma operação em argumentos diferentes são todos distintos. Por exemplo, todas as operações de biblioteca (e todos os simuladores) pressupõem que os dois qubits passados para um NOT controlado sejam qubits diferentes. Violar essa pressuposição pode levar a resultados imprevisíveis. É possível testar isso usando o simulador de rastreamento de computação quântica.
- A função Microsoft.Quantum.Bind pode não funcionar conforme o esperado em todos os casos.
- No namespace Microsoft.Quantum.Extensions.Math, a função SignD retorna um Double em vez de um Int, embora a função System.Math.Sign subjacente sempre retorne um inteiro. É seguro comparar o resultado com relação a 1,0,-1,0 e 0,0, pois todos esses doubles têm representações binárias exatas.
