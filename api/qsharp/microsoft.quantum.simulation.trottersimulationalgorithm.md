---
uid: Microsoft.Quantum.Simulation.TrotterSimulationAlgorithm
title: Функция Троттерсимулатионалгорисм
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterSimulationAlgorithm
qsharp.summary: '`SimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate the time-evolution operator _exp(-iHt)_.'
ms.openlocfilehash: aa8338ab359441765db72a12f84a3a51e5bee3ce
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192542"
---
# <a name="trottersimulationalgorithm-function"></a>Функция Троттерсимулатионалгорисм

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


`SimulationAlgorithm` функция, использующая декомпозицию Троттер – Сузуки для приближения оператора времени _(-ИХТ)_.

```qsharp
function TrotterSimulationAlgorithm (trotterStepSize : Double, trotterOrder : Int) : Microsoft.Quantum.Simulation.SimulationAlgorithm
```


## <a name="input"></a>Входные данные

### <a name="trotterstepsize--double"></a>Троттерстепсизе: [Double](xref:microsoft.quantum.lang-ref.double)

Продолжительность имитации времени — развитие в одном Троттер шаге.


### <a name="trotterorder--int"></a>Троттерордер: [int](xref:microsoft.quantum.lang-ref.int)

Порядок Троттер интегратора. Это должно быть либо 1, либо четное число.



## <a name="output--simulationalgorithm"></a>Выходные данные: [симулатионалгорисм](xref:Microsoft.Quantum.Simulation.SimulationAlgorithm)

Тип `SimulationAlgorithm`.