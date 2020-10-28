---
uid: Microsoft.Quantum.Research.Chemistry._DeltaParityCNOTbitstring
title: Функция _DeltaParityCNOTbitstring
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _DeltaParityCNOTbitstring
qsharp.summary: Classical processing step of `ApplyDeltaParity`. This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.
ms.openlocfilehash: 95b4c2df05f32cb937ec2cf421f43f2fdbf319da
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710848"
---
# <a name="_deltaparitycnotbitstring-function"></a>Функция _DeltaParityCNOTbitstring

Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)

Пакеты [](https://nuget.org/packages/)


Классический этап обработки `ApplyDeltaParity` .
При этом вычисляется список элементов управления Кубитс для оценки разницы четности между любыми двумя ПКРС... условия четной длины.

```qsharp
function _DeltaParityCNOTbitstring (prevFermionicTerm : Int[], nextFermionicTerm : Int[]) : (Int, Bool[])
```


## <a name="input"></a>Входные данные

### <a name="prevfermionicterm--int"></a>Превфермиониктерм: [int](xref:microsoft.quantum.lang-ref.int)[]




### <a name="nextfermionicterm--int"></a>Некстфермиониктерм: [int](xref:microsoft.quantum.lang-ref.int)[]





## <a name="output--intbool"></a>Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int),[bool](xref:microsoft.quantum.lang-ref.bool)[])



## <a name="remarks"></a>Remarks

Предполагается, что длина терминов равна.
Вычисление списка элементов управления для разницы четности между любыми двумя терминами.
Предполагается, что списки ввода сортируются в возрастающем порядке.