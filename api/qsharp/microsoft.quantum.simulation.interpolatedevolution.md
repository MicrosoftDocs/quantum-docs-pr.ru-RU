---
uid: Microsoft.Quantum.Simulation.InterpolatedEvolution
title: Функция Интерполатедеволутион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolatedEvolution
qsharp.summary: Interpolates between two generators with a uniform schedule, returning an operation that applies simulated evolution under the resulting time-dependent generator to a qubit register.
ms.openlocfilehash: 18026b9872f6a3344a1e5c2122f55927975ccb59
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710582"
---
# <a name="interpolatedevolution-function"></a>Функция Интерполатедеволутион

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакеты [](https://nuget.org/packages/)


Выполняет интерполяцию между двумя генераторами с единым расписанием, возвращая операцию, которая применяет смоделированное развитие в рамках генератора, зависящего от времени, к кубит регистру.

```qsharp
function InterpolatedEvolution (interpolationTime : Double, evolutionGeneratorStart : Microsoft.Quantum.Simulation.EvolutionGenerator, evolutionGeneratorEnd : Microsoft.Quantum.Simulation.EvolutionGenerator, timeDependentSimulationAlgorithm : Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="interpolationtime--double"></a>Интерполатионтиме: [Double](xref:microsoft.quantum.lang-ref.double)

Время для выполнения интерполяции.


### <a name="evolutiongeneratorstart--evolutiongenerator"></a>Еволутионженераторстарт: [еволутионженератор](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)

Начальный генератор для моделирования развития.


### <a name="evolutiongeneratorend--evolutiongenerator"></a>Еволутионженераторенд: [еволутионженератор](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)

Окончательный генератор для моделирования развития.


### <a name="timedependentsimulationalgorithm--timedependentsimulationalgorithm"></a>Тимедепендентсимулатионалгорисм: [тимедепендентсимулатионалгорисм](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)

Алгоритм моделирования, зависящий от времени, который будет использоваться для моделирования развития во время единообразия расписания интерполяции.



## <a name="output--qubit--unit-adj--ctl"></a>Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL



## <a name="remarks"></a>Remarks

Если время интерполяции выбрано в соответствии с условиями адиабатик, эта функция возвращает операцию, которая выполняет подготовку адиабатик State для финального динамического генератора.