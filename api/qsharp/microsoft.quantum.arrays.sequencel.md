---
uid: Microsoft.Quantum.Arrays.SequenceL
title: Функция Sequence
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceL
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 3e5c7f64825f09d82792d3e46fe3f53f5814510b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220269"
---
# <a name="sequencel-function"></a>Функция Sequence

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Получение массива целых чисел в заданном интервале.

```qsharp
function SequenceL (from : BigInt, to : BigInt) : BigInt[]
```


## <a name="input"></a>Входные данные

### <a name="from--bigint"></a>от: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Инклюзивный начальный индекс интервала.


### <a name="to--bigint"></a>в: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Включающий Конечный индекс интервала, который не меньше `from` .



## <a name="output--bigint"></a>Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)[]

Массив, содержащий последовательность чисел `from` , `from + 1` ,..., `to` .

## <a name="remarks"></a>Комментарии

Разница между `from` и `to` должна соответствовать `Int` значению.