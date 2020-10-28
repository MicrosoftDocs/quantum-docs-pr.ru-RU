---
uid: Microsoft.Quantum.Diagnostics.DumpOperation
title: Операция Думпоператион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpOperation
qsharp.summary: Given an operation, displays diagnostics about the operation that are made available by the current execution target.
ms.openlocfilehash: 444d42e2440b30b3bdf50d55a399568bed063222
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712863"
---
# <a name="dumpoperation-operation"></a>Операция Думпоператион

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакеты [](https://nuget.org/packages/)


При наличии операции отображает диагностику операции, которая стала доступной для текущего целевого объекта выполнения.

```qsharp
operation DumpOperation (nQubits : Int, op : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a>Входные данные

### <a name="nqubits--int"></a>Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)

Число Кубитс, на которых действует данная операция.


### <a name="op--qubit--unit-adj"></a>Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода

Операция, которую необходимо диагностировать.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Вызов этой операции не имеет наблюдаемого воздействия в Q #. Точная диагностика, отображаемая при их наличии, зависит от текущего целевого объекта выполнения и среды редактора.
Например, при использовании в симуляторе с полным состоянием отображается единая матрица, используемая для представления `op` .

Обратите внимание, что при запуске в симуляторах, которые приводят к неоднозначности глобального этапа (например, симулятор с полным состоянием), возвращаемые представления могут отличаться до глобального этапа.

Аналогичным образом, упорядочивание матричных представлений строк и столбцов может отличаться от соглашений, используемых каждым симулятором, поддерживающим эту операцию.