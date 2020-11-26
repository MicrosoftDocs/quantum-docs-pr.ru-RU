---
uid: Microsoft.Quantum.Simulation.IntsToPaulis
title: Функция Интстопаулис
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntsToPaulis
qsharp.summary: Converts an array of integers to an array of single-qubit Pauli operators.
ms.openlocfilehash: 2333dcbd2988480e2b2b9b217b26705f3578de00
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230537"
---
# <a name="intstopaulis-function"></a>Функция Интстопаулис

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Преобразует массив целых чисел в массив однокубитных операторов Паули.

```qsharp
function IntsToPaulis (ints : Int[]) : Pauli[]
```


## <a name="input"></a>Входные данные

### <a name="ints--int"></a>ints: [int](xref:microsoft.quantum.lang-ref.int)[]

Массив целых чисел в диапазоне, `0..3`  который должен быть преобразован в операторы Паули.



## <a name="output--pauli"></a>Выходные данные: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]

Массив `paulis` операторов Паули `Pauli[]` имеет одинаковую длину `ints` , `paulis[idxPauli]` равную элементу, `[PauliI, PauliX, PauliY, PauliZ]` заданному параметром `ints[idxPauli]` .