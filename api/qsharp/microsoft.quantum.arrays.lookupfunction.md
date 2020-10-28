---
uid: Microsoft.Quantum.Arrays.LookupFunction
title: Функция Лукупфунктион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: LookupFunction
qsharp.summary: Given an array, returns a function which returns elements of that array.
ms.openlocfilehash: c929054b96ee499db896cacf0e3ae4da6f6c4b98
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730152"
---
# <a name="lookupfunction-function"></a>Функция Лукупфунктион

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


При наличии массива возвращает функцию, которая возвращает элементы этого массива.

```qsharp
function LookupFunction<'T> (array : 'T[]) : (Int -> 'T)
```


## <a name="input"></a>Входные данные

### <a name="array--t"></a>массив: 'T []

Массив, который будет представлен как функция уточняющего запроса.



## <a name="output--int---t"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int) ->

Функция `f` , которая `f(idx) == f[idx]` .

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип элементов массива, представленного в виде функции уточняющего запроса.

## <a name="remarks"></a>Remarks

Эта функция в основном полезна для взаимодействия с функциями и операциями, которые принимают `Int -> 'T` в качестве аргументов функции. Это обычно, например, в библиотеке представления генератора, где функции используются, чтобы избежать необходимости записи всего массива в памяти.