---
uid: Microsoft.Quantum.Canon.ApplyIfC
title: Операция Апплифк
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfC
qsharp.summary: Applies a controllable operation conditioned on a classical bit.
ms.openlocfilehash: ef16b23349b604d174e72d9ae06d2052e2ab60f8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841860"
---
# <a name="applyifc-operation"></a>Операция Апплифк

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет управляемую операцию к классическому биту.

```qsharp
operation ApplyIfC<'T> (op : ('T => Unit is Ctl), bit : Bool, target : 'T) : Unit is Ctl
```


## <a name="description"></a>Описание

При наличии операции `op` и битового значения `bit` применяется `op` к, `target` Если имеет `bit` значение `true` . Если значение `false` равно, то ничего не происходит с `target` .
Суффикс `C` указывает, что операция, которая должна быть применена, является управляемой.

## <a name="input"></a>Входные данные

### <a name="op--t--unit--is-ctl"></a>Op: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — CTL

Операция, применяемая к условию.


### <a name="bit--bool"></a>bit: [bool](xref:microsoft.quantum.lang-ref.bool)

Логическое значение, определяющее, применяется ли оператор Op.


### <a name="target--t"></a>Целевой объект: 'T

Входные данные, к которым применяется операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип входных данных операции, которая должна применяться условно.

## <a name="example"></a>Пример

Следующий командлет готовит регистр Кубитс в вычислительное состояние, представленное классическим битом строки, заданным как массив `Bool` значений:

```qsharp
let bitstring = [true, false, true];
using (register = Qubit(3)) {
    ApplyToEach(ApplyIf(X, _, _), Zipped(bitstring, register));
    // register should now be in the state |101⟩.
    ...
}
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплифк](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [Microsoft. тактов. Canon. Апплифа](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [Microsoft. тактов. Canon. Апплифка](xref:Microsoft.Quantum.Canon.ApplyIfCA)