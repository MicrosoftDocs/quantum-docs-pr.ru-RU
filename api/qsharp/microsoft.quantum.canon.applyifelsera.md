---
uid: Microsoft.Quantum.Canon.ApplyIfElseRA
title: Операция Апплифелсера
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseRA
qsharp.summary: Applies one of two adjointable operations, depending on the value of a classical result.
ms.openlocfilehash: 0a7683adfa15f787f96c7ae55f94e2c52426df75
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845014"
---
# <a name="applyifelsera-operation"></a>Операция Апплифелсера

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет одну из двух операций аджоинтабле в зависимости от значения классического результата.

```qsharp
operation ApplyIfElseRA<'T, 'U> (result : Result, (zeroOp : ('T => Unit is Adj), zeroInput : 'T), (oneOp : ('U => Unit is Adj), oneInput : 'U)) : Unit is Adj
```


## <a name="description"></a>Описание

Учитывая результат `result` , применяет операцию `zeroOp` с в `zeroInput` качестве входных данных, если равен `result` `Zero` , и применяется, `oneOp(oneInput)` когда `result == One` .

## <a name="input"></a>Входные данные

### <a name="result--__invalidresult__"></a>результат: __недопустимо <Result>__

Результат измерения, используемый для определения `zeroOp` применения или `oneOp` .


### <a name="zeroop--t--unit--is-adj"></a>Зеруп: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  Нагода

Операция аджоинтабле, применяемая при `result == Zero` .


### <a name="zeroinput--t"></a>Зероинпут: 'T

Входные данные, которые должны быть предоставлены в `zeroOp` when `result == Zero` .


### <a name="oneop--u--unit--is-adj"></a>Онеоп: "U = [единица](xref:microsoft.quantum.lang-ref.unit) > является просуммой

Операция аджоинтабле, применяемая при `result == One` .


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