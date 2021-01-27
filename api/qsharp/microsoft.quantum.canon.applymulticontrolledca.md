---
uid: Microsoft.Quantum.Canon.ApplyMultiControlledCA
title: Operação ApplyMultiControlledCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiControlledCA
qsharp.summary: Applies a multiply controlled version of a singly controlled operation. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: a6549084b1c2fda885823f451d17f9c2ebbb4600
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841688"
---
# <a name="applymulticontrolledca-operation"></a>Operação ApplyMultiControlledCA

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Aplica uma versão controlada de multiplicação de uma operação controlada individualmente.
O modificador `CA` indica que a operação single-qubit é controlável e adjointable.

```qsharp
operation ApplyMultiControlledCA (singlyControlledOp : (Qubit[] => Unit is Adj), ccnot : Microsoft.Quantum.Canon.CCNOTop, controls : Qubit[], targets : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Entrada

### <a name="singlycontrolledop--qubit--unit--is-adj"></a>singlyControlledOp: [qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [unidade](xref:microsoft.quantum.lang-ref.unit)  é adj

Uma operação controlada em um único qubit.
O primeiro qubit no argumento da operação assumida como um controle e o restante são considerados como destino qubits.
`ApplyMultiControlled` sempre chama `singlyControlledOp` com um argumento de comprimento pelo menos 1.


### <a name="ccnot--ccnotop"></a>ccnot: [CCNOTop](xref:Microsoft.Quantum.Canon.CCNOTop)

A porta controlada por controlado não usada para a construção.


### <a name="controls--qubit"></a>controles: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

O qubits que deve `singlyControlledOp` ser controlado em.
O comprimento de `controls` deve ser pelo menos 1.


### <a name="targets--qubit"></a>destinos: [qubit](xref:microsoft.quantum.lang-ref.qubit)[]

O qubits de destino que `singlyControlledOp` atua.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Esta operação usa apenas qubits limpo ancilla.

Para obter a explicação e o diagrama de circuito, consulte a Figura 4,10, seção 4,3 em Nielsen & Chuang

## <a name="references"></a>Referências

- [*Michael A. Nielsen, Julio L. Chuang*, computação Quantum e informações de Quantum](http://doi.org/10.1017/CBO9780511976667)

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. Canon. ApplyMultiControlledC](xref:Microsoft.Quantum.Canon.ApplyMultiControlledC)