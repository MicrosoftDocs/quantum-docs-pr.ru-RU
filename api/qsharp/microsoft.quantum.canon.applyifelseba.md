---
uid: Microsoft.Quantum.Canon.ApplyIfElseBA
title: Операция Апплифелсеба
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseBA
qsharp.summary: Applies one of two adjointable operations, depending on the value of a classical bit.
ms.openlocfilehash: 74d43344481c5a808e84ce9c9e36fa3e83cd0d89
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218671"
---
# <a name="applyifelseba-operation"></a>Операция Апплифелсеба

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет одну из двух операций аджоинтабле в зависимости от значения классического бита.

```qsharp
operation ApplyIfElseBA<'T, 'U> (bit : Bool, (trueOp : ('T => Unit is Adj), trueInput : 'T), (falseOp : ('U => Unit is Adj), falseInput : 'U)) : Unit is Adj
```


## <a name="description"></a>Описание

Учитывая бит `bit` , применяет операцию `trueOp` с в `trueInput` качестве входных данных `bit` , если имеет значение `true` , и применяется, `falseOp(falseInput)` Если `bit` имеет значение `false` .

## <a name="input"></a>Входные данные

### <a name="bit--bool"></a>bit: [bool](xref:microsoft.quantum.lang-ref.bool)

Логическое значение, используемое для определения того, применяется ли оператор `trueOp` или `falseOp` .


### <a name="trueop--t--unit--is-adj"></a>Труеоп: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  Нагода

Операция аджоинтабле, применяемая, если `bit` имеет значение `true` .


### <a name="trueinput--t"></a>Труеинпут: 'T

Входные данные, которые должны быть предоставлены, `trueOp` Если `bit` имеет значение `true` .


### <a name="falseop--u--unit--is-adj"></a>Фалсеоп: "U = [единица](xref:microsoft.quantum.lang-ref.unit) > является просуммой

Операция аджоинтабле, применяемая, если `bit` имеет значение `false` .


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