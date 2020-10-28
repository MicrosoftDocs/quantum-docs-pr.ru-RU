---
uid: Microsoft.Quantum.Arrays.IsPermutation
title: Функция перестановки
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsPermutation
qsharp.summary: Outputs true if and only if a given array represents a permutation.
ms.openlocfilehash: 361bb21bedc725c25a1f3dfc811e9cfda4cb45ff
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730176"
---
# <a name="ispermutation-function"></a>Функция перестановки

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


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



## <a name="remarks"></a>Remarks

Массив нулевой длины является тривиальной перестановкой.