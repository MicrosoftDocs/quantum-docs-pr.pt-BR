---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced
title: Operação AssertOperationsEqualReferenced
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualReferenced
qsharp.summary: >-
  Given two operations, asserts that they act identically for all input states.

  This assertion is implemented by using the Choi–Jamiołkowski isomorphism to reduce the assertion to one of a qubit state assertion on two entangled registers. Thus, this operation needs only a single call to each operation being tested, but requires twice as many qubits to be allocated. This assertion can be used to ensure, for instance, that an optimized version of an operation acts identically to its naïve implementation, or that an operation which acts on a range of non-quantum inputs agrees with known cases.
ms.openlocfilehash: 045f00a720e9f4d2e6993c66ace44a81e192ff30
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853473"
---
# <a name="assertoperationsequalreferenced-operation"></a>Operação AssertOperationsEqualReferenced

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pacote: [Microsoft. Quantum. QSharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Dadas duas operações, afirma que elas agem de forma idêntica para todos os Estados de entrada.

Essa declaração é implementada usando o Choi – Jamiołkowski isomorphism para reduzir a asserção para uma de uma declaração de estado qubit em dois registros de confusas.
Portanto, essa operação precisa apenas de uma única chamada para cada operação que está sendo testada, mas requer duas vezes mais qubits a ser alocada.
Essa declaração pode ser usada para garantir, por exemplo, que uma versão otimizada de uma operação atue de forma idêntica à sua implementação ingênua ou que uma operação que atue em uma variedade de entradas não Quantum concorde com casos conhecidos.

```qsharp
operation AssertOperationsEqualReferenced (nQubits : Int, actual : (Qubit[] => Unit), expected : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a>Entrada

### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

Número de qubits a serem passadas para cada operação.


### <a name="actual--qubit--unit"></a>real: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit) de> 

Operação a ser testada.


### <a name="expected--qubit--unit--is-adj"></a>esperado: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] = [unidade](xref:microsoft.quantum.lang-ref.unit)  de> é adj

Operação que define o comportamento esperado para a operação em teste.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Esta operação requer que a operação que está modelando o comportamento esperado seja de modo adjacente, para que o inverso possa ser executado apenas no registro de destino.
Formalmente, é possível especificar uma operação de transpoção, o que ameniza esse requisito, mas a operação de transpoção não está em geral fisicamente realizable para operações Quantum arbitrárias e, portanto, não é incluída aqui como uma opção.