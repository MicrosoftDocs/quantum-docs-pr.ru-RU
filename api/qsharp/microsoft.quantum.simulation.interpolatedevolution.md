---
uid: Microsoft.Quantum.Simulation.InterpolatedEvolution
title: Функция Интерполатедеволутион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolatedEvolution
qsharp.summary: Interpolates between two generators with a uniform schedule, returning an operation that applies simulated evolution under the resulting time-dependent generator to a qubit register.
ms.openlocfilehash: 4d2e04513c96c6e5f41e85f1df685e91e2973098
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858094"
---
# <a name="interpolatedevolution-function"></a>Функция Интерполатедеволутион

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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



## <a name="output--qubit--unit--is-adj--ctl"></a>Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit)  ">" + CTL



## <a name="remarks"></a>Remarks

Если время интерполяции выбрано в соответствии с условиями адиабатик, эта функция возвращает операцию, которая выполняет подготовку адиабатик State для финального динамического генератора.