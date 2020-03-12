---
title: Esquema Broombridge quantum química
description: Visão geral do esquema Broombridge quantum química, usado para modelar problemas de química do mundo real com o Microsoft Quantum Development Kit.
author: martinro
ms.author: martinro@microsoft.com
ms.date: 10/17/2018
ms.topic: article
uid: microsoft.quantum.libraries.chemistry.schema.broombridge
ms.openlocfilehash: 708c4277080c358cb35a49fbf1dde0394d331043
ms.sourcegitcommit: d61b388651351e5abd4bfe7a672e88b84a6697f8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2020
ms.locfileid: "79022538"
---
# <a name="broombridge-quantum-chemistry-schema"></a>Esquema Broombridge quantum química # 

Um software robusto de química computacional, como o [NWChem](http://www.nwchem-sw.org/) , permite modelar uma ampla gama de problemas de química do mundo real. Para acessar modelos do NWChem molecular com a biblioteca do Microsoft quantum química, use um esquema baseado em [YAML](https://en.wikipedia.org/wiki/YAML)chamado **Broombridge**. O nome foi escolhido em referência a um [ponto](https://en.wikipedia.org/wiki/Broom_Bridge) de entrada que, em alguns círculos, é comemorou como local de Hamiltonians. 

O [NWChem](https://github.com/nwchemgit/nwchem) é um projeto de software livre licenciado sob a licença de licença de comunidade educacional permissiva (ECL) 2,0. O [esquema Broombridge quantum química](https://docs.microsoft.com/quantum/libraries/chemistry/schema/spec_v_0_2)) é um esquema de software livre que inclui uma [definição](https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/broombridge-0.1.schema.json) após [RFC 2119](https://tools.ietf.org/html/rfc2119) e um [script de validador](https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/validator.py) licenciado sob a licença MIT. 

Sendo baseado em YAML, o Broombridge é uma maneira estruturada, legível e humana, de representar problemas de estrutura eletrônica. Em particular, os dados a seguir podem ser representados:
- Fermionic Hamiltonians pode ser representado usando integrals de um e dois.
- Os Estados terrestre e empolgante podem ser apresentados usando sequências de criação.
- Os limites superiores e inferiores dos níveis de energia podem ser especificados.

Os dados podem ser gerados a partir de NWChem usando vários métodos, como o uso de uma instalação completa do NWChem para executar baralhos de química (por exemplo, aqueles fornecidos na [biblioteca NWChem](https://github.com/nwchemgit/nwchem/tree/master/QA/chem_library_tests) que geram Broombridge como parte da execução) ou uma imagem do Docker de NWChem que também pode ser usada para gerar Broombridge de baralhos de química. Para começar com o química computacional rapidamente sem precisar instalar nenhum software de química, você pode usar a interface visual para NWChem fornecida pelas [setas EMSL](https://arrows.emsl.pnnl.gov/api/qsharp_chem).

Em um alto nível, a Interplay entre NWChem e a Microsoft Quantum Development Kit pode ser visualizada da seguinte maneira: ![pilha de química](~/media/broombridge.png) a caixa sombreada azul representa o esquema Broombridge, as várias caixas sombreadas de cinza representam outras representações de dados internas que foram escolhidas para representar e processar algoritmos Quantum para química computacional com base em problemas de química do mundo real.

A pasta [integral/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML) no repositório de exemplos do kit de desenvolvimento do Quantum contém várias representações químicas definidas usando o esquema Broombridge.
