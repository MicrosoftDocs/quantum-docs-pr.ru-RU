---
uid: Microsoft.Quantum.Simulation.EstimateEnergy
title: Операция Естиматинерги
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EstimateEnergy
qsharp.summary: Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.
ms.openlocfilehash: 0a02a8aad891c45b184b9b18d4e9383236485940
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229500"
---
# <a name="estimateenergy-operation"></a>Операция Естиматинерги

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Выполняет подготовку состояния, применяя к `statePrepUnitary` выводимой оценке этапа входного состояния по отношению к `qpeUnitary` результирующему состоянию с помощью `phaseEstAlgorithm` .

```qsharp
operation EstimateEnergy (nQubits : Int, statePrepUnitary : (Qubit[] => Unit), qpeUnitary : (Qubit[] => Unit is Adj + Ctl), phaseEstAlgorithm : ((Microsoft.Quantum.Oracles.DiscreteOracle, Qubit[]) => Double)) : Double
```


## <a name="input"></a>Входные данные

### <a name="nqubits--int"></a>Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)

Число Кубитс, используемых для моделирования.


### <a name="stateprepunitary--qubit--unit"></a>Статепрепунитари: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Oracle, представляющий подготовку состояния для первоначального динамического генератора.


### <a name="qpeunitary--qubit--unit--is-adj--ctl"></a>Кпеунитари: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Oracle, представляющий отдельный оператор $U $ представляющие развитие времени $ \делта t $ в динамическом генераторе с состоянием заземления $ \кет{\фи} $ и состоянием заземления $E = \фи \\ , \делта t $.


### <a name="phaseestalgorithm--discreteoraclequbit--double"></a>Фасисталгорисм: ([дискретеоракле](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) => [double](xref:microsoft.quantum.lang-ref.double) 

Операция, выполняющая оценку этапа для данной отдельной операции.
Дополнительные сведения см. в статье [Оценка этапа итерации](/quantum/libraries/characterization#iterative-phase-estimation) .



## <a name="output--double"></a>Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)

Оценка $ \хат{\фи} $ в энергетическом состоянии Energy $ \фи $ от силы заземления генератора, представленного $U $.