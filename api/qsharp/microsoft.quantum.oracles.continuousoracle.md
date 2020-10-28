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
# <a name="continuousoracle-user-defined-type"></a>Определяемый пользователем тип Континуаусоракле

Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)

Пакеты [](https://nuget.org/packages/)


Представляет Oracle с непрерывным временем.

Это Oracle, который реализует $U (\делта t): \кет{\пси (t)} \мапсто \кет{\пси (t + \делта t)} $ для всех случаев $t $, где $U $ является фиксированной операцией и где $ \делта t $ — неотрицательное вещественное число.

```qsharp

newtype ContinuousOracle = (((Double, Qubit[]) => Unit is Adj + Ctl));
```

