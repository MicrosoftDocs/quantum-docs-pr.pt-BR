---
uid: Microsoft.Quantum.Canon.ApproximatelyMultiplexPauli
title: Operação ApproximatelyMultiplexPauli
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximatelyMultiplexPauli
qsharp.summary: Applies a Pauli rotation conditioned on an array of qubits, truncating small rotation angles according to a given tolerance.
ms.openlocfilehash: 8024df4608f14408bfcd46139e72454ff44b116f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207744"
---
# <a name="approximatelymultiplexpauli-operation"></a>Operação ApproximatelyMultiplexPauli

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma rotação Pauli condição em uma matriz de qubits, truncando pequenos ângulos de rotação de acordo com uma determinada tolerância.

```qsharp
operation ApproximatelyMultiplexPauli (tolerance : Double, coefficients : Double[], pauli : Pauli, control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Descrição

Isso aplica uma operação unitário controlada com controle de multiplicação que executa rotações por meio do ângulo $ \ theta_j $ sobre o operador Pauli de qubit único $P $ quando controlado pelo estado do número $n $-qubit $ \ket{j} $.
Em particular, a ação dessa operação é representada pelo unitário

$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j} \otimes e ^ {i P \ theta_j}.
\end{align}

##

## <a name="input"></a>Entrada

### <a name="tolerance--double"></a>tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)

Uma tolerância abaixo que pequenos coeficientes são truncados.


### <a name="coefficients--double"></a>coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]

Matriz de até $2 ^ n $ coeficientes $ \ theta_j $. O coeficiente $j $ th indexa o estado de número $ \ket{j} $ codificado em um formato little-endian.


### <a name="pauli--pauli"></a>Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Operador Pauli $P $ que determina o eixo de rotação.


### <a name="control--littleendian"></a>controle: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n o registro de controle $-qubit que codifica Estados de número $ \ket{j} $ no formato little-endian.


### <a name="target--qubit"></a>destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Registro de qubit único que é girado por $e ^ {i P \ theta_j} $.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

`coefficients` será preenchido com os elementos $ \ theta_j = $0 se menos de $2 ^ n $ forem especificados.

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. MultiplexPauli](xref:Microsoft.Quantum.Canon.MultiplexPauli)