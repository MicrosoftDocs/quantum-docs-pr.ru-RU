---
uid: Microsoft.Quantum.Simulation.EvolutionUnitary
title: Определяемый пользователем тип Еволутионунитари
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionUnitary
qsharp.summary: >-
  Represents a unitary time-evolution operator.

  The first parameter is is duration of time-evolution, and the second parameter is the qubit register acted upon by the unitary.
ms.openlocfilehash: ea160bb9a0a8bb5106c3e37a6a16155bad71dd25
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856044"
---
# <a name="evolutionunitary-user-defined-type"></a>Определяемый пользователем тип Еволутионунитари

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Представляет отдельный оператор времени развития.

Первый параметр — это длительность развития времени, а второй параметр — кубит регистр, который зависит от единой.

```qsharp

newtype EvolutionUnitary = (((Double, Qubit[]) => Unit is Adj + Ctl));
```

