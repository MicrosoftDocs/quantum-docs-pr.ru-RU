---
uid: Microsoft.Quantum.Arrays.IsPermutation
title: Функция перестановки
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsPermutation
qsharp.summary: Outputs true if and only if a given array represents a permutation.
ms.openlocfilehash: 7e563650f33b0292e1e41f629829a2d3b9e5fd28
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848096"
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



## <a name="example"></a>Пример

Следующий код Q # выводит сообщение "все диагностические сообщения успешно выполнены":

```qsharp
Fact(IsPermutation([2, 0, 1], "");
Contradiction(IsPermutation([5, 0, 1], "[5, 0, 1] isn't a permutation");
Message("All diagnostics completed successfully.");
```

## <a name="remarks"></a>Remarks

Массив нулевой длины является тривиальной перестановкой.