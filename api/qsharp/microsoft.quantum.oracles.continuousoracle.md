---
uid: Microsoft.Quantum.Oracles.ContinuousOracle
title: Tipo definido pelo usuário ContinuousOracle
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ContinuousOracle
qsharp.summary: >-
  Represents a continuous-time oracle.

  This is an oracle that implements $U(\delta t) : \ket{\psi(t)} \mapsto \ket{\psi(t + \delta t)}$ for all times $t$, where $U$ is a fixed operation, and where $\delta t$ is a non-negative real number.
ms.openlocfilehash: ac254b7556878550216d5c0c9222620fdc5c5702
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855925"
---
# <a name="continuousoracle-user-defined-type"></a><span data-ttu-id="5cef4-102">Tipo definido pelo usuário ContinuousOracle</span><span class="sxs-lookup"><span data-stu-id="5cef4-102">ContinuousOracle user defined type</span></span>

<span data-ttu-id="5cef4-103">Namespace: [Microsoft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="5cef4-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="5cef4-104">Pacote: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5cef4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5cef4-105">Representa um Oracle de tempo contínuo.</span><span class="sxs-lookup"><span data-stu-id="5cef4-105">Represents a continuous-time oracle.</span></span>

<span data-ttu-id="5cef4-106">Esse é um Oracle que implementa $U (\delta t): \ket{\psi (t)} \mapsto \ket{\psi (t + \delta t)} $ para todos os horários $t $, em que $U $ é uma operação fixa e em que $ \delta t $ é um número real não negativo.</span><span class="sxs-lookup"><span data-stu-id="5cef4-106">This is an oracle that implements $U(\delta t) : \ket{\psi(t)} \mapsto \ket{\psi(t + \delta t)}$ for all times $t$, where $U$ is a fixed operation, and where $\delta t$ is a non-negative real number.</span></span>

```qsharp

newtype ContinuousOracle = (((Double, Qubit[]) => Unit is Adj + Ctl));
```

