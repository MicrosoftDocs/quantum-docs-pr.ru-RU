---
uid: Microsoft.Quantum.Logical.LexographicComparison
title: Функция Лексографиккомпарисон
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LexographicComparison
qsharp.summary: Given a comparison function, returns a new function that lexographically compares two arrays.
ms.openlocfilehash: 4d8596c52b0fc8082a2b766d95d4052a4964b8b9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197590"
---
# <a name="lexographiccomparison-function"></a>Функция Лексографиккомпарисон

Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии функции сравнения возвращает новую функцию, лексографикалли сравнение двух массивов.

```qsharp
function LexographicComparison<'T> (elementComparison : (('T, 'T) -> Bool)) : (('T[], 'T[]) -> Bool)
```


## <a name="input"></a>Входные данные

### <a name="elementcomparison--tt---bool"></a>Елементкомпарисон: ('T) — > [bool](xref:microsoft.quantum.lang-ref.bool)

Функция, которая сравнивает два элемента `x` и `y` возвращает, если `x` меньше или равно `y` .



## <a name="output--tt---bool"></a>Выходные данные: ('T [], t [])-> [bool](xref:microsoft.quantum.lang-ref.bool)

Функция, которая сравнивает два массива `xs` и `ys` и возвращает значение, если `xs` происходит до или равно `ys` в порядке лексографикал.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип элементов сравниваемых массивов.

## <a name="remarks"></a>Комментарии

Сравнение лексографик между двумя массивами `xs` и `ys` определяется следующей процедурой. Мы говорим, что два элемента `x` и `y` эквивалентны, если `elementComparison(x, y)` и `elementComparison(y, x)` оба имеют значение true.

- Оба массива сравниваются по элементу до тех пор, пока первая пара элементов не эквивалентна. Массив, содержащий элемент, который в первую очередь выполняется в соответствии с `elementComparison` , считается первым в упорядочении лексографикал.
- Если неэквивалентные элементы не найдены и один массив длиннее другого, то считается, что первым является более короткий массив.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Arrays. Sorted](xref:Microsoft.Quantum.Arrays.Sorted)