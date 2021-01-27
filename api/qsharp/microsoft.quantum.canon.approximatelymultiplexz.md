---
uid: Microsoft.Quantum.Canon.ApproximatelyMultiplexZ
title: Operação ApproximatelyMultiplexZ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximatelyMultiplexZ
qsharp.summary: Applies a Pauli Z rotation conditioned on an array of qubits, truncating small rotation angles according to a given tolerance.
ms.openlocfilehash: b69b4de62241a7d16c2f07449115f864defda45d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841099"
---
# <a name="approximatelymultiplexz-operation"></a>Operação ApproximatelyMultiplexZ

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma rotação de Pauli Z condicionalmente em uma matriz de qubits, truncando pequenos ângulos de rotação de acordo com uma determinada tolerância.

```qsharp
operation ApproximatelyMultiplexZ (tolerance : Double, coefficients : Double[], control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Descrição

Isso aplica a operação unitário controlada de multiplicação que executa rotações por ângulo $ \ theta_j $ sobre o operador Pauli de qubit único $Z $ quando controlado pelo estado do número $n $-qubit $ \ket{j} $.
Em particular, essa operação pode ser representada pelo unitário

$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j} \otimes e ^ {i Z \ theta_j}.
\end{align} $ $

## <a name="input"></a>Entrada

### <a name="tolerance--double"></a>tolerância: [dupla](xref:microsoft.quantum.lang-ref.double)

Uma tolerância abaixo que pequenos coeficientes são truncados.


### <a name="coefficients--double"></a>coeficientes: [duplo](xref:microsoft.quantum.lang-ref.double)[]

Matriz de até $2 ^ n $ coeficientes $ \ theta_j $. O coeficiente $j $ th indexa o estado de número $ \ket{j} $ codificado em um formato little-endian.


### <a name="control--littleendian"></a>controle: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n o registro de controle $-qubit que codifica Estados de número $ \ket{j} $ no formato little-endian.


### <a name="target--qubit"></a>destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Registro de qubit único que é girado por $e ^ {i P \ theta_j} $.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

`coefficients` será preenchido com os elementos $ \ theta_j = $0 se menos de $2 ^ n $ forem especificados.

## <a name="references"></a>Referências

- Síntese de circuitos lógicos Quantum Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. MultiplexZ](xref:Microsoft.Quantum.Canon.MultiplexZ)