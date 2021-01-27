---
uid: Microsoft.Quantum.Simulation.InterpolateGeneratorSystems
title: Функция Интерполатеженераторсистемс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolateGeneratorSystems
qsharp.summary: Returns a `TimeDependentGeneratorSystem` representing the linear interpolation between two `GeneratorSystem`s.
ms.openlocfilehash: c56f1eaf13afb649777c0d9368e97d85996cc67b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842260"
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