---
uid: Microsoft.Quantum.Arrays.Fold
title: Функция fold
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Fold
qsharp.summary: Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.
ms.openlocfilehash: d12e070058178ce2cbdd70cade5bc16607a55d5e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848606"
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

## <a name="example"></a>Пример

```qsharp
function Plus(a : Double, b : Double) {
    return a + b;
}
function Sum(xs : Double[]) {
    return Fold(Plus, 0.0, xs);
}
```