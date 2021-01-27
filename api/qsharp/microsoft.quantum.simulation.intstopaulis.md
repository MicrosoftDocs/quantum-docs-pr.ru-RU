---
uid: Microsoft.Quantum.Simulation.IntsToPaulis
title: Функция Интстопаулис
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntsToPaulis
qsharp.summary: Converts an array of integers to an array of single-qubit Pauli operators.
ms.openlocfilehash: 6904054bb1aff3a57c80882694b4c217812b2b81
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842227"
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