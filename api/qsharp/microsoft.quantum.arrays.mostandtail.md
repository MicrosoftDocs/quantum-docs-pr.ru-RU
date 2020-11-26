---
uid: Microsoft.Quantum.Arrays.MostAndTail
title: Функция Мостандтаил
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MostAndTail
qsharp.summary: Returns a tuple of all but one and the last element of the array.
ms.openlocfilehash: 392efb20e4aaba80a77664444bb415d8bc9b0930
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220575"
---
# <a name="mostandtail-function"></a>Функция Мостандтаил

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает кортеж всех, кроме одного и последнего элемента массива.

```qsharp
function MostAndTail<'A> (array : 'A[]) : ('A[], 'A)
```


## <a name="input"></a>Входные данные

### <a name="array--a"></a>массив: ' A []

Массив, содержащий по крайней мере один элемент.



## <a name="output--aa"></a>Выходные данные: ("A []," A)

Кортеж всех, кроме одного и последнего элемента массива.

## <a name="type-parameters"></a>Параметры типа

### <a name="a"></a>' A

Тип элементов массива.