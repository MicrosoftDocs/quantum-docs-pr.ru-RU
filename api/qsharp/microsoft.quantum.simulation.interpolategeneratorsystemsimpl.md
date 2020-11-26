---
uid: Microsoft.Quantum.Simulation.InterpolateGeneratorSystemsImpl
title: Функция Интерполатеженераторсистемсимпл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolateGeneratorSystemsImpl
qsharp.summary: Linearly interpolates between two `GeneratorSystems` according to a schedule parameter `s` between 0 and 1 (inclusive).
ms.openlocfilehash: 1ca9580ba603db8fee40e008a7ea51cb7a04d7d3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229228"
---
# <a name="interpolategeneratorsystemsimpl-function"></a>Функция Интерполатеженераторсистемсимпл

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Линейная интерполяция между двумя в `GeneratorSystems` соответствии с параметром расписания `s` от 0 до 1 (включительно).

```qsharp
function InterpolateGeneratorSystemsImpl (schedule : Double, generatorSystemStart : Microsoft.Quantum.Simulation.GeneratorSystem, generatorSystemEnd : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>Входные данные

### <a name="schedule--double"></a>Расписание: [Double](xref:microsoft.quantum.lang-ref.double)

Параметр расписания $s \ин [0, 1] $.


### <a name="generatorsystemstart--generatorsystem"></a>Женераторсистемстарт: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Начало `GeneratorSystem` .


### <a name="generatorsystemend--generatorsystem"></a>Женераторсистеменд: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Конец `GeneratorSystem` .



## <a name="output--generatorsystem"></a>Выходные данные: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Объект, `GeneratorSystem` представляющий систему, которая является суммой систем генератора входных данных с весовым коэффициентом $ (1-s) $ ON `generatorSystemStart` и весом $s $ On `generatorSystemEnd` .

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. моделирование. Женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)