---
uid: Microsoft.Quantum.ErrorCorrection.MeasureStabilizerGenerators
title: Операция Меасурестабилизерженераторс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: MeasureStabilizerGenerators
qsharp.summary: Measures the given set of generators of a stabilizer group.
ms.openlocfilehash: 6c048c17df21d1026dc671f30d72a13ed8d8b7f5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200634"
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

## <a name="remarks"></a>Комментарии

Это не проверяет, работает ли данный набор генераторов.
В противном случае результат измерения может быть произвольным.