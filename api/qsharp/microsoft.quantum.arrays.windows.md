---
uid: Microsoft.Quantum.Arrays.Windows
title: Функция Windows
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Windows
qsharp.summary: Returns all consecutive subarrays of length `size`.
ms.openlocfilehash: 6071d1c3e5981855c57abd0e741b1de0201c30a3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729936"
---
# <a name="windows-function"></a>Функция Windows

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


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