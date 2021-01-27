---
uid: Microsoft.Quantum.Characterization.EstimateFrequencyA
title: Операция Естиматефрекуенциа
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateFrequencyA
qsharp.summary: Given a preparation that is adjointable and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.
ms.openlocfilehash: 6cca8dff70283e0d69441db8a5b31fb5bfb3082a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839913"
---
# <a name="estimatefrequencya-operation"></a>Операция Естиматефрекуенциа

Пространство имен: [Microsoft. тактов. charactering](xref:Microsoft.Quantum.Characterization)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Учитывая аджоинтабле и измерение подготовки, вы оцениваете частоту, с которой измерение завершается (Возвращает `Zero` ), выполняя заданное число испытаний.

```qsharp
operation EstimateFrequencyA (preparation : (Qubit[] => Unit is Adj), measurement : (Qubit[] => Result), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a>Входные данные

### <a name="preparation--qubit--unit--is-adj"></a>подготовка: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit) >

Операция аджоинтабле $P $, которая подготавливает заданное состояние $ \рхо $ к входному регистру.


### <a name="measurement--qubit--__invalidresult__"></a>Измерение: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = __недопустимый <Result>__> 

Операция $M $, представляющая интересующую вас единицу измерения.


### <a name="nqubits--int"></a>Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)

Количество Кубитс, для которых каждый из них является подготовительным и измеряется.


### <a name="nmeasurements--int"></a>Нмеасурементс: [int](xref:microsoft.quantum.lang-ref.int)

Количество случаев, когда измерение должно быть выполнено, чтобы оценить интересующую вас частоту.



## <a name="output--double"></a>Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)

Оценка $ \хат{п} $ частоты, с которой $M (P (\ket{00 \кдотс 0} \bra{00 \кдотс 0})) $ Returns `Zero` , полученный с помощью несмещенного биномиальное оценщика $ \хат{п} = n \_ {\упарров}/n \_ {\текст{меасурементс}} $, где $n \_ {\упарров} $ — это количество `Zero` наблюдаемых результатов.

## <a name="remarks"></a>Remarks

Для операций аджоинтабле определенные предположения, такие как вызов операции, будут подготавливать Кубитс в точно такое же состояние, что позволит целевым компьютерам выполнять оптимизацию производительности.