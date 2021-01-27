---
uid: Microsoft.Quantum.Arrays.EmptyArray
title: Функция Емптяррай
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: EmptyArray
qsharp.summary: Returns the empty array of a given type.
ms.openlocfilehash: cf15e61862bb64fb3408db2318fafb56d532b365
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846173"
---
# <a name="emptyarray-function"></a>Функция Емптяррай

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Возвращает пустой массив заданного типа.

```qsharp
function EmptyArray<'TElement> () : 'TElement[]
```


## <a name="output--telement"></a>Выходные данные: ' TElement []

Пустой массив.

## <a name="type-parameters"></a>Параметры типа

### <a name="telement"></a>' TElement

Тип элементов массива.

## <a name="example"></a>Пример

```qsharp
let empty = EmptyArray<Int>();
```