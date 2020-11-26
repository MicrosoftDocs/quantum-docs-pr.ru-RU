---
uid: Microsoft.Quantum.Arrays.Interleaved
title: Функция с чередованием
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Interleaved
qsharp.summary: Interleaves two arrays of (almost) same size.
ms.openlocfilehash: 1ff5999cc19f47e3dcae601b960446923b613d90
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220966"
---
# <a name="interleaved-function"></a>Функция с чередованием

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Покидает два массива (почти) одинакового размера.

```qsharp
function Interleaved<'T> (first : 'T[], second : 'T[]) : 'T[]
```


## <a name="description"></a>Описание

Эта функция возвращает два массива, начиная с первого элемента из первого массива, затем первый элемент из второго массива и т. д.

Первый массив должен иметь длину, равную второму, или может иметь еще один элемент.

## <a name="input"></a>Входные данные

### <a name="first--t"></a>Первый: 'T []

Первый массив для чередования.


### <a name="second--t"></a>секунда: 'T []

Второй массив для чередования.



## <a name="output--t"></a>Выходные данные: 'T []

Массив с чередованием

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип каждого элемента `first` и `second` .