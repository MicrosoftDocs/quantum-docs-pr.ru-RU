---
uid: Microsoft.Quantum.Arrays.LookupFunction
title: Функция Лукупфунктион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: LookupFunction
qsharp.summary: Given an array, returns a function which returns elements of that array.
ms.openlocfilehash: 22b56bb7e9f03ebc5b2225efb2e6450d56022664
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845698"
---
# <a name="lookupfunction-function"></a>Функция Лукупфунктион

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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