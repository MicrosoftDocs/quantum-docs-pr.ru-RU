---
uid: Microsoft.Quantum.ErrorCorrection.MeasureStabilizerGenerators
title: Операция Меасурестабилизерженераторс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: MeasureStabilizerGenerators
qsharp.summary: Measures the given set of generators of a stabilizer group.
ms.openlocfilehash: d7c8df079e49b2ce0a5106e430ef4060df85cdc4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98825753"
---
# <a name="measurestabilizergenerators-operation"></a>Операция Меасурестабилизерженераторс

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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


### <a name="gadget--pauliqubit--__invalidresult__"></a>Мини-приложение: ([Паули](xref:microsoft.quantum.lang-ref.pauli)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) __= <Result> Недопустимый__> 

Операция, указывающая, как измерять оператор мултикубит Паули.



## <a name="output--syndrome"></a>Выходные данные: [синдром](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)

Результат измерений.

## <a name="remarks"></a>Remarks

Это не проверяет, работает ли данный набор генераторов.
В противном случае результат измерения может быть произвольным.