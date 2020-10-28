---
uid: Microsoft.Quantum.Canon.ApplyIfElseRC
title: Операция Апплифелсерк
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseRC
qsharp.summary: Applies one of two controllable operations, depending on the value of a classical result.
ms.openlocfilehash: 45bd0f46fb2e28c5c9aaa21cb7ec065baf279d2a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718114"
---
# <a name="applyifelserc-operation"></a>Операция Апплифелсерк

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет одну из двух контролируемых операций в зависимости от значения классического результата.

```qsharp
operation ApplyIfElseRC<'T, 'U> (result : Result, (zeroOp : ('T => Unit is Ctl), zeroInput : 'T), (oneOp : ('U => Unit is Ctl), oneInput : 'U)) : Unit
```


## <a name="description"></a>Описание

Учитывая результат `result` , применяет операцию `zeroOp` с в `zeroInput` качестве входных данных, если равен `result` `Zero` , и применяется, `oneOp(oneInput)` когда `result == One` .

## <a name="input"></a>Входные данные

### <a name="result--__invalidresult__"></a>результат: __недопустимо <Result>__

Результат измерения, используемый для определения `zeroOp` применения или `oneOp` .


### <a name="zeroop--t--unit-ctl"></a>Зеруп: 'T = список CTL для [единицы](xref:microsoft.quantum.lang-ref.unit)>

Управляемая операция, применяемая при `result == Zero` .


### <a name="zeroinput--t"></a>Зероинпут: 'T

Входные данные, которые должны быть предоставлены в `zeroOp` when `result == Zero` .


### <a name="oneop--u--unit-ctl"></a>Онеоп: "U = список доверия для [единицы](xref:microsoft.quantum.lang-ref.unit)>

Управляемая операция, применяемая при `result == One` .


### <a name="oneinput--u"></a>Онеинпут: ' U

Входные данные, которые должны быть предоставлены в `oneOp` when `result == One` .



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип входных данных операции `zeroOp` , которая должна применяться условно.
### <a name="u"></a>' U

Тип входных данных операции `oneOp` , которая должна применяться условно.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплифзеро](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [Microsoft. тактов. Canon. Апплифоне](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [Microsoft. тактов. Canon. Апплифелсерк](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [Microsoft. тактов. Canon. Апплифелсера](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [Microsoft. тактов. Canon. Апплифелсерка](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)