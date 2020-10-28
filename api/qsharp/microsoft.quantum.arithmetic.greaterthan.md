---
uid: Microsoft.Quantum.Arithmetic.GreaterThan
title: Operação GreaterThan
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: GreaterThan
qsharp.summary: Applies a greater-than comparison between two integers encoded into qubit registers, flipping a target qubit based on the result of the comparison.
ms.openlocfilehash: b7214b43dacd07b4750be4b681f30937185ac953
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92694787"
---
# <a name="greaterthan-operation"></a>Operação GreaterThan

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Agrupa [](https://nuget.org/packages/)


Aplica uma comparação maior que entre dois inteiros codificados em registros de qubit, invertendo um qubit de destino com base no resultado da comparação.

```qsharp
operation GreaterThan (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Qubit) : Unit
```


## <a name="description"></a>Descrição

Executa uma comparação estritamente maior que de dois inteiros $x $ e $y $, codificados em qubit registra xs e haves. Se $x > y $, o resultado qubit será invertido, caso contrário, o resultado qubit reterá seu estado.

## <a name="input"></a>Entrada

### <a name="xs--littleendian"></a>xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

LittleEndian qubit registrar a codificação do primeiro inteiro $x $.


### <a name="ys--littleendian"></a>haves: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

LittleEndian qubit a codificação do segundo inteiro $y $.


### <a name="result--qubit"></a>resultado: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit único que será invertido se $x > y $.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Usa o truque que $x-y = (x ' + y) ' $, onde ' denota o complemento de um.

## <a name="references"></a>Referências

- Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A New Quantum-balcão de adição de", 2004.
  https://arxiv.org/abs/quant-ph/0410184v1

- Thomas Haener, Martin Roetteler, Krysta M. Svore: "fatoração usando 2n + 2 qubits com multiplicação modular baseada em Toffoli", 2016 https://arxiv.org/abs/1611.07995