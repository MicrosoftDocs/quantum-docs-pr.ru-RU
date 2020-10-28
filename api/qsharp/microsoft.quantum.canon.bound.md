---
uid: Microsoft.Quantum.Canon.Bound
title: Связанная функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Bound
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.
ms.openlocfilehash: 34ca2b79d0ee09bd3b5b5b3f0c0b20420d5b3882
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716700"
---
# <a name="bound-function"></a>Связанная функция

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


При наличии массива операций, исдействующих один вход, создает новую операцию, которая выполняет каждую заданную операцию последовательно.

```qsharp
function Bound<'T> (operations : ('T => Unit)[]) : ('T => Unit)
```


## <a name="input"></a>Входные данные

### <a name="operations--t--unit-"></a>операции: t => [Unit](xref:microsoft.quantum.lang-ref.unit) []

Последовательность операций, выполняемых с заданным входом.



## <a name="output--t--unit"></a>Выходные данные: 'T => [единица](xref:microsoft.quantum.lang-ref.unit) 

Новая операция, которая выполняет каждую заданную операцию последовательно по входным данным.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Целевой объект, на котором выполняется каждая операция в массиве.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Баундк](xref:Microsoft.Quantum.Canon.BoundC)
- [Microsoft. тактов. Canon. Bounds](xref:Microsoft.Quantum.Canon.BoundA)
- [Microsoft. тактов. Canon. Баундка](xref:Microsoft.Quantum.Canon.BoundCA)