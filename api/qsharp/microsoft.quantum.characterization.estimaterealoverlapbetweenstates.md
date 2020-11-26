---
uid: Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates
title: Операция Естиматереаловерлапбетвинстатес
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateRealOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the real part of the overlap between the states prepared by each operation.
ms.openlocfilehash: d9f569ceffc16f377189dc94035213b9075609cc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216189"
---
# <a name="estimaterealoverlapbetweenstates-operation"></a>Операция Естиматереаловерлапбетвинстатес

Пространство имен: [Microsoft. тактов. charactering](xref:Microsoft.Quantum.Characterization)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии двух операций, каждый из которых подготавливает копии состояния, оценивает реальную часть перекрытия между состояниями, подготовленными каждой операцией.

```qsharp
operation EstimateRealOverlapBetweenStates (commonPreparation : (Qubit[] => Unit is Adj), preparation1 : (Qubit[] => Unit is Adj + Ctl), preparation2 : (Qubit[] => Unit is Adj + Ctl), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a>Входные данные

### <a name="commonpreparation--qubit--unit--is-adj"></a>Коммонпрепаратион: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit) >

Операция, которая подготавливает фиксированное состояние ввода.


### <a name="preparation1--qubit--unit--is-adj--ctl"></a>preparation1: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Первая из двух операций подготовки состояния для сравнения.


### <a name="preparation2--qubit--unit--is-adj--ctl"></a>preparation2: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Вторая из двух операций подготовки состояния для сравнения.


### <a name="nqubits--int"></a>Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)

Число Кубитс, для которых `commonPreparation` действует, `preparation1` и `preparation2` .


### <a name="nmeasurements--int"></a>Нмеасурементс: [int](xref:microsoft.quantum.lang-ref.int)

Количество измерений, используемых для оценки перекрытия.



## <a name="output--double"></a>Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>Комментарии

Эта операция использует тест Хадамард для поиска действительной части $ $ \бегин{алигн} \бракет{\пси | V ^ {\дагжер} U | \пси} \енд{алигн} $ $, где $ \кет{\пси} $ — это состояние, подготовленное `commonPreparation` , $U $ является единым представлением действия `preparation1` , а $V $ соответствует `preparation2` .

## <a name="references"></a>Ссылки

- Ахаронов *et al.* [Куант-pH/0511096](https://arxiv.org/abs/quant-ph/0511096).

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. characters. Естиматеимаговерлапбетвинстатес](xref:Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates)
- [Microsoft. тактов. characters. Естиматеоверлапбетвинстатес](xref:Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates)