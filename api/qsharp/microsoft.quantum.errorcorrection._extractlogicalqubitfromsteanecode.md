---
uid: Microsoft.Quantum.ErrorCorrection._ExtractLogicalQubitFromSteaneCode
title: _ExtractLogicalQubitFromSteaneCode operação
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: _ExtractLogicalQubitFromSteaneCode
qsharp.summary: >-
  Syndrome measurement and the inverse of embedding.

  $X$- and $Z$-stabilizers are not treated equally, which is due to the particular choice of the encoding circuit. This asymmetry leads to a different syndrome extraction routine. One could measure the syndrome by measuring multi-qubit Pauli operator directly on the code state, but for the distillation purpose the logical qubit is returned into a single qubit, in course of which the syndrome measurements can be done without further ancillas.
ms.openlocfilehash: 273692efa629cb8cc20069ef500c4e0902fbc3ff
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201335"
---
# <a name="_extractlogicalqubitfromsteanecode-operation"></a>_ExtractLogicalQubitFromSteaneCode operação

Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Medição da síndrome e o inverso da incorporação.

$X $-e $Z $-estabilizadores não são tratados igualmente, o que se deve à escolha específica do circuito de codificação.
Essa assimetria leva a uma rotina de extração de síndrome diferente.
É possível medir a síndrome, medindo o operador qubit Pauli diretamente no estado do código, mas, para a finalidade do detalhamento, o qubit lógico é retornado em um único qubit, o que faz com que as medidas da síndrome possam ser feitas sem mais ancillas.

```qsharp
operation _ExtractLogicalQubitFromSteaneCode (code : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit, Int, Int)
```


## <a name="input"></a>Entrada

### <a name="code--logicalregister"></a>código: [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)





## <a name="output--qubitintint"></a>Saída: ([qubit](xref:microsoft.quantum.lang-ref.qubit),[int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))

O qubit lógico e um par de inteiros para $X $-síndrome e $Z $-síndrome.
Elas representam o índice do código qubit em que um único $X $-ou $Z $-Error teria causado a síndrome medida.

## <a name="remarks"></a>Comentários

Observe que essa operação não está marcada como `internal` , pois os testes de unidade dependem diretamente dessa operação. Como uma melhoria futura, os testes de unidade devem ser refatoráveis para depender apenas dos chamadores públicos diretamente.

> [!WARNING]
> Essa rotina é adaptada a um circuito de codificação específico para o código de 7 qubit de Steane; Se o circuito de codificação for modificado, o resultado da síndrome poderá ter que ser interpretado de forma diferente.