---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCodeRecoveryFn
title: Função FiveQubitCodeRecoveryFn
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCodeRecoveryFn
qsharp.summary: Returns function that maps error syndrome measurements to the appropriate error-correcting Pauli operators by table lookup for the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 5b8afe222d197eb7d342ac45f027f2de9130b61a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693459"
---
# <a name="fivequbitcoderecoveryfn-function"></a>Função FiveQubitCodeRecoveryFn

Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Agrupa [](https://nuget.org/packages/)


Retorna a função que mapeia as medições de erro de síndrome para os operadores de Pauli de correção de erros apropriados por pesquisa de tabela para o código Quantum ⟦ 5, 1, 3 ⟧.

```qsharp
function FiveQubitCodeRecoveryFn () : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="output--recoveryfn"></a>Saída: [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

Função do tipo `RecoveryFn` que usa uma medida de síndrome `Result[]` e retorna os `Pauli[]` operadores que corrigem o erro detectado.

## <a name="remarks"></a>Comentários

Ao iterar em todos os erros de peso de $1 $, obtemos um total de US $3 \ vezes 5 = 15 $ possíveis síndromes não triviais.
Junto com a identidade, uma tabela de erros e a síndrome correspondente são criadas. Para o código de 5 qubit, essa tabela é fornecida por: $X \_ 1: (0, 0, 0, 1); X \_ 2: (1, 0, 0, 0); X \_ 3: (1, 1, 0, 0); X \_ 4: (0, 1, 1, 0); X \_ 5: (0, 0, 1, 1) $, $Z \_ 1: (1, 0, 1, 0); Z \_ 2: (0, 1, 0, 1); Z \_ 3: (0, 0, 1, 0); Z \_ 4: (1, 0, 0, 1); Z \_ 5: (0, 1, 0, 0) $ com $Y _i $ obtido adicionando as per$Xs _i $ e $Z _i $. Observe que a ordem na recuperação de pesquisa de tabela é fornecida pela conversão de bitvectors em inteiros (usando little endian).

## <a name="see-also"></a>Consulte Também

- [Microsoft. Quantum. ErrorCorrection. RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)