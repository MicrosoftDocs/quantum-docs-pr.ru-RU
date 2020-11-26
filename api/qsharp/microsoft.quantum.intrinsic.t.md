---
uid: Microsoft.Quantum.Intrinsic.T
title: Операция T
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: T
qsharp.summary: Applies the T gate to a single qubit.
ms.openlocfilehash: 352ef2c1b15a46dea85c420fc6f1cfab0382e73a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198407"
---
# <a name="t-operation"></a>Операция T

Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Применяет T-шлюз к одному кубит.

```qsharp
operation T (qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

Эта операция может быть смоделирована единой матрицей \бегин{алигн} T \масрел{: =} \бегин{бматрикс} 1 & 0 \\ \\ 0 & e ^ {i \пи/4} \енд{бматрикс}.
\енд{алигн}

## <a name="input"></a>Входные данные

### <a name="qubit--qubit"></a>Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Кубит, к которому должен быть применен шлюз.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

