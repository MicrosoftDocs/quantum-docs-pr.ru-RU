---
uid: Microsoft.Quantum.Arrays.ForEach
title: Операция ForEach
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ForEach
qsharp.summary: Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.
ms.openlocfilehash: 90dd6f94408d37d2b32d82e772a482b0e69c523f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848581"
---
# <a name="foreach-operation"></a>Операция ForEach

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии массива и операции, определенной для элементов массива, возвращает новый массив, состоящий из изображений исходного массива в операции.

```qsharp
operation ForEach<'T, 'U> (action : ('T => 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a>Входные данные

### <a name="action--t--u"></a>действие: 'T => ' U 

Операция из `'T` к `'U` , которая применяется к каждому элементу.


### <a name="array--t"></a>массив: 'T []

Массив элементов `'T` .



## <a name="output--u"></a>Выходные данные: ' U []

Массив `'U[]` элементов, сопоставленных с `action` операцией.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип `array` элементов.
### <a name="u"></a>' U

Тип результата `action` операции.

## <a name="remarks"></a>Remarks

Операция определяется для универсальных типов, т. е. Если у нас есть массив `'T[]` и операция, `action : 'T -> 'U` которые мы можем сопоставлять элементы массива и создаем новый массив типа `'U[]` .