---
uid: Microsoft.Quantum.Arrays.Fold
title: Функция fold
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Fold
qsharp.summary: Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.
ms.openlocfilehash: 47c23dd657391d80fe473d98f2036d8ddf1dbb0b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730241"
---
# <a name="fold-function"></a>Функция fold

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


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