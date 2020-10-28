---
uid: Microsoft.Quantum.Canon.ApplyIfCA
title: Операция Апплифка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfCA
qsharp.summary: Applies a unitary operation conditioned on a classical bit.
ms.openlocfilehash: 9057c79622f15a082963d94fc261664e00322feb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729592"
---
# <a name="applyifca-operation"></a>Операция Апплифка

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет единую операцию с условием на Классический бит.

```qsharp
operation ApplyIfCA<'T> (op : ('T => Unit is Ctl + Adj), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a>Описание

При наличии операции `op` и битового значения `bit` применяется `op` к, `target` Если имеет `bit` значение `true` . Если значение `false` равно, то ничего не происходит с `target` .
Суффикс `CA` указывает, что применяемая операция является единой (управляемой и аджоинтабле).

## <a name="input"></a>Входные данные

### <a name="op--t--unit-ctl--adj"></a>Op: t => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + прилагательные

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