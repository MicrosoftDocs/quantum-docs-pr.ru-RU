---
uid: Microsoft.Quantum.Canon.Bound
title: Связанная функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Bound
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.
ms.openlocfilehash: c12ce37054ddde1b98778888e90916c6e4725814
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207604"
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

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Баундк](xref:Microsoft.Quantum.Canon.BoundC)
- [Microsoft. тактов. Canon. Bounds](xref:Microsoft.Quantum.Canon.BoundA)
- [Microsoft. тактов. Canon. Баундка](xref:Microsoft.Quantum.Canon.BoundCA)