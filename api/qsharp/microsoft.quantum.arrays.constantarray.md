---
uid: Microsoft.Quantum.Arrays.ConstantArray
title: Функция Константаррай
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ConstantArray
qsharp.summary: Creates an array of given length with all elements equal to given value.
ms.openlocfilehash: 848f18944829d08a10ec602dcb5d99c100c81f76
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730377"
---
# <a name="constantarray-function"></a>Функция Константаррай

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


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

