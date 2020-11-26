---
uid: Microsoft.Quantum.Preparation.PurifiedMixedState
title: Função PurifiedMixedState
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedState
qsharp.summary: "Returns an operation that prepares a a purification of a given mixed state.\rA \"purified mixed state\" refers to states of the form |ψ⟩ = Σᵢ √\U0001D45Dᵢ |\U0001D456⟩ |garbageᵢ⟩ specified by a vector of\rcoefficients {\U0001D45Dᵢ}. States of this form can be reduced to mixed states ρ ≔ \U0001D45Dᵢ |\U0001D456⟩⟨\U0001D456| by tracing over the \"garbage\"\rregister (that is, a mixed state that is diagonal in the computational basis).\r\rSee https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion."
ms.openlocfilehash: 73b031f1082d0a12975abad074b07184dcbabdbe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230014"
---
# <a name="purifiedmixedstate-function"></a>Função PurifiedMixedState

Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna uma operação que prepara um Purification de um determinado estado misto.
Um "estado misto de purified" refere-se aos Estados do formulário | ψ ⟩ = σi √ Pi | i ⟩ | lixoi ⟩ especificado por um vetor de coeficientes {PI}. Os Estados deste formulário podem ser reduzidos para Estados mistos ρ ≔ Pi | i ⟩ ⟨ i | rastreando o registro de "lixo" (ou seja, um estado misto que é diagonal na base computacional).

Consulte https://arxiv.org/pdf/1805.03662.pdf?page=15 para mais discussões.

```qsharp
function PurifiedMixedState (targetError : Double, coefficients : Double[]) : Microsoft.Quantum.Preparation.MixedStatePreparation
```


## <a name="description"></a>Descrição

Usa a técnica de ROM Quantum para representar uma determinada matriz de densidade, retornando essa representação como uma operação de preparação de estado.

Em particular, dada uma lista de $N $ coeficientes $ \ alpha_j $, essa função retorna uma operação que usa a técnica de ROM da Quantum para preparar uma aproximação $ $ \begin{align} \tilde\rho = \ sum_ {j = 0} ^ {N-1} p_j \ket{j}\bra{j} \end{align} $ $ do estado misto $ $ \begin{align} \rho = \ sum_ {j = 0} ^ {N-1} \ frac {| alpha_j |} {\ sum_k | \ alpha_k |} \ket{j}\bra{j}, \end{Align} $ $, em que cada $p _j $ é uma aproximação para o coeficiente determinado $ \ alpha_j $ de que $ $ \begin{align} \left | p_j-\frac{| \ alpha_j |} {\ sum_k | \ alpha_k |} \le \frac{\epsilon}{N} \end{align} $ $ para cada $j $.

Quando passou um registro de índice e um registro de qubits de lixo, inicialmente no estado $ \ket {0} \ket{00\cdots 0}, a operação retornada prepara ambos os registros para Purification de $ \tilde \rho $, $ $ \begin{align} \ sum_ {j = 0} ^ {N-1} \sqrt{p_j} \ket{j}\ket{\text{garbage} _J}, \end{align} $ $ para que a redefinição e desalocação do registro de lixo atue na preparação desejada para dentro do erro de destino $ \epsilon $.

## <a name="input"></a>Entrada

### <a name="targeterror--double"></a>targetError: [Double](xref:microsoft.quantum.lang-ref.double)

O erro de destino $ \epsilon $.


### <a name="coefficients--double"></a>coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]

Matriz de $N $ coeficientes especificando a probabilidade de Estados de base.
Números negativos $-\ alpha_j $ serão tratados como $ | \ alpha_j | $.



## <a name="output--mixedstatepreparation"></a>Saída: [MixedStatePreparation](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)

Uma operação que prepara $ \tilde \rho $ como um Purification para um índice conjunta e registro de lixo.

## <a name="remarks"></a>Comentários

Os coeficientes fornecidos a essa operação são normalizados seguindo a norma 1, de modo que os coeficientes são sempre considerados para descrever uma distribuição de probabilidade categórica válida.

## <a name="references"></a>Referências

- Codificação eletrônica de Spectra em circuitos Quantum com complexidade T linear Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru fosco, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Preparation. PurifiedMixedStateWithData](xref:Microsoft.Quantum.Preparation.PurifiedMixedStateWithData)