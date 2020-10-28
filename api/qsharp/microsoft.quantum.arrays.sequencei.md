---
uid: Microsoft.Quantum.Arrays.SequenceI
title: Функция Секуенцеи
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceI
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: d5dc4377c696e14b505c63701c2f5ca0dadca672
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730033"
---
# <a name="sequencei-function"></a>Функция Секуенцеи

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


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