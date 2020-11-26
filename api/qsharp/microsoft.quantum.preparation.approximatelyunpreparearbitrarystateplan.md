---
uid: Microsoft.Quantum.Preparation.ApproximatelyUnprepareArbitraryStatePlan
title: Функция Аппроксимателюнпрепареарбитраристатеплан
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: ApproximatelyUnprepareArbitraryStatePlan
qsharp.summary: Implementation step of arbitrary state preparation procedure.
ms.openlocfilehash: 2aab8b7a21ded729e90695c82709901bfacc18e7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226508"
---
# <a name="approximatelyunpreparearbitrarystateplan-function"></a>Функция Аппроксимателюнпрепареарбитраристатеплан

Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Этап реализации процедуры подготовки произвольного состояния.

```qsharp
function ApproximatelyUnprepareArbitraryStatePlan (tolerance : Double, coefficients : Microsoft.Quantum.Math.ComplexPolar[], (rngControl : Range, idxTarget : Int)) : (Qubit[] => Unit is Adj + Ctl)[]
```


## <a name="input"></a>Входные данные

### <a name="tolerance--double"></a>Допуск: [Double](xref:microsoft.quantum.lang-ref.double)




### <a name="coefficients--complexpolar"></a>коэффициенты: [комплексполар](xref:Microsoft.Quantum.Math.ComplexPolar)[]




### <a name="rngcontrol--range"></a>Рнгконтрол: [диапазон](xref:microsoft.quantum.lang-ref.range)




### <a name="idxtarget--int"></a>Идкстаржет: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--qubit--unit--is-adj--ctl"></a>Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit) > — "года + CTL" []



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. подготовка. Препареарбитраристате](xref:Microsoft.Quantum.Preparation.PrepareArbitraryState)
- [Microsoft. тактов. Canon. Мултиплекспаули](xref:Microsoft.Quantum.Canon.MultiplexPauli)