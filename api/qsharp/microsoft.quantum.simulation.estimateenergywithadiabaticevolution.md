---
uid: Microsoft.Quantum.Simulation.EstimateEnergyWithAdiabaticEvolution
title: Операция Естиматинергивисадиабатицеволутион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EstimateEnergyWithAdiabaticEvolution
qsharp.summary: Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state, followed by adiabatic state preparation using a `adiabaticUnitary`, and finally phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.
ms.openlocfilehash: b279d35418b8f013ad0d72e9a980c9bf6ce0689a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225335"
---
# <a name="estimateenergywithadiabaticevolution-operation"></a>Операция Естиматинергивисадиабатицеволутион

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Выполняет подготовку состояния, применяя к `statePrepUnitary` автоматически выделенному входному состоянию, за которым следует подготовка состояния адиабатик с помощью `adiabaticUnitary` , и, наконец, Оценка этапа по отношению к `qpeUnitary` результирующему состоянию с помощью `phaseEstAlgorithm` .

```qsharp
operation EstimateEnergyWithAdiabaticEvolution (nQubits : Int, statePrepUnitary : (Qubit[] => Unit), adiabaticUnitary : (Qubit[] => Unit), qpeUnitary : (Qubit[] => Unit is Adj + Ctl), phaseEstAlgorithm : ((Microsoft.Quantum.Oracles.DiscreteOracle, Qubit[]) => Double)) : Double
```


## <a name="input"></a>Входные данные

### <a name="nqubits--int"></a>Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)

Число Кубитс, используемых для моделирования.


### <a name="stateprepunitary--qubit--unit"></a>Статепрепунитари: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Oracle, представляющий подготовку состояния для первоначального динамического генератора.


### <a name="adiabaticunitary--qubit--unit"></a>Адиабатикунитари: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Oracle, представляющий алгоритм эволюции адиабатик, который используется для реализации очистки до окончательного состояния алгоритма.


### <a name="qpeunitary--qubit--unit--is-adj--ctl"></a>Кпеунитари: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Oracle, представляющий отдельный оператор $U $ представляющие развитие времени $ \делта t $ в динамическом генераторе с состоянием заземления $ \кет{\фи} $ и состоянием заземления $E = \фи \\ , \делта t $.


### <a name="phaseestalgorithm--discreteoraclequbit--double"></a>Фасисталгорисм: ([дискретеоракле](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) => [double](xref:microsoft.quantum.lang-ref.double) 

Операция, выполняющая оценку этапа для данной отдельной операции.
Дополнительные сведения см. в статье [Оценка этапа итерации](/quantum/libraries/characterization#iterative-phase-estimation) .



## <a name="output--double"></a>Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)

Оценочное значение $ \хат{\фи} $ от земли $ \фи $ генератора, представленного $U $.