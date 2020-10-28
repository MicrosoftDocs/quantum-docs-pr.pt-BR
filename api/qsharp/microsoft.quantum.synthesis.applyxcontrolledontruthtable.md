---
uid: Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTable
title: Operação ApplyXControlledOnTruthTable
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyXControlledOnTruthTable
qsharp.summary: Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.
ms.openlocfilehash: 73d63936f02a52dfbbad7b8575110177a9e4463d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92697058"
---
# <a name="applyxcontrolledontruthtable-operation"></a>Operação ApplyXControlledOnTruthTable

Namespace: [Microsoft. Quantum. síntese](xref:Microsoft.Quantum.Synthesis)

Agrupa [](https://nuget.org/packages/)


Aplica a @"microsoft.quantum.intrinsic.x" operação em `target` , se a função booliana `func` for avaliada como true para a atribuição clássica no `controlRegister` .

```qsharp
operation ApplyXControlledOnTruthTable (func : BigInt, controlRegister : Qubit[], target : Qubit) : Unit
```


## <a name="description"></a>Descrição

A operação implementa a operação unitário \begin{align} U\ket {x} \ ket {y} = \ket{x}\ket{y \oplus f (x)} \end{align} em que $x $ e $y $ representam `controlRegister` e `target` , respectivamente.

A função booliana $f $ é representada como uma tabela verdadeira em termos de um grande inteiro.
Por exemplo, a função principal em três entradas é representada pelo bitstring `11101000` , onde o bit mais significativo `1` corresponde à atribuição de entrada `(1, 1, 1)` e o bit menos significativo `0` corresponde à atribuição de entrada `(0, 0, 0)` .
Ele pode ser representado pelo grande inteiro `0xE8L` em notação hexadecimal ou como `232L` em notação decimal.  O `L` sufixo indica que a constante é do tipo `BigInt` .
Mais detalhes sobre essa representação também podem ser encontrados nas [tabelas da verdade Kata](https://github.com/microsoft/QuantumKatas/tree/main/TruthTables).

A implementação usa @"microsoft.quantum.intrinsic.cnot" e @"microsoft.quantum.intrinsic.r1" Gates.

## <a name="input"></a>Entrada

### <a name="func--bigint"></a>Func: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Tabela booliana da verdade representada como um inteiro grande


### <a name="controlregister--qubit"></a>controlRegister: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Registro de qubits de controle


### <a name="target--qubit"></a>destino: [qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit de destino



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Referências

- [*N. Schuch* , *J. Siewert* , PRL 91, no. 027902, 2003, arXiv: Quant-pH/0303063](https://arxiv.org/abs/quant-ph/0303063)
- [*Mathias Soeken* , *Martin Roetteler* , arXiv: 2005.12310](https://arxiv.org/abs/2005.12310)

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. síntese. ApplyXControlledOnTruthTableWithCleanTarget](xref:Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget)