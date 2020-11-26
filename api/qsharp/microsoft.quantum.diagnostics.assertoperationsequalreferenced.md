---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced
title: Операция Ассертоператионсекуалреференцед
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualReferenced
qsharp.summary: >-
  Given two operations, asserts that they act identically for all input states.

  This assertion is implemented by using the Choi–Jamiołkowski isomorphism to reduce the assertion to one of a qubit state assertion on two entangled registers. Thus, this operation needs only a single call to each operation being tested, but requires twice as many qubits to be allocated. This assertion can be used to ensure, for instance, that an optimized version of an operation acts identically to its naïve implementation, or that an operation which acts on a range of non-quantum inputs agrees with known cases.
ms.openlocfilehash: 59c0fa72c9ca8f3bc512b6ed674fd73babc57f84
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202317"
---
# <a name="assertoperationsequalreferenced-operation"></a>Операция Ассертоператионсекуалреференцед

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Учитывая две операции, утверждает, что они действуют одинаково для всех входных состояний.

Это утверждение реализуется с помощью Чои – Жамиоłковски исоморфисм, чтобы уменьшить утверждение до одного из утверждений состояния кубит для двух регистров запутанными.
Таким образом, для этой операции требуется только один вызов каждой проверяемой операции, но в два раза требуется выделить не больше Кубитс.
Это утверждение можно использовать, чтобы убедиться, что оптимизированная версия операции действует аналогично его упрощенной реализации, или что операция, которая работает с диапазоном нетактовых входных данных, соглашается с известными случаями.

```qsharp
operation AssertOperationsEqualReferenced (nQubits : Int, actual : (Qubit[] => Unit), expected : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a>Входные данные

### <a name="nqubits--int"></a>Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)

Число Кубитс, которые должны быть переданы каждой операции.


### <a name="actual--qubit--unit"></a>фактически: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Проверяемая операция.


### <a name="expected--qubit--unit--is-adj"></a>ожидалось: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit) >

Операция, определяющая ожидаемое поведение для тестируемой операции.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Комментарии

Для выполнения этой операции необходимо, чтобы моделирование операции выполнялось как аджоинтабле, чтобы обратная операция могла выполняться только с регистром целевого объекта.
Формально можно указать операцию преобразования, которая ослабляет это требование, но операция перестановки не является физически реализабле для произвольных операций такта и, таким образом, не включается в этот параметр.