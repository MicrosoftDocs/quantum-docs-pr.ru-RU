---
uid: Microsoft.Quantum.Simulation.IntToPauli
title: Функция Инттопаули
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntToPauli
qsharp.summary: Converts a integer to a single-qubit Pauli operator.
ms.openlocfilehash: 76f482b86ff4a27b6e6ce6ae4ec3d59422563f12
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842249"
---
# <a name="inttopauli-function"></a>Функция Инттопаули

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Преобразует целое число в один кубит Паули оператор.

```qsharp
function IntToPauli (idx : Int) : Pauli
```


## <a name="input"></a>Входные данные

### <a name="idx--int"></a>IDX: [int](xref:microsoft.quantum.lang-ref.int)

Целое число в диапазоне `0..3` для преобразования в операторы Паули.



## <a name="output--pauli"></a>Выходные данные: [Паули](xref:microsoft.quantum.lang-ref.pauli)

`Pauli`Оператор, заданный параметром `[PauliI, PauliX, PauliY, PauliZ][idx]` .