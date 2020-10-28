---
uid: Microsoft.Quantum.ErrorCorrection.MeasureStabilizerGenerators
title: Операция Меасурестабилизерженераторс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: MeasureStabilizerGenerators
qsharp.summary: Measures the given set of generators of a stabilizer group.
ms.openlocfilehash: a3f48ff24a39d13a57f7a144e21d4e41bb8a8b49
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712262"
---
# <a name="measurestabilizergenerators-operation"></a>Операция Меасурестабилизерженераторс

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакеты [](https://nuget.org/packages/)


Измеряет заданный набор генераторов группы стабилизер.

```qsharp
operation MeasureStabilizerGenerators (stabilizerGroup : Pauli[][], logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister, gadget : ((Pauli[], Qubit[]) => Result)) : Microsoft.Quantum.ErrorCorrection.Syndrome
```


## <a name="input"></a>Входные данные

### <a name="stabilizergroup--pauli"></a>Стабилизерграуп: [Паули](xref:microsoft.quantum.lang-ref.pauli)[] []

Массив операторов Паули мултикубит.
Например, `stabilizerGroup[0]` представляет собой список однокубитных матриц Паули, продукт тензорные, который является генератором стабилизер.


### <a name="logicalregister--logicalregister"></a>Логикалрегистер: [логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Массив Кубитс, в котором определен код стабилизер.


### <a name="gadget--pauliqubit--__invalidresult__"></a>Мини-приложение: ( [Паули](xref:microsoft.quantum.lang-ref.pauli)[], [кубит](xref:microsoft.quantum.lang-ref.qubit)[]) __= <Result> Недопустимый__ > 

Операция, указывающая, как измерять оператор мултикубит Паули.



## <a name="output--syndrome"></a>Выходные данные: [синдром](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)

Результат измерений.

## <a name="remarks"></a>Remarks

Это не проверяет, работает ли данный набор генераторов.
В противном случае результат измерения может быть произвольным.