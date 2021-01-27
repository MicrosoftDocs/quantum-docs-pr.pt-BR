---
uid: Microsoft.Quantum.Preparation.PurifiedMixedStateWithData
title: Função PurifiedMixedStateWithData
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedStateWithData
qsharp.summary: "Returns an operation that prepares a a purification of a given mixed\rstate, entangled with a register representing a given collection of data.\rA \"purified mixed state with data\" refers to a state of the form Σᵢ √\U0001D45Dᵢ |\U0001D456⟩ |\U0001D465ᵢ⟩ |garbageᵢ⟩,\rwhere each \U0001D465ᵢ is a bitstring encoding additional data associated with the register |\U0001D456⟩.\r\rSee https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion."
ms.openlocfilehash: fc7bf8e6157af079ae4233ef45e67ce8ddfb8fe3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854289"
---
# <a name="purifiedmixedstatewithdata-function"></a>Função PurifiedMixedStateWithData

Namespace: [Microsoft. Quantum. preparação](xref:Microsoft.Quantum.Preparation)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retorna uma operação que prepara um Purification de um determinado estado misto, confusas com um registro que representa uma determinada coleção de dados.
Um "estado misto de purified com dados" refere-se a um estado do formulário σi √ Pi | i ⟩ | XI ⟩ | lixoi ⟩, em que cada XI é um bitstring de dados adicionais de codificação associados ao registro | i ⟩.

Consulte https://arxiv.org/pdf/1805.03662.pdf?page=15 para mais discussões.

```qsharp
function PurifiedMixedStateWithData (targetError : Double, coefficients : (Double, Bool[])[]) : Microsoft.Quantum.Preparation.MixedStatePreparation
```


## <a name="description"></a>Descrição

Usa a técnica de ROM Quantum para representar uma determinada matriz de densidade, retornando essa representação como uma operação de preparação de estado.

Em particular, dada uma lista de $N $ coeficientes $ \ alpha_j $ e um bitstring $ \vec{x}_j $ associado a cada coeficiente, essa função retorna uma operação que usa a técnica de ROM Quantum para preparar uma aproximação $ $ \begin{align} \tilde\rho = \sum_{j = 0} ^ {N-1} p_j \ket{j}\bra{j} \otimes \ket{\vec{x} _J} \bra{\vec{x}_j} \end{align} $ $ do estado misto $ $ \begin{align} \rho = \sum_{j = 0} ^ {N-1} \ frac {| alpha_j |} {\ sum_k | \ alpha_k |} \ket{j}\bra{j} \otimes \ket{\vec{x} _j} \bra{\vec{x} _j}, \end{Align} $ $, em que cada $p _j $ é uma aproximação para o coeficiente determinado $ \ alpha_j $ de que $ $ \begin{align} \left | p_j-\frac{| \ alpha_j |} {\ sum_k | \ alpha_k |} \le \frac{\epsilon}{N} \end{align} $ $ para cada $j $.

Quando passou um registro de índice e um registro de qubits de lixo, inicialmente no estado $ \ket {0} \ket{00\cdots 0}, a operação retornada prepara os registros para o Purification de $ \tilde \rho $, $ $ \begin{align} \ sum_ {j = 0} ^ {N-1} \sqrt{p_j} \ket{j} \ket{\vec{x} _J} \ket{\text{garbage} _J}, \end{align} $ $ para que a redefinição e desalocação do registro de lixo atue na preparação desejada para dentro do erro de destino $ \epsilon $.

## <a name="input"></a>Entrada

### <a name="targeterror--double"></a>targetError: [Double](xref:microsoft.quantum.lang-ref.double)

O erro de destino $ \epsilon $.


### <a name="coefficients--doublebool"></a>coeficientes: ([duplo](xref:microsoft.quantum.lang-ref.double),[bool](xref:microsoft.quantum.lang-ref.bool)[]) []

Matriz de $N $ coeficientes especificando a probabilidade de Estados de base, juntamente com o bitstring $ \vec{x} _j $ associado a cada coeficiente.
Números negativos $-\ alpha_j $ serão tratados como $ | \ alpha_j | $.



## <a name="output--mixedstatepreparation"></a>Saída: [MixedStatePreparation](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)

Uma operação que prepara $ \tilde \rho $ como um Purification para um índice conjunta e registro de lixo.

## <a name="remarks"></a>Comentários

Os coeficientes fornecidos a essa operação são normalizados seguindo a norma 1, de modo que os coeficientes são sempre considerados para descrever uma distribuição de probabilidade categórica válida.

## <a name="references"></a>Referências

- Codificação eletrônica de Spectra em circuitos Quantum com complexidade T linear Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru fosco, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Preparation. PurifiedMixedState](xref:Microsoft.Quantum.Preparation.PurifiedMixedState)