---
uid: Microsoft.Quantum.Arrays.ConstantArray
title: Функция Константаррай
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ConstantArray
qsharp.summary: Creates an array of given length with all elements equal to given value.
ms.openlocfilehash: a3ad8a18856888a0ca6f9dd691242156b0c044d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846222"
---
# <a name="constantarray-function"></a>Функция Константаррай

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Создает массив заданной длины со всеми элементами, равными заданному значению.

```qsharp
function ConstantArray<'T> (length : Int, value : 'T) : 'T[]
```


## <a name="input"></a>Входные данные

### <a name="length--int"></a>Длина: [int](xref:microsoft.quantum.lang-ref.int)

Длина нового массива.


### <a name="value--t"></a>значение: 'T

Значение каждого элемента нового массива.



## <a name="output--t"></a>Выходные данные: 'T []

Новый массив длины `length` , каждый элемент которого имеет значение `value` .

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е



## <a name="example"></a>Пример

Следующий код создает массив из трех логических значений, каждый из которых равен `true` :

```qsharp
let array = ConstantArray(3, true);
```