---
uid: Microsoft.Quantum.Canon.ApplyIfC
title: Операция Апплифк
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfC
qsharp.summary: Applies a controllable operation conditioned on a classical bit.
ms.openlocfilehash: e16254154909eb844164538acb7b82fedc11f86a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729593"
---
# <a name="applyifc-operation"></a>Операция Апплифк

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет управляемую операцию к классическому биту.

```qsharp
operation ApplyIfC<'T> (op : ('T => Unit is Ctl), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a>Описание

При наличии операции `op` и битового значения `bit` применяется `op` к, `target` Если имеет `bit` значение `true` . Если значение `false` равно, то ничего не происходит с `target` .
Суффикс `C` указывает, что операция, которая должна быть применена, является управляемой.

## <a name="input"></a>Входные данные

### <a name="op--t--unit-ctl"></a>Op: 'T => [единицы](xref:microsoft.quantum.lang-ref.unit) CTL

Операция, применяемая к условию.


### <a name="bit--bool"></a>bit: [bool](xref:microsoft.quantum.lang-ref.bool)

Логическое значение, определяющее, применяется ли оператор Op.


### <a name="target--t"></a>Целевой объект: 'T

Входные данные, к которым применяется операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип входных данных операции, которая должна применяться условно.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплифк](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [Microsoft. тактов. Canon. Апплифа](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [Microsoft. тактов. Canon. Апплифка](xref:Microsoft.Quantum.Canon.ApplyIfCA)