---
uid: Microsoft.Quantum.Research.Chemistry._DeltaParityCNOTbitstring
title: Функция _DeltaParityCNOTbitstring
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _DeltaParityCNOTbitstring
qsharp.summary: Classical processing step of `ApplyDeltaParity`. This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.
ms.openlocfilehash: 0c0da60e3c389f8208f9f7d5c84a09893f3c1bda
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226083"
---
# <a name="_deltaparitycnotbitstring-function"></a>Функция _DeltaParityCNOTbitstring

Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)

Пакет: [Microsoft. тактов. Research. Химия](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)


Классический этап обработки `ApplyDeltaParity` .
При этом вычисляется список элементов управления Кубитс для оценки разницы четности между любыми двумя ПКРС... условия четной длины.

```qsharp
function _DeltaParityCNOTbitstring (prevFermionicTerm : Int[], nextFermionicTerm : Int[]) : (Int, Bool[])
```


## <a name="input"></a>Входные данные

### <a name="prevfermionicterm--int"></a>Превфермиониктерм: [int](xref:microsoft.quantum.lang-ref.int)[]




### <a name="nextfermionicterm--int"></a>Некстфермиониктерм: [int](xref:microsoft.quantum.lang-ref.int)[]





## <a name="output--intbool"></a>Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int),[bool](xref:microsoft.quantum.lang-ref.bool)[])



## <a name="remarks"></a>Комментарии

Предполагается, что длина терминов равна.
Вычисление списка элементов управления для разницы четности между любыми двумя терминами.
Предполагается, что списки ввода сортируются в возрастающем порядке.