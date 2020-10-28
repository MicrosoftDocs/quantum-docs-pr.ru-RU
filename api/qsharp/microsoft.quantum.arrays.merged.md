---
uid: Microsoft.Quantum.Arrays.Merged
title: Объединенная функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Merged
qsharp.summary: Given two sorted arrays, returns a single array containing the elements of both in sorted order. Used internally by merge sort.
ms.openlocfilehash: da15a36f8f057cdc15062c96070ec21becc4794a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730112"
---
# <a name="merged-function"></a>Объединенная функция

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


При наличии двух отсортированных массивов возвращает один массив, содержащий элементы обоих элементов в отсортированном порядке. Используется для внутренних целей при сортировке слиянием.

```qsharp
function Merged<'T> (comparison : (('T, 'T) -> Bool), left : 'T[], right : 'T[]) : 'T[]
```


## <a name="input"></a>Входные данные

### <a name="comparison--tt---bool"></a>Сравнение: ('T) — > [bool](xref:microsoft.quantum.lang-ref.bool)




### <a name="left--t"></a>Left: ' ' []




### <a name="right--t"></a>Right: ' ' []





## <a name="output--t"></a>Выходные данные: 'T []



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

