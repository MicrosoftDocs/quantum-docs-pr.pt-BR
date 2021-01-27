---
uid: Microsoft.Quantum.Arithmetic.Carry
title: Operação de execução
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Carry
qsharp.summary: Implements a reversible carry gate. Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2` and the carry-out is xored to the qubit `carryOut`.
ms.openlocfilehash: dfb08a9a9c805c0b611ab993c9b1eb949810a7da
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843346"
---
# <a name="carry-operation"></a>Operação de execução

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Implementa uma porta de transporte reversível. Dado um bit de transporte codificado em qubit `carryIn` e dois bits de soma codificados no `summand1` e no, o `summand2` computa o XOR bit e o de `carryIn` `summand1` `summand2` qubit `summand2` e a execução é XORed para o qubit `carryOut` .

```qsharp
operation Carry (carryIn : Qubit, summand1 : Qubit, summand2 : Qubit, carryOut : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="carryin--qubit"></a>transporte: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit de transporte.


### <a name="summand1--qubit"></a>summand1: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Primeiro soma qubit.


### <a name="summand2--qubit"></a>summand2: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Segundo soma qubit, é substituído pelo menor bit da soma de `summand1` e `summand2` .


### <a name="carryout--qubit"></a>postergar: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit de execução, será XORed com o bit mais alto da soma.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)

