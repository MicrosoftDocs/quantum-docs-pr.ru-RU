---
uid: Microsoft.Quantum.Arrays.SequenceI
title: Функция Секуенцеи
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceI
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 3cf09e48cce1aeb1aac837465ee3a5e06adf5169
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851005"
---
# <a name="sequencei-function"></a>Функция Секуенцеи

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Получение массива целых чисел в заданном интервале.

```qsharp
function SequenceI (from : Int, to : Int) : Int[]
```


## <a name="input"></a>Входные данные

### <a name="from--int"></a>от: [int](xref:microsoft.quantum.lang-ref.int)

Инклюзивный начальный индекс интервала.


### <a name="to--int"></a>в: [int](xref:microsoft.quantum.lang-ref.int)

Включающий Конечный индекс интервала, который не меньше `from` .



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]

Массив, содержащий последовательность чисел `from` , `from + 1` ,..., `to` .

## <a name="example"></a>Пример

```qsharp
let arr1 = SequenceI(0, 3); // [0, 1, 2, 3]
let arr2 = SequenceI(23, 29); // [23, 24, 25, 26, 27, 28, 29]
let arr3 = SequenceI(-5, -2); // [-5, -4, -3, -2]

let numbers = SequenceI(0, _); // function to create sequence from 0 to `to`
let naturals = SequenceI(1, _); // function to create sequence from 1 to `to`
```