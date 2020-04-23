---
title: Q# técnicas - Juntando tudo
description: Passe por um programa básico q# que demonstre teletransporte quântico.
uid: microsoft.quantum.techniques.puttingittogether
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 4bd91699017e4c1acd9f4449b8a65e39bd07878e
ms.sourcegitcommit: b6b8459eb654040f1e19f66411b29fc9e48e95c9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2020
ms.locfileid: "82030558"
---
# <a name="putting-it-all-together-teleportation"></a>Colocando tudo junto: teletransporte #
Voltemos ao exemplo do circuito de teletransporte definido em [Circuitos Quânticos.](xref:microsoft.quantum.concepts.circuits) Vamos usar isso para ilustrar os conceitos que aprendemos até agora. Uma explicação do teletransporte quântico é fornecida abaixo para aqueles que não estão familiarizados com a teoria, seguido por um passo a passo da implementação do código em Q#. 

## <a name="quantum-teleportation-theory"></a>Teletransporte Quântico: Teoria
Teletransporte quântico é uma técnica para enviar um estado quântico desconhecido (que vamos nos referir como a '__mensagem__') de um qubit em um local para um qubit em outro local (vamos nos referir a esses qubits como '__aqui__' e '__lá__', respectivamente). Podemos representar nossa __mensagem__ como um vetor usando a notação Dirac: 

$$ \ket{\psi} = \alfa\ket{0} +{1} \beta\ket $$

O estado do qubit de __mensagem__ é desconhecido para nós, pois não sabemos os valores de $\alpha$ e $\beta$.

### <a name="step-1-create-an-entangled-state"></a>Passo 1: Criar um estado emaranhado
Para enviar a __mensagem__ precisamos que o qubit __aqui__ fique emaranhado com o qubit __lá.__ Isso é conseguido aplicando um portão Hadamard, seguido por um portão CNOT. Vamos ver a matemática por trás dessas operações do portal.

Vamos começar com os qubits __aqui__ e __ali__ ambos no estado de $ket{0}$ . Depois de envolver esses qubits, eles estão no estado:

$${1}\ket{\\phi^}= \frac {\sqrt{2}{00} }(\ket + \ket{11}) $$

### <a name="step-2-send-the-message"></a>Passo 2: Envie a mensagem
Para enviar a __mensagem__ primeiro aplicamos um portão CNOT com o qubit de __mensagem__ e __aqui__ qubit como entradas (o qubit da __mensagem__ é o controle e o qubit __aqui__ é o qubit de destino, neste caso). Este estado de entrada pode ser escrito:

$$ \ket{\psi}\ket{\phi^}={0} (\alfa\ket + \beta\ket{1})(\frac{1}{2}{\sqrt }(\ket{00} + \ket{11})) $$

Isso se expande para:

$$ \ket{\psi}\ket{\phi^}={2}\frac{\alpha}{\\sqrt{000} }\ket + \frac{\alpha}\\sqrt{2}}\ket{011} + \frac{\beta}{\sqrt{2}}\ket{100} + \frac{\beta}{\\\\\sqrt }\\\sqrt{2}}\ket{111} $$

Como lembrete, o portão CNOT vira o qubit de destino quando o qubit de controle é 1. Assim, por exemplo, uma entrada{000}de $\ket $ não resultará em nenhuma alteração, pois o primeiro qubit (o controle) é 0. No entanto, pegue um caso em que o primeiro qubit é 1 - por exemplo, uma entrada de $\ket{100}$. Neste caso, a saída é{110}$\ket $ como o segundo qubit (o alvo) é virado pelo portão CNOT.

Vamos agora considerar nossa saída uma vez que o portão CNOT tenha agido em nossa entrada acima. O resultado é:

{2}$$ \frac{\alpha}{\sqrt }\ket{000} + \frac{\alpha}\\sqrt{2}}\ket{011} + \frac{\beta}{\sqrt{2}}\ket{110} + \frac{\beta}\\sqrt{2}}\ket{101} $$

O próximo passo para enviar a __mensagem__ é aplicar um portão Hadamard ao qubit da __mensagem__ (esse é o primeiro qubit de cada termo). 

Como lembrete, o portão Hadamard faz o seguinte:

Entrada | Saída
---------------------------| ---------------------------------------------------------------
$\ket{0}$  | $\frac{1}{\sqrt{2}}(\ket{0} {1}+ \ket )$
$\ket{1}$  | $\frac{1}{\sqrt{2}}(\ket{0} {1}- \ket )$

Se aplicarmos o portão Hadamard ao primeiro qubit de cada termo de nossa produção acima, obtemos o seguinte resultado:

$$ \frac{\alpha}{\sqrt{2}}(\frac{1}{\sqrt{2}{0} }(\ket + \ket{1}))\ket{00} {2}+ \frac{\alfa}\\sqrt }(\frac{1}{\sqrt{11} {2}{1}{2}{0} {1}{10} {2}{1}{2}{0} {1}{01} {2}}(\ket{0} + \ket))\ket{1}+ \frac{\beta}{\\sqrt }(\frac {\sqrt }(\ket) \ket ))\ket + \frac{\beta}{\sqrt }(\frac {\sqrt }(\ket - \ket ))\ket $$

Observe que cada termo tem{1}dois fatores{2}$\frac {\sqrt }$$ . Podemos multiplicar estes dando o seguinte resultado:

$${2}\frac{\alfa} (\ket{0} {1}+ \ket )\ket{00} +{2}\frac{\alfa} (\ket{0} +{1}\ket )\ket{0} {1}{10} {2}{0} {1}{01} {11} + \frac{\beta}{2}(\ket - \ket )\ket + \frac{\beta} (\ket - \ket )\ket $$

O fator $\frac{1}{2}$ é comum a cada termo, então agora podemos levá-lo fora dos suportes:

{1}{2}$$ \frac \big[\alfa(\ket{0} {1}+ \ket )\ket{00} {0} + \alfa(\ket +{1}\ket{0} ){1}\ket{11} + \beta(\ket){1}\ket{10} + \beta(\ket-{0} \ket ) \ket \ket{01}\grande] $$

Podemos então multiplicar os suportes para cada termo dando:

$${1}{2}\frac \grande[\alfa\ket{000} +{100} \alfa\ket{011} + \alfa\ket +{111} \alfa\ket + \beta\ket{001} {101}{010} - \beta\ket{110} + \beta\ket - \beta\ket \grande] $$ $

### <a name="step-3-measure-the-result"></a>Passo 3: Meça o resultado

Devido a __aqui__ e __ali__ estar emaranhado, qualquer medida __aqui__ afetará o estado de __lá.__ Se medirmos o primeiro e o segundo qubit __(mensagem__ e __aqui)__ podemos saber em que estado __há,__ devido a essa propriedade de emaranhamento. 

* Se medirmos e conseguirmos um resultado 00, a superposição entra em colapso, deixando apenas termos consistentes com este resultado. Isso é $\alpha\ket{000} +\beta\ket{001}$. Isso pode ser refatorado{00}para $\ket (\alpha\ket{0} +\beta\ket{1})$. Portanto, se medirmos o primeiro e o segundo qubit a ser 00, sabemos que o{0} terceiro qubit,{1} __lá,__ está no estado $(\alfa\ket +\beta\ket )$.
* Se medirmos e conseguirmos um resultado 01, a superposição entra em colapso, deixando apenas termos consistentes com este resultado. Isso é $\alpha\ket{011} +\beta\ket{010}$. Isso pode ser refatorado{01}para $\ket (\alpha\ket{1} +\beta\ket{0})$. Portanto, se medirmos o primeiro e segundo qubit a ser 01, sabemos que o terceiro{1} qubit, __lá,__ está no estado $(\alfa\ket +\beta\ket{0})$.
* Se medirmos e conseguirmos um resultado 10, a superposição entra em colapso, deixando apenas termos consistentes com este resultado. Isso é $\alpha\ket{100} -\beta\ket{101}$. Isso pode ser refatorado{10}para $\ket (\alfa\ket{0} -\beta\ket{1})$. Portanto, se medirmos o primeiro e o segundo qubit para ser 10, sabemos que o{0} terceiro qubit,{1} __lá,__ está no estado $(\alfa\ket -\beta\ket )$.
* Se medirmos e conseguirmos um resultado 11, a superposição entra em colapso, deixando apenas termos consistentes com este resultado. Isso é $\alpha\ket{111} -\beta\ket{110}$. Isso pode ser refatorado{11}para $\ket (\alfa\ket{1} -\beta\ket{0})$. Portanto, se medirmos o primeiro e o segundo qubit para ser 11, sabemos que o{1} terceiro qubit,{0} __lá,__ está no estado $(\alfa\ket -\beta\ket )$.

### <a name="step-4-interpret-the-result"></a>Passo 4: Interprete o resultado

Como lembrete, a __mensagem__ original que queríamos enviar era:

$$ \ket{\psi} = \alfa\ket{0} +{1} \beta\ket $$

Precisamos colocar o qubit __lá__ neste estado, para que o estado recebido seja o que se pretendia. 

* Se medimos e obtivemos um resultado de 00, então o terceiro qubit,{0} __lá,__ está no estado $(\alfa\ket +\beta\ket{1})$. Como esta é a __mensagem pretendida,__ nenhuma alteração é necessária.
* Se medimos e obtivemos um resultado de 01, então o terceiro qubit,{1} __lá,__ está no estado $(\alfa\ket +\beta\ket{0})$. Isso difere da __mensagem__pretendida, no entanto, aplicar um portão{0} NOT nos dá{1}o estado desejado $(\alpha\ket +\beta\ket )$.
* Se medimos e obtivemos um resultado de 10, então o terceiro qubit,{0} __lá,__ está no estado $(\alfa\ket -\beta\ket{1})$. Isso difere da __mensagem__pretendida, no entanto, a aplicação de{0} um portão Z{1}nos dá o estado desejado $(\alpha\ket +\beta\ket )$.
* Se medimos e obtivemos um resultado de 11, então o terceiro qubit,{1} __lá,__ está no estado $(\alfa\ket -\beta\ket{0})$. Isso difere da __mensagem__pretendida, no entanto, aplicar um portão NOT seguido de{0} um portão{1}Z nos dá o estado desejado $(\alfa\ket +\beta\ket )$.

Resumindo, se medirmos e o primeiro qubit for 1, um portão Z é aplicado. Se medirmos e o segundo qubit for 1, um portão NOT será aplicado.

### <a name="summary"></a>Resumo
Mostrado abaixo é um circuito quântico de livro-texto que implementa o teletransporte. Movendo-se da esquerda para a direita você pode ver:
- Passo 1: Enroscando __aqui__ e __ali__ aplicando um portão Hadamard e portão CNOT.
- Passo 2: Enviar a __mensagem__ usando um portão CNOT e um portão Hadamard.
- Passo 3: Fazer uma medição do primeiro e segundo qubits, __mensagem__ e __aqui__.
- Passo 4: Aplicando um portão NOT ou um portão Z, dependendo do resultado da medição na etapa 3.

!['Teleporte(msg : Qubit, lá : Qubit) : Unidade'](~/media/teleportation.svg)

## <a name="quantum-teleportation-code"></a>Teletransporte Quântico: Código

Temos nosso circuito para teletransporte quântico:

!['Teleporte(msg : Qubit, lá : Qubit) : Unidade'](~/media/teleportation.svg)

Agora podemos traduzir cada um dos passos deste circuito quântico em Q#.

### <a name="step-0-definition"></a>Passo 0: Definição
Quando realizamos o teletransporte, devemos saber a __mensagem__ que desejamos enviar, e para onde desejamos enviá-la __(lá).__ Por essa razão, começamos definindo uma nova operação de Teleporte `msg` que `there`recebe dois qubits como argumentos, e :

```qsharp
operation Teleport(msg : Qubit, there : Qubit) : Unit {
```

Também precisamos alocar um `here` qubit que `using` oalcancemos com um bloco:

```qsharp
    using (here = Qubit()) {
```

### <a name="step-1-create-an-entangled-state"></a>Passo 1: Criar um estado emaranhado
Podemos então criar o par `here` `there` emaranhado entre @"microsoft.quantum.intrinsic.h" @"microsoft.quantum.intrinsic.cnot" e usando as operações e:

```qsharp
        H(here);
        CNOT(here, there);
```

### <a name="step-2-send-the-message"></a>Passo 2: Envie a mensagem
Em seguida, usamos os próximos $\operatorname{CNOT}$ e $H$ gates para mover nosso qubit de mensagem:

```qsharp
        CNOT(msg, here);
        H(msg);
```

### <a name="step-3--4-measuring-and-interpreting-the-result"></a>Passo 3 & 4: Medir e interpretar o resultado
Por fim, @"microsoft.quantum.intrinsic.m" utilizamos para realizar as medições e realizar as operações `if` de portão necessárias para obter o estado desejado, conforme denotado pelas declarações:

```qsharp
        // Measure out the entanglement
        if (M(msg) == One)  { Z(there); }
        if (M(here) == One) { X(there); }
```

### <a name="step-5-restarting-the-qubit-register"></a>Passo 5: Reiniciar o registro de qubit

No final de cada operação Q# precisamos deixar os qubits{0}no estado $\ket $. Podemos usar @"microsoft.quantum.intrinsic.reset" para reiniciar todos os qubits para o estado zero e isso vai terminar nossa operação.

```qsharp
        Reset(msg);
        Reset(here);
        Reset(there);
    }
}
```


