---
uid: Microsoft.Quantum.Arrays.IsPermutation
title: Функция перестановки
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsPermutation
qsharp.summary: Outputs true if and only if a given array represents a permutation.
ms.openlocfilehash: 144f683818b5d75de5b075328365d3e994de29d1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220932"
---
# <a name="ispermutation-function"></a>Функция перестановки

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Выводит значение true только в том случае, если данный массив представляет перестановку.

```qsharp
function IsPermutation (permuation : Int[]) : Bool
```


## <a name="description"></a>Описание

При наличии массива `array` длины `n` возвращает значение true только в том случае, если каждое целое число из `0` должно `n - 1` встречаться ровно один раз в `array` , например, `array` может интерпретироваться как перестановка `n` элементов.

## <a name="input"></a>Входные данные

### <a name="permuation--int"></a>пермуатион: [int](xref:microsoft.quantum.lang-ref.int)[]

Массив, который может или не может представлять перестановку.



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)



## <a name="remarks"></a>Комментарии

Массив нулевой длины является тривиальной перестановкой.