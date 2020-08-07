---
title: Instalação da biblioteca do Microsoft Q# química
description: Saiba como instalar a biblioteca química do Microsoft Quantum e usá-la com a plataforma química computacional NWChem.
author: guanghaolow
ms.author: gulow
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.chemistry.concepts.installation
no-loc:
- Q#
- $$v
ms.openlocfilehash: 5fe973d24ceffd413cdbd3c543013dcc7ee379c0
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869334"
---
# <a name="chemistry-library-installation"></a>Instalação da biblioteca do química

O [exemplo **MolecularHydrogen** ](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogen) usa os dados de entrada do molecular que são configurados manualmente.
Embora isso seja bom para pequenos exemplos, a quantum química em escala exige Hamiltonians com milhões ou bilhões de termos.
Esses Hamiltonians, gerados por pacotes de química computacional escalonáveis, são muito grandes para serem importados manualmente.

A biblioteca química do Quantum para o kit de desenvolvimento Quantum foi projetada para funcionar bem com pacotes químicas computacionais, mais notavelmente a plataforma [**NWChem**](http://www.nwchem-sw.org/) computacional química desenvolvida pelo EMSL (ambiente Molecular Sciences Environment) no laboratório nacional do noroeste do Pacífico.
Em particular, o [pacote **Microsoft. Quantum. química** ](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) fornece ferramentas para carregar instâncias de problemas de simulação de química do Quantum representados no [esquema Broombridge](xref:microsoft.quantum.libraries.chemistry.schema.broombridge), também com suporte para exportação por versões recentes do NWChem.

A biblioteca química do kit de desenvolvimento do Quantum também fornece uma ferramenta de linha de comando, `qdk-chem` , para conversão entre formatos herdados e [Broombridge](xref:microsoft.quantum.libraries.chemistry.schema.broombridge).

Esta seção fornece detalhes sobre como usar o kit de desenvolvimento Quantum com NWChem e Broombridge, ou formatos herdados e o `qdk-chem` .

## <a name="using-the-quantum-development-kit-with-nwchem"></a>Usando o kit de desenvolvimento Quantum com NWChem

Para começar a usar o NWChem junto com o kit de desenvolvimento Quantum, use um dos seguintes métodos:

- Comece a usar os arquivos Broombridge existentes fornecidos com os exemplos em [IntegralData/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML).
- Use o [Construtor de setas EMSL para o Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) que é um front-end baseado na Web para NWChem, para gerar novos arquivos de entrada molecular Broombridge.  
- Use a [imagem do Docker](https://hub.docker.com/r/nwchemorg/nwchem-qc/) fornecida pelo PNNL para executar NWChem ou
- [Compile o NWChem](http://www.nwchem-sw.org/index.php/Compiling_NWChem) para sua plataforma.

Consulte de [ponta a ponta com NWChem](xref:microsoft.quantum.chemistry.examples.endtoend) para obter mais informações sobre como trabalhar com o NWChem para modelos químicos para analisar com a biblioteca do Quantum Developer Kit química.

### <a name="getting-started-using-broombridge-files-provided-with-the-samples"></a>Introdução ao uso de arquivos Broombridge fornecidos com os exemplos

A pasta [IntegralData/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML) no repositório de exemplos do kit de desenvolvimento do Quantum contém arquivos de dados molécula com formato Broombridge.  

Como um exemplo simples, use o exemplo de biblioteca de química, [GetGateCount](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/GetGateCount) para carregar o Hamiltonian de um dos arquivos Broombridge e executar estimativas de portão de algorigthms de simulação de Quantum:

```bash
cd Quantum/Chemistry/GetGateCount
dotnet run -- --path=../IntegralData/YAML/h2.yaml --format=YAML
```

Consulte [carregando um Hamiltonian do arquivo](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) para obter mais informações sobre como inserir moléculas representado pelo esquema Broombridge.  

Confira [obtendo contagens de recursos](xref:microsoft.quantum.chemistry.examples.resourcecounts) para obter mais informações sobre a estimativa de recursos.  

### <a name="getting-started-using-the-emsl-arrows-builder"></a>Introdução ao uso do construtor de setas EMSL

EMSL Arrows é uma ferramenta que usa bancos de dados computacionais NWChem e químicas para gerar molécula.  [O EMSL Arrows Builder para o Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) permite que você insira seu modelo usando vários construtores de modelo molecular e gere o arquivo de configuração do Broombridge para ser usado pelo kit de desenvolvimento Quantum.  

Na página EMSL, clique na guia [' instuctions '] e siga as instruções [' exemplos simples '] para gerar arquivos Broombridge.  Em seguida, tente executar [' GetGateCount '] para ver as estimativas de recursos Quantum para esses moléculas.

### <a name="installing-nwchem-from-source"></a>Instalando o NWChem da origem

Instruções completas sobre como instalar o NWChem da origem [são fornecidas pelo PNNL](http://www.nwchem-sw.org/index.php/Compiling_NWChem).

> [!TIP]
> Se você quiser usar o NWChem do Windows 10, o subsistema do Windows para Linux é uma ótima opção.
> Depois de ter instalado o [Ubuntu 18, 4 LTS para Windows](https://www.microsoft.com/en-us/p/ubuntu-1804-lts/9n9tngvndl3q#activetab=pivot:overviewtab), execute `ubuntu18.04` do seu terminal favorito e siga as instruções acima para instalar o NWChem da origem.

Depois de compilar o NWChem da origem, você pode executar o `yaml_driver` script fornecido com NWChem para produzir rapidamente instâncias de Broombridge de baralhos de entrada NWChem:

```bash
$NWCHEM_TOP/contrib/quasar/yaml_driver input.nw
```

Esse comando criará um novo `input.yaml` arquivo no formato Broombridge dentro do diretório atual.

### <a name="using-nwchem-with-docker"></a>Usando o NWChem com o Docker

As imagens predefinidas para usar o NWChem estão disponíveis para a plataforma cruzada por meio do [Hub do Docker](https://hub.docker.com).
Para começar, siga as instruções de instalação do Docker para sua plataforma:

- [Instalar o Docker para Ubuntu](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
- [Instalar o Docker para macOS](https://docs.docker.com/docker-for-mac/install/)
- [Instalar o Docker for Windows 10](https://docs.docker.com/docker-for-windows/install/)

> [!TIP]
> Se estiver usando Docker for Windows, você precisará compartilhar a unidade que contém seu diretório temporário (normalmente, essa é a `C:\` unidade) com o daemon do Docker. Consulte a [documentação do Docker](https://docs.docker.com/docker-for-windows/#shared-drives) para obter mais detalhes.

Depois de instalar o Docker, você pode usar o módulo do PowerShell fornecido com os exemplos do kit de desenvolvimento do Quantum para executar a imagem ou pode executar a imagem manualmente.
Nós detalhamos o uso do PowerShell aqui; Se você quiser usar a imagem do Docker manualmente, consulte a [documentação fornecida com a imagem](https://hub.docker.com/r/nwchemorg/nwchem-qc/).

#### <a name="running-nwchem-through-powershell-core"></a>Executando o NWChem por meio do PowerShell Core

Para usar a imagem do Docker NWChem com o kit de desenvolvimento Quantum, fornecemos um pequeno módulo do PowerShell que lida com a movimentação de arquivos para dentro e fora do NWChem para você.
Se você ainda não tiver o PowerShell Core instalado, poderá baixá-lo entre plataformas do [repositório do PowerShell no GitHub](https://github.com/PowerShell/PowerShell#get-powershell).

> [!NOTE]
> O PowerShell Core também é usado para alguns exemplos para demonstrar a interoperabilidade com fluxos de trabalho de ciência de dados e análise de negócios.

Depois de instalar o PowerShell Core, importe `InvokeNWChem.psm1` para tornar os comandos do NWChem disponíveis na sessão atual:

```powershell
cd Quantum/utilities/
Import-Module ./InvokeNWChem.psm1
```

Isso tornará o `Convert-NWChemToBroombridge` comando disponível em sua sessão atual do PowerShell.
Para baixar todas as imagens necessárias do Docker e usá-las para executar os baralhos de entrada do NWChem e capturar a saída para Broombridge, execute o seguinte:

```powershell
Convert-NWChemToBroombridge ./input.nw
```

Isso criará um arquivo Broombridge executando NWChem em `input.nw` .
Por padrão, a saída Broombridge terá o mesmo nome e caminho que o baralho de entrada, com a `.nw` extensão substituída por `.yaml` .
Isso pode ser substituído usando o `-DestinationPath` parâmetro para `Convert-NWChemToBroombridge` .
Mais informações podem ser obtidas usando a funcionalidade interna de ajuda do PowerShell:

```powershell
Convert-NWChemToBroombridge -?
Get-Help Convert-NWChemToBroombridge -Full
```

## <a name="using-the-quantum-development-kit-with-qdk-chem"></a>Usando o kit de desenvolvimento Quantum com`qdk-chem`

Para instalar `qdk-chem` o, você pode usar o SDK do .NET Core na linha de comando:

```dotnetcli
dotnet tool install --global Microsoft.Quantum.Chemistry.Tools
```

Depois de instalar o `qdk-chem` , você pode usar a `--help` opção para obter mais detalhes sobre a funcionalidade oferecida pela `qdk-chem` ferramenta.

Para converter de e para Broombridge, você pode usar o `qdk-chem convert` comando:

```
qdk-chem convert --from fcidump --to broombridge data.fcidump --out data.yml
```

O `qdk-chem convert` comando também pode aceitar seus dados de entrada padrão e pode gravar na saída padrão; isso é especialmente útil em scripts e para integração com ferramentas que são exportadas para formatos herdados.
Por exemplo, no Bash:

```bash
cat data.fcidump | qdk-convert --from fcidump --to broombridge - > data.yml
```
