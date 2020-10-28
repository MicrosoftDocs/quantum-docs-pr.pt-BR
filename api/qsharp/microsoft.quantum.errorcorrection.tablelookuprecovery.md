---
uid: Microsoft.Quantum.ErrorCorrection.TableLookupRecovery
title: Função TableLookupRecovery
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: TableLookupRecovery
qsharp.summary: For a given table of Pauli operations on a given register of qubits, this function returns an object of type `RecoveryFn` which contains all information needed to perform a table-lookup decoding with respect to the given array of Pauli operations.
ms.openlocfilehash: c56a9bbb1db72b5ba03ee9976e648a59f651aa16
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92693419"
---
# <a name="tablelookuprecovery-function"></a><span data-ttu-id="702b6-102">Função TableLookupRecovery</span><span class="sxs-lookup"><span data-stu-id="702b6-102">TableLookupRecovery function</span></span>

<span data-ttu-id="702b6-103">Namespace: [Microsoft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="702b6-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="702b6-104">Agrupa [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="702b6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="702b6-105">Para uma determinada tabela de operações de Pauli em um determinado registro de qubits, essa função retorna um objeto do tipo `RecoveryFn` que contém todas as informações necessárias para executar uma decodificação de tabela de pesquisa em relação à matriz de operações de Pauli especificada.</span><span class="sxs-lookup"><span data-stu-id="702b6-105">For a given table of Pauli operations on a given register of qubits, this function returns an object of type `RecoveryFn` which contains all information needed to perform a table-lookup decoding with respect to the given array of Pauli operations.</span></span>

```qsharp
function TableLookupRecovery (table : Pauli[][]) : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="input"></a><span data-ttu-id="702b6-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="702b6-106">Input</span></span>

### <a name="table--pauli"></a><span data-ttu-id="702b6-107">tabela: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="702b6-107">table : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="702b6-108">Tabela de operações Pauli que operam em um determinado registro do qubit</span><span class="sxs-lookup"><span data-stu-id="702b6-108">Table of Pauli operations that operate on a given qubit register</span></span>



## <a name="output--recoveryfn"></a><span data-ttu-id="702b6-109">Saída: [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="702b6-109">Output : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="702b6-110">Um objeto do tipo `RecoveryFn` , ou seja, um mapa `Syndrome -> Pauli[]` que associa a uma determinada matriz da síndrome uma operação de correção de Pauli correspondente.</span><span class="sxs-lookup"><span data-stu-id="702b6-110">An object of type `RecoveryFn`, i.e., a map `Syndrome -> Pauli[]` that associates with a given syndrome array a corresponding Pauli correction operation.</span></span>