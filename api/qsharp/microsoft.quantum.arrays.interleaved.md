---
uid: Microsoft.Quantum.Arrays.Interleaved
title: Функция с чередованием
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Interleaved
qsharp.summary: Interleaves two arrays of (almost) same size.
ms.openlocfilehash: 3605c0d0bc43cdb1097d025861c3ec2424763c86
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848111"
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

## <a name="example"></a>Пример

```qsharp
// same as int1 = [1, -1, 2, -2, 3, -3]
let int1 = Interleaved([1, 2, 3], [-1, -2, -3])

// same as int2 = [false, true, false, true, false]
let int2 = Interleaved(ConstantArray(3, false), ConstantArray(2, true));
```