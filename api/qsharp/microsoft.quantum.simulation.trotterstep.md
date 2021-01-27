---
uid: Microsoft.Quantum.Simulation.TrotterStep
title: Функция Троттерстеп
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterStep
qsharp.summary: Implements a single time-step of time-evolution by the system described in an `EvolutionGenerator` using a Trotter–Suzuki decomposition.
ms.openlocfilehash: 4c0e7dd89b1beae9fb6a35ae5b8d16e09d355ab8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854709"
---
# <a name="trotterstep-function"></a>Функция Троттерстеп

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Реализует однократный шаг за пределом времени с помощью системы, описанной в `EvolutionGenerator` с использованием декомпозиции Троттер – Сузуки.

```qsharp
function TrotterStep (evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, trotterOrder : Int, trotterStepSize : Double) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="evolutiongenerator--evolutiongenerator"></a>Еволутионженератор: [еволутионженератор](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)

Полное описание системы для имитации.


### <a name="trotterorder--int"></a>Троттерордер: [int](xref:microsoft.quantum.lang-ref.int)

Порядок Троттер интегратора. Это должно быть либо 1, либо четное число.


### <a name="trotterstepsize--double"></a>Троттерстепсизе: [Double](xref:microsoft.quantum.lang-ref.double)

Продолжительность имитации времени — развитие в одном Троттер шаге.



## <a name="output--qubit--unit--is-adj--ctl"></a>Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit)  ">" + CTL

Единая операция, которая приблизительно составляет один шаг времени — развитие длительности `trotterStepSize` .

## <a name="remarks"></a>Remarks

Дополнительные сведения о декомпозиции Троттер – Сузуки см. в разделе [упорядочение по времени](/quantum/libraries/control-flow#time-ordered-composition).