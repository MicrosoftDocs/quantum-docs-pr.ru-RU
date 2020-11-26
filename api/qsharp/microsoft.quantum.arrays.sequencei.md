---
uid: Microsoft.Quantum.Arrays.SequenceI
title: Функция Секуенцеи
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceI
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 5f03e5f2baff8077c1fa3fb5f1f079528ef0e215
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220303"
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