---
title: Broombridge-esquema de química do Quantum
description: Visão geral do esquema Broombridge quantum química, usado para modelar problemas de química do mundo real com o Microsoft Quantum Development Kit.
author: martinro
ms.author: martinro@microsoft.com
ms.date: 10/17/2018
ms.topic: article
uid: microsoft.quantum.libraries.chemistry.schema.broombridge
ms.openlocfilehash: a746b63055bb1b2c1168b89993a7459ca9597f86
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907810"
---
# <a name="broombridge-quantum-chemistry-schema"></a>Esquema Broombridge quantum química # 

Um software robusto de química computacional, como o [NWChem](http://www.nwchem-sw.org/) , permite modelar uma ampla gama de problemas de química do mundo real. Para acessar os modelos do NWChem molecular com a biblioteca química do Microsoft Quantum, usamos um esquema baseado em [YAML](https://en.wikipedia.org/wiki/YAML)que chamamos de **Broombridge**. O nome foi escolhido em referência a um [ponto](https://en.wikipedia.org/wiki/Broom_Bridge) de entrada que, em alguns círculos, é comemorou como local de Hamiltonians. 

O [NWChem](https://github.com/nwchemgit/nwchem) é um projeto de software livre licenciado sob a licença de licença de comunidade educacional permissiva (ECL) 2,0. Broombridge é um esquema de software livre que é especificado [aqui](xref:microsoft.quantum.libraries.chemistry.schema.broombridge) e que vem com uma [definição](https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/broombridge-0.1.schema.json) após [RFC 2119](https://tools.ietf.org/html/rfc2119) e [script de validador](https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/validator.py) licenciados sob a licença MIT. 

Sendo baseado em YAML, o Broombridge é uma maneira estruturada, legível e humana, de representar problemas de estrutura eletrônica. Em particular, os dados a seguir podem ser representados: 
- Fermionic Hamiltonians pode ser representado usando integrals de um e dois. 
- Os Estados terrestre e empolgante podem ser apresentados usando sequências de criação.
- Os limites superiores e inferiores dos níveis de energia podem ser especificados.

O formato de dados pode ser gerado a partir de NWChem com facilidade sem esforço: há uma variedade de métodos disponíveis que variam de uma instalação completa do NWChem para executar baralhos de química, como os fornecidos [aqui](https://github.com/nwchemgit/nwchem/tree/master/QA/chem_library_tests) e saída Broombridge como parte da execução, em uma imagem do Docker de NWChem que também pode ser usada para gerar Broombridge de baralhos de química. Finalmente, um método Visual para começar com a química computacional rapidamente sem precisar instalar nenhum software de química é fornecido pela interface de [setas EMSL](https://arrows.emsl.pnnl.gov/api/qsharp_chem) para NWChem. 

Em um alto nível, a Interplay entre NWChem e a Microsoft Quantum Development Kit pode ser visualizada da seguinte maneira: ![pilha de química](~/media/broombridge.png) a caixa sombreada azul representa o esquema Broombridge, as várias caixas sombreadas de cinza representam outras representações de dados internas que foram escolhidas para representar e processar algoritmos Quantum para química computacional com base em problemas de química do mundo real. 

Várias representações químicas definidas usando o esquema Broombridge são fornecidas [aqui](https://github.com/microsoft/Quantum/tree/master/Chemistry/IntegralData/YAML).
