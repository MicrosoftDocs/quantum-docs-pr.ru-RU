---
uid: Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates
title: Операция Естиматеоверлапбетвинстатес
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the squared overlap between the states prepared by each operation.
ms.openlocfilehash: e083d6da13b0780905bf365c7a428ebc9666ce9e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839716"
---
# <a name="estimateoverlapbetweenstates-operation"></a>Операция Естиматеоверлапбетвинстатес

Пространство имен: [Microsoft. тактов. charactering](xref:Microsoft.Quantum.Characterization)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии двух операций, каждый из которых подготавливает копии состояния, вычисляет квадрат перекрытия между состояниями, подготовленными каждой операцией.

```qsharp
operation EstimateOverlapBetweenStates (preparation1 : (Qubit[] => Unit is Adj), preparation2 : (Qubit[] => Unit is Adj), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a>Входные данные

### <a name="preparation1--qubit--unit--is-adj"></a>preparation1: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit) >

Первая из двух операций подготовки состояния для сравнения.


### <a name="preparation2--qubit--unit--is-adj"></a>preparation2: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit) >

Вторая из двух операций подготовки состояния для сравнения.


### <a name="nqubits--int"></a>Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)

Число Кубитс, для которых `commonPreparation` действует, `preparation1` и `preparation2` .


### <a name="nmeasurements--int"></a>Нмеасурементс: [int](xref:microsoft.quantum.lang-ref.int)

Количество измерений, используемых для оценки перекрытия.



## <a name="output--double"></a>Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>Remarks

Эта операция использует тест подкачки для поиска $ $ \бегин{алигн} \лефт | \braket{00\cdots 0 | V ^ {\дагжер} U | 00 \ кдотс 0} \ригхт | ^ 2 \енд{алигн} $ $ WHERE $U $ является единым представлением действия `preparation1` , а $V $ соответствует `preparation2` .

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. characters. Естиматереаловерлапбетвинстатес](xref:Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates)
- [Microsoft. тактов. characters. Естиматеимаговерлапбетвинстатес](xref:Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates)