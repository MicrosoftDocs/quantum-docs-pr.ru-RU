---
uid: Microsoft.Quantum.Arrays.ForEach
title: Операция ForEach
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ForEach
qsharp.summary: Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.
ms.openlocfilehash: ab6ac6eb913095f31ba166ac27f034f2e2875acf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730240"
---
# <a name="foreach-operation"></a>Операция ForEach

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


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