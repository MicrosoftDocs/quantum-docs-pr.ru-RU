---
uid: Microsoft.Quantum.Intrinsic.T
title: Операция T
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: T
qsharp.summary: Applies the T gate to a single qubit.
ms.openlocfilehash: bee252d9905aed26f6bf663f895e464e38073f44
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98817514"
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

