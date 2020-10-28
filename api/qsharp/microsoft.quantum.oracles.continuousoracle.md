---
uid: Microsoft.Quantum.Oracles.ContinuousOracle
title: Определяемый пользователем тип Континуаусоракле
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ContinuousOracle
qsharp.summary: >-
  Represents a continuous-time oracle.

  This is an oracle that implements $U(\delta t) : \ket{\psi(t)} \mapsto \ket{\psi(t + \delta t)}$ for all times $t$, where $U$ is a fixed operation, and where $\delta t$ is a non-negative real number.
ms.openlocfilehash: 9bc9b4bbdab6905a6a79893b1d559425ac679400
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733400"
---
# <a name="continuousoracle-user-defined-type"></a><span data-ttu-id="b3f5d-102">Определяемый пользователем тип Континуаусоракле</span><span class="sxs-lookup"><span data-stu-id="b3f5d-102">ContinuousOracle user defined type</span></span>

<span data-ttu-id="b3f5d-103">Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="b3f5d-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="b3f5d-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b3f5d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b3f5d-105">Представляет Oracle с непрерывным временем.</span><span class="sxs-lookup"><span data-stu-id="b3f5d-105">Represents a continuous-time oracle.</span></span>

<span data-ttu-id="b3f5d-106">Это Oracle, который реализует $U (\делта t): \кет{\пси (t)} \мапсто \кет{\пси (t + \делта t)} $ для всех случаев $t $, где $U $ является фиксированной операцией и где $ \делта t $ — неотрицательное вещественное число.</span><span class="sxs-lookup"><span data-stu-id="b3f5d-106">This is an oracle that implements $U(\delta t) : \ket{\psi(t)} \mapsto \ket{\psi(t + \delta t)}$ for all times $t$, where $U$ is a fixed operation, and where $\delta t$ is a non-negative real number.</span></span>

```qsharp

newtype ContinuousOracle = (((Double, Qubit[]) => Unit is Adj + Ctl));
```

