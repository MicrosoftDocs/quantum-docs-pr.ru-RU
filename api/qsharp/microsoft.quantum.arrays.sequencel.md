---
uid: Microsoft.Quantum.Arrays.SequenceL
title: Функция Sequence
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceL
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: d5ce63575e703341fce42c0be393765c342bbd89
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730024"
---
# <a name="sequencel-function"></a>Функция Sequence

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


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

## <a name="remarks"></a>Remarks

Разница между `from` и `to` должна соответствовать `Int` значению.