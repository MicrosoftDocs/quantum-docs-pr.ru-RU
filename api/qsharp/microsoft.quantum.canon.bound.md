---
uid: Microsoft.Quantum.Canon.Bound
title: Связанная функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Bound
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.
ms.openlocfilehash: 041f654c14f6e926d60038fee698b2b829fab8b3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841052"
---
# <a name="bound-function"></a>Связанная функция

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

## <a name="example"></a>Пример

Следующие эквивалентны:

```qsharp
let bound = Bound([U, V]);
bound(x);
```

и

```qsharp
U(x); V(x);
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Баундк](xref:Microsoft.Quantum.Canon.BoundC)
- [Microsoft. тактов. Canon. Bounds](xref:Microsoft.Quantum.Canon.BoundA)
- [Microsoft. тактов. Canon. Баундка](xref:Microsoft.Quantum.Canon.BoundCA)