---
uid: Microsoft.Quantum.Simulation.IntsToPaulis
title: Функция Интстопаулис
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntsToPaulis
qsharp.summary: Converts an array of integers to an array of single-qubit Pauli operators.
ms.openlocfilehash: 605257aa7ca39e457127e3c3459b5891145b1863
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709448"
---
# <a name="intstopaulis-function"></a>Функция Интстопаулис

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакеты [](https://nuget.org/packages/)


Преобразует массив целых чисел в массив однокубитных операторов Паули.

```qsharp
function IntsToPaulis (ints : Int[]) : Pauli[]
```


## <a name="input"></a>Входные данные

### <a name="ints--int"></a>ints: [int](xref:microsoft.quantum.lang-ref.int)[]

Массив целых чисел в диапазоне, `0..3`  который должен быть преобразован в операторы Паули.



## <a name="output--pauli"></a>Выходные данные: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]

Массив `paulis` операторов Паули `Pauli[]` имеет одинаковую длину `ints` , `paulis[idxPauli]` равную элементу, `[PauliI, PauliX, PauliY, PauliZ]` заданному параметром `ints[idxPauli]` .