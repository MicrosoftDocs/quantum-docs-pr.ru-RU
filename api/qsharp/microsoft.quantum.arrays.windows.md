---
uid: Microsoft.Quantum.Arrays.Windows
title: Функция Windows
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Windows
qsharp.summary: Returns all consecutive subarrays of length `size`.
ms.openlocfilehash: 8f32a23aa4379744b84c3b8d9c8f565e61c3c64e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219895"
---
# <a name="windows-function"></a>Функция Windows

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает все последовательные подмассивы длины `size` .

```qsharp
function Windows<'T> (size : Int, array : 'T[]) : 'T[][]
```


## <a name="description"></a>Описание

Эта функция возвращает все `n - size + 1` подмассивы длины `size` в порядке, где `n` — это длина `arr` .
Первые подмассивы находятся `arr[0..size - 1], arr[1..size], arr[2..size + 1]` до последнего подмассива `arr[n - size..n - 1]` .

Если `size <= 0` или `size > n` , возвращается пустой массив.

## <a name="input"></a>Входные данные

### <a name="size--int"></a>Размер: [int](xref:microsoft.quantum.lang-ref.int)

Длина подмассивов.


### <a name="array--t"></a>массив: 'T []

Массив элементов.



## <a name="output--t"></a>Выходные данные: 'T [] []



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип `array` элементов.