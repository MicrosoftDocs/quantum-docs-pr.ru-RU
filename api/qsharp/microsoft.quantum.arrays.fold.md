---
uid: Microsoft.Quantum.Arrays.Fold
title: Функция fold
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Fold
qsharp.summary: Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.
ms.openlocfilehash: a42f9a832c18bd612c1ae416187f3f2513eed54d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221170"
---
# <a name="fold-function"></a>Функция fold

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Выполняет итерацию функции `f` через массив `array` , возвращая `f(f(f(initialState, array[0]), array[1]), ...)` .

```qsharp
function Fold<'State, 'T> (folder : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State
```


## <a name="input"></a>Входные данные

### <a name="folder--statet---state"></a>Папка: ("State, t"-> "State

Функция для свертывания массива.


### <a name="state--state"></a>состояние: "состояние

Начальное состояние папки.


### <a name="array--t"></a>массив: 'T []

Массив значений, по которым будет выполняться свертывание.



## <a name="output--state"></a>Выходные данные: "штат

Конечное состояние, возвращенное папкой после прохода по всем элементам `array` .

## <a name="type-parameters"></a>Параметры типа

### <a name="state"></a>"State

Тип состояний `folder` , в которых функция работает, т. е. принимает в качестве первого аргумента и возвращает.
### <a name="t"></a>Е

Тип `array` элементов.