---
uid: Microsoft.Quantum.Arrays._SwapOrderToPermuteArray
title: Функция _SwapOrderToPermuteArray
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: _SwapOrderToPermuteArray
qsharp.summary: Returns the order elements in an array need to be swapped to produce an ordered array. Assumes swaps occur in place.
ms.openlocfilehash: 965f2f3d4f8b366abb27287ce0d27a3b7d7b8fb8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730432"
---
# <a name="_swapordertopermutearray-function"></a>Функция _SwapOrderToPermuteArray

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


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

## <a name="remarks"></a>Remarks

## <a name="psuedocode"></a>псуедокоде

для (индекс в 0.. Length (newOrder) – 1) {while newOrder [Индекс]! = Индекс {Switch newOrder [Индекс] с newOrder [newOrder [index]]}}