---
uid: Microsoft.Quantum.Arrays.MostAndTail
title: Функция Мостандтаил
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MostAndTail
qsharp.summary: Returns a tuple of all but one and the last element of the array.
ms.openlocfilehash: fd5569f1b71ac2fdf2b5c08ba7dde172e3a6744e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845591"
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