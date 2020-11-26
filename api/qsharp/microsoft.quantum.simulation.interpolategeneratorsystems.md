---
uid: Microsoft.Quantum.Simulation.InterpolateGeneratorSystems
title: Функция Интерполатеженераторсистемс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolateGeneratorSystems
qsharp.summary: Returns a `TimeDependentGeneratorSystem` representing the linear interpolation between two `GeneratorSystem`s.
ms.openlocfilehash: ee47637996313fe1b77c76f00b08417dac956247
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230588"
---
# <a name="interpolategeneratorsystems-function"></a>Функция Интерполатеженераторсистемс

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает значение, `TimeDependentGeneratorSystem` представляющее линейную интерполяцию между двумя `GeneratorSystem` s.

```qsharp
function InterpolateGeneratorSystems (generatorSystemStart : Microsoft.Quantum.Simulation.GeneratorSystem, generatorSystemEnd : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem
```


## <a name="input"></a>Входные данные

### <a name="generatorsystemstart--generatorsystem"></a>Женераторсистемстарт: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Начало `GeneratorSystem` .


### <a name="generatorsystemend--generatorsystem"></a>Женераторсистеменд: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Конец `GeneratorSystem` .



## <a name="output--timedependentgeneratorsystem"></a>Выходные данные: [тимедепендентженераторсистем](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)

Объект, `TimeDependentGeneratorSystem` представляющий систему, которая является суммой систем генератора входных данных с весовым коэффициентом $ (1-s) $ ON `generatorSystemStart` и весом $s $ On `generatorSystemEnd` .

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. моделирование. Женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)
- [Microsoft. тактов. моделирование. Тимедепендентженераторсистем](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)