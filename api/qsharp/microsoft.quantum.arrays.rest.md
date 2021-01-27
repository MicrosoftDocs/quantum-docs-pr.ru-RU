---
uid: Microsoft.Quantum.Arrays.Rest
title: Функция RESTful
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Rest
qsharp.summary: Creates an array that is equal to an input array except that the first array element is dropped.
ms.openlocfilehash: b6c579df354185a2defb08cd78bce816d8cc5959
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845480"
---
# <a name="rest-function"></a>Функция RESTful

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Создает массив, равный входному массиву, за исключением того, что первый элемент массива удаляется.

```qsharp
function Rest<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a>Входные данные

### <a name="array--t"></a>массив: 'T []

Массив, второй с последними элементами которого образуют выходной массив.



## <a name="output--t"></a>Выходные данные: 'T []

Массив, содержащий элементы `array[1..Length(array) - 1]` .

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип элементов массива.