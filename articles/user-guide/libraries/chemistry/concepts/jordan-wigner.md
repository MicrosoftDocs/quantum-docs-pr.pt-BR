---
title: Representação de Jordan-Wigner
description: Saiba mais sobre a representação de Jordan-Wigner, que mapeia operadores de Hamiltonian para matrizes de unitários que podem ser implementadas mais facilmente em um computador Quantum.
author: bradben
ms.author: v-benbra
ms.date: 10/09/2017
ms.topic: conceptual
uid: microsoft.quantum.chemistry.concepts.jordanwigner
no-loc:
- Q#
- $$v
ms.openlocfilehash: 738c8262ea66b8a02ea7541e402953237dc2ea48
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844128"
---
# <a name="jordan-wigner-representation"></a>Representação de Jordan-Wigner

Embora o segundo Hamiltonians quantificado seja convenientemente representado em termos de $a ^ \dagger $ (criação) e $a $ (Annihilation), essas operações não são operações fundamentais em computadores Quantum.
Como resultado, se quisermos implementá-los em um computador Quantum, precisamos mapear os operadores para matrizes de unitários que podem ser implementadas em um computador Quantum.
A representação da Jordânia – Wigner fornece um desses mapas.
No entanto, outras pessoas como a representação Bravyi – Kitaev também existem e têm suas próprias vantagens e desvantagens relativas.
A principal vantagem da representação de Jordan-Wigner é sua simplicidade.

A representação de Jordan-Wigner é direta para derivar.
Lembre-se de que um estado $ \ket {0} _J $ implica que o spin orbital $j $ está vazio e $ \ket {1} _J $ indica que está ocupado.
Isso significa que o qubits pode, naturalmente, armazenar a ocupação de um determinado orbital de rotação.
Em seguida, temos isso $a ^ \ dagger_j \ket {0} _J = \ket {1} _J $ e $a ^ \ dagger_j \ket {1} _J = $0.
É fácil verificar se o \begin{align} a ^ \ dagger_j &= \begin{bmatrix}0 & 0 \\ \ 1 &0 \end{bmatrix} = \frac{X_j-iY_j} {2} , \nonumber \\ \\ a_j &= \begin{bmatrix}0 & 1 \\ \ 0 &0 \end{bmatrix} = \frac{X_j + iY_j} {2} , \end{align} em que $X _J $ e $Y _J $ são os operadores Pauli-$X $ e-$Y $ que atuam em qubit $j $.

>[!NOTE]
> No Q# estado $ \ket {0} $ representa o + 1 eigenstate do operador $Z $. Em algumas áreas de física $ \ket {0} $ representam o estado de aterramento de baixa energia e, portanto, a-1 eigenstate do operador $Z $. Portanto, algumas fórmulas podem ser diferentes da literatura popular.

Na biblioteca química, usamos $ \ket {0} $ para representar um orbital de rotação não ocupado.
Isso mostra que, para um único orbital de rotação, é fácil representar os operadores de criação e Annihilation em termos de matrizes de unitários que os computadores Quantum entendem.
Observe que, embora $X $ e $Y $ sejam unitários $a ^ \dagger $ e $a $ não são.
Veremos mais tarde que isso não representa um desafio para a simulação.

Um problema que resta é que, embora a construção acima funcione para um único orbital de rotação, ela falhará em sistemas com duas ou mais órbitas de rotação.
Como fermions são antisymmetic, sabemos que $a ^ \ dagger_j um ^ \ dagger_k =-a ^ \ dagger_k a ^ \ dagger_j $ para qualquer $j $ e $k $.
No entanto, $ $ \left (\frac{X_j-iY_j} {2} \right) \left (\frac{X_k-iY_k} {2} \right) = \left (\frac{X_k-iY_k} {2} \right) \left (\frac{X_j-iY_j} {2} \right).
$ $ Em outras palavras, os dois operadores de criação não realizam o anti-mudo conforme necessário.
Isso pode ser remediado, embora de maneira simples, se for inelegante.
A correção é observar que os operadores de Pauli naturalmente AntiAnti-mudo.
Em particular, $XZ =-ZX $ e $YZ =-ZY $.
Assim, ao intercalar $Z $ Operators na construção do operador, podemos emular a antimutação correta.
A construção completa é a seguinte: 

\begin{align} a ^ \ dagger_1 &= \left (\frac{X-iY} {2} \right) \otimes 1 \otimes 1 \otimes 1 \otimes \cdots \otimes 1, \\ \\ a ^ \ dagger_2 &= Z\otimes\left (\frac{X-iy} {2} \right) \otimes 1 \ OTimes 1 \otimes \cdots \otimes 1, \\ \\ um ^ \ dagger_3 &= Z\otimes Z\otimes \left (\frac{X-iy} {2} \right) \otimes 1 \otimes \cdots \otimes \vdots Z\otimes Z\otimes \\ \\ \\ \\ a ^ \ & dagger_N = Z\otimes \otimes \cdots Z \otimes Z\otimes \left (\frac{X-iy} \right {2} ). \label{EQ: JW} \end{align}

Também é conveniente expressar os operadores numéricos, $n _j $, em termos de operadores Pauli.
Felizmente, as cadeias de caracteres de $Z $ Operators (conhecidas como Jordan-Wigner cadeias de caracteres) cancelam depois de uma faz essa substituição.
Depois de fazer isso (e chamar esse $X _jY_j = iZ_j $), temos \begin{Equation} n_j = a ^ \ dagger_j a_j = \frac{(1-Z_j)} {2} .
\end{equation}


## <a name="constructing-hamiltonians-in-jordan-wigner-representation"></a>Construindo Hamiltonians na representação Jordan-Wigner

Depois que invocamos a representação de Jordan-Wigner traduzir o Hamiltonian para uma soma de operadores Pauli é direta.
Basta substituir cada um dos operadores $a ^ \dagger $ e $a $ no Hamiltonian Fermionic com as cadeias de caracteres Pauli-Operators fornecidos acima.
Quando um executa essa substituição, há apenas cinco classes de termos no Hamiltonian.
Essas cinco classes correspondem às diferentes maneiras pelas quais podemos escolher o $p, q $ e $p, q, r, s $ nos termos de um corpo e de dois corpo no Hamiltonian.
Essas cinco classes, para o caso em que $p>q>r>s $ e órbitas com valor real, são

\begin{align} h_ {PP} a_p ^ \dagger a_p &= \ sum_p \frac{h_ {PP}} {2} (1-Z_p) \\ \\ h_ {pq} (a_p ^ \dagger a_q + a ^ \ dagger_q a_p) &= \frac{h_ {pq}} {2} \left (\ prod_ {j = q + 1} ^ {p-1} Z_j \right) \left (X_pX_q + Y_pY_q \right) \\ \\ h_ {pqqp} n_p n_q &= \frac{h_ {pqqp}} {4} \left (1-Z_p-Z_q + Z_pZ_q \right) \\ \\ H_ {pqqr} &= \frac{h_ {pqqr}} {2} \left (\ prod_ {j = r + 1} ^ {p-1} Z_j \right) \left (X_pX_r + Y_pY_r \right) \left (\frac{1-Z_q} {2} \right) \\ \\ H_ {PQRS} &= \frac{h_ {PQRS}} {8} \ prod_ {j = s + 1} ^ {r-1} Z_j \ prod_ {k = q + 1} ^ {p-1} Z_k \Big (XXXX-XXYY + XYXY\nonumber \\ \\ & \qquad\qquad\qquad\qquad\qquad + YXXY + YXYX-YYXX\nonumber \\ \\ & \qquad\qquad\qquad\qquad\qquad + XYYX + YYYY\Big) \end{align}

Embora gerar tal Hamiltonians manualmente exija a aplicação dessas regras de substituição, isso seria inviável para grandes moléculas, o que pode consistir em milhões de Hamiltonian termos.
Como alternativa, podemos construir automaticamente a `JordanWignerEncoding` `FermionHamiltonian` representação determinada da Hamiltonian.

```csharp
    // We load the namespace containing fermion and Pauli objects. 
    using Microsoft.Quantum.Chemistry.Fermion;
    using Microsoft.Quantum.Chemistry.Pauli;
    
    // We create an example `FermionHamiltonian` instance.
    var fermionHamiltonian = new FermionHamiltonian();

    // We convert this Fermion Hamiltonian to a Jordan-Wigner representation.
    var jordanWignerEncoding = fermionHamiltonian.ToPauliHamiltonian(QubitEncoding.JordanWigner);
```

Depois que os Hamiltonians são construídos neste formulário, podemos usar um host de algoritmos de simulação de Quantum para compilar o Dynamics gerado por $e ^ {-iHt} $ em uma sequência de Gates elementares (dentro de uma tolerância de erros definíveis pelo usuário).
Discutimos os dois métodos mais populares para a simulação de Quantum, as fórmulas qubitization e Trotter – Suzuki, na documentação do Algorithm. Fornecemos implementações para ambos os métodos na biblioteca de simulação de Hamiltonian.
