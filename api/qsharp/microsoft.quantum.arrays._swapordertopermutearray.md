---
uid: Microsoft.Quantum.Arrays._SwapOrderToPermuteArray
title: Функция _SwapOrderToPermuteArray
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: _SwapOrderToPermuteArray
qsharp.summary: Returns the order elements in an array need to be swapped to produce an ordered array. Assumes swaps occur in place.
ms.openlocfilehash: ff8e4e23dde7d69f93054a275548ded49d5b0bfb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846293"
---
# <a name="_swapordertopermutearray-function"></a>Функция _SwapOrderToPermuteArray

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает порядок элементов в массиве, который должен быть переключен для создания упорядоченного массива.
Предполагается, что происходит переключение на месте.

```qsharp
function _SwapOrderToPermuteArray (newOrder : Int[]) : (Int, Int)[]
```


## <a name="input"></a>Входные данные

### <a name="neworder--int"></a>newOrder: [int](xref:microsoft.quantum.lang-ref.int)[]

Массив с перестановкой индексов нового массива. Должно быть $n $ Elements, каждое из которых является уникальным целым числом от $0 $ до $n-$1.



## <a name="output--intint"></a>Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []

Кортеж представляет два индекса, которые нужно поменять местами. Перестановки начинаются с самого низкого индекса.

## <a name="example"></a>Пример

```qsharp
// The following returns [(0, 5),(0, 4),(0, 1),(0, 3)];
let swapOrder = _SwapOrderToPermuteArray([5, 3, 2, 0, 1, 4]);
```

## <a name="remarks"></a>Remarks

## <a name="psuedocode"></a>псуедокоде

для (индекс в 0.. Length (newOrder) – 1) {while newOrder [Индекс]! = Индекс {Switch newOrder [Индекс] с newOrder [newOrder [index]]}}