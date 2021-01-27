---
uid: Microsoft.Quantum.Arrays.SequenceL
title: Функция Sequence
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceL
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 7e3c5c31428f9be152e28afbe478a3d15eb0a56c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850984"
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

## <a name="example"></a>Пример

```qsharp
let arr1 = SequenceL(0L, 3L); // [0L, 1L, 2L, 3L]
let arr2 = SequenceL(23L, 29L); // [23L, 24L, 25L, 26L, 27L, 28L, 29L]
let arr3 = SequenceL(-5L, -2L); // [-5L, -4L, -3L, -2L]
```

## <a name="remarks"></a>Remarks

Разница между `from` и `to` должна соответствовать `Int` значению.