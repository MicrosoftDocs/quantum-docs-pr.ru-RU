---
uid: Microsoft.Quantum.Canon.ApplyIfElseBCA
title: Операция Апплифелсебка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseBCA
qsharp.summary: Applies one of two unitary operations, depending on the value of a classical bit.
ms.openlocfilehash: 0ebd086f4c8166a8d6b593200b0a3354c1420c6e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718197"
---
# <a name="applyifelsebca-operation"></a>Операция Апплифелсебка

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет одну из двух операций в зависимости от значения классического бита.

```qsharp
operation ApplyIfElseBCA<'T, 'U> (bit : Bool, (trueOp : ('T => Unit is Adj + Ctl), trueInput : 'T), (falseOp : ('U => Unit is Adj + Ctl), falseInput : 'U)) : Unit
```


## <a name="description"></a>Описание

Учитывая бит `bit` , применяет операцию `trueOp` с в `trueInput` качестве входных данных `bit` , если имеет значение `true` , и применяется, `falseOp(falseInput)` Если `bit` имеет значение `false` .

## <a name="input"></a>Входные данные

### <a name="bit--bool"></a>bit: [bool](xref:microsoft.quantum.lang-ref.bool)

Логическое значение, используемое для определения того, применяется ли оператор `trueOp` или `falseOp` .


### <a name="trueop--t--unit-adj--ctl"></a>Труеоп: 'T => [модульные](xref:microsoft.quantum.lang-ref.unit) года + CTL

Единая операция, применяемая, если `bit` имеет значение `true` .


### <a name="trueinput--t"></a>Труеинпут: 'T

Входные данные, которые должны быть предоставлены, `trueOp` Если `bit` имеет значение `true` .


### <a name="falseop--u--unit-adj--ctl"></a>Фалсеоп: "U => [единицы](xref:microsoft.quantum.lang-ref.unit) + CTL

Единая операция, применяемая, если `bit` имеет значение `false` .


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