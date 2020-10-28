---
uid: Microsoft.Quantum.Canon.ApplyIfElseBC
title: Операция Апплифелсебк
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseBC
qsharp.summary: Applies one of two controllable operations, depending on the value of a classical bit.
ms.openlocfilehash: 032d92484dc96481cb981d9d8acfeed248a9116d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729577"
---
# <a name="applyifelsebc-operation"></a>Операция Апплифелсебк

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет одну из двух контролируемых операций в зависимости от значения классического бита.

```qsharp
operation ApplyIfElseBC<'T, 'U> (bit : Bool, (trueOp : ('T => Unit is Ctl), trueInput : 'T), (falseOp : ('U => Unit is Ctl), falseInput : 'U)) : Unit
```


## <a name="description"></a>Описание

Учитывая бит `bit` , применяет операцию `trueOp` с в `trueInput` качестве входных данных `bit` , если имеет значение `true` , и применяется, `falseOp(falseInput)` Если `bit` имеет значение `false` .

## <a name="input"></a>Входные данные

### <a name="bit--bool"></a>bit: [bool](xref:microsoft.quantum.lang-ref.bool)

Логическое значение, используемое для определения того, применяется ли оператор `trueOp` или `falseOp` .


### <a name="trueop--t--unit-ctl"></a>Труеоп: 'T = список CTL для [единицы](xref:microsoft.quantum.lang-ref.unit)>

Управляемая операция, применяемая `bit` , если имеет значение `true` .


### <a name="trueinput--t"></a>Труеинпут: 'T

Входные данные, которые должны быть предоставлены, `trueOp` Если `bit` имеет значение `true` .


### <a name="falseop--u--unit-ctl"></a>Фалсеоп: "U = список доверия для [единицы](xref:microsoft.quantum.lang-ref.unit)>

Управляемая операция, применяемая `bit` , если имеет значение `false` .


### <a name="falseinput--u"></a>Фалсеинпут: ' U

Входные данные, которые должны быть предоставлены, `falseOp` Если `bit` имеет значение `false` .



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип входных данных операции `trueOp` , которая должна применяться условно.
### <a name="u"></a>' U

Тип входных данных операции `falseOp` , которая должна применяться условно.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплифзеро](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [Microsoft. тактов. Canon. Апплифоне](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [Microsoft. тактов. Canon. Апплифелсерк](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [Microsoft. тактов. Canon. Апплифелсера](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [Microsoft. тактов. Canon. Апплифелсерка](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)