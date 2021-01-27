---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderNoCarryTTK
title: Operação RippleCarryAdderNoCarryTTK
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderNoCarryTTK
qsharp.summary: Reversible, in-place ripple-carry addition of two integers without carry out.
ms.openlocfilehash: 0e131204d3eaff7f99aa9ff7c3c1ae93a1bf611b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846337"
---
# <a name="ripplecarryaddernocarryttk-operation"></a>Operação RippleCarryAdderNoCarryTTK

Namespace: [Microsoft. Quantum. aritmético](xref:Microsoft.Quantum.Arithmetic)

Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Reversível, ondulado no local, adição de dois inteiros sem execução.

```qsharp
operation RippleCarryAdderNoCarryTTK (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Descrição

Dado dois $n inteiros de $ bit codificados em registros LittleEndian `xs` e `ys` , a operação computa a soma dos dois módulos inteiros módulo $2 ^ n $, em que $n $ é o tamanho do bit das entradas `xs` e `ys` . Ele não computa o bit de execução.

## <a name="input"></a>Entrada

### <a name="xs--littleendian"></a>xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

LittleEndian qubit registrar o primeiro soma inteiro.


### <a name="ys--littleendian"></a>haves: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

LittleEndian qubit a codificação do segundo inteiro soma, é modificado para manter o $n $ menos significativo bits da soma.



## <a name="output--unit"></a>Saída: [unidade](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Comentários

Esta operação tem a mesma funcionalidade que RippleCarryAdderTTK, mas não retorna o bit de execução.

## <a name="references"></a>Referências

- Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "circuitos de adição Quantum e Fan-out não vinculado", informações de Quantum e computação, Vol. 10, 2010.
  https://arxiv.org/abs/0910.2530