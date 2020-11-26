---
uid: Microsoft.Quantum.Oracles.ContinuousOracle
title: Определяемый пользователем тип Континуаусоракле
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ContinuousOracle
qsharp.summary: >-
  Represents a continuous-time oracle.

  This is an oracle that implements $U(\delta t) : \ket{\psi(t)} \mapsto \ket{\psi(t + \delta t)}$ for all times $t$, where $U$ is a fixed operation, and where $\delta t$ is a non-negative real number.
ms.openlocfilehash: fb05e97c635ba75fc2d85dc2a7cea27f3a3af63f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226797"
---
# <a name="continuousoracle-user-defined-type"></a>Определяемый пользователем тип Континуаусоракле

Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Представляет Oracle с непрерывным временем.

Это Oracle, который реализует $U (\делта t): \кет{\пси (t)} \мапсто \кет{\пси (t + \делта t)} $ для всех случаев $t $, где $U $ является фиксированной операцией и где $ \делта t $ — неотрицательное вещественное число.

```qsharp

newtype ContinuousOracle = (((Double, Qubit[]) => Unit is Adj + Ctl));
```

