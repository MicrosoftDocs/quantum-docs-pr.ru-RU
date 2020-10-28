---
uid: Microsoft.Quantum.Simulation.GetGeneratorSystemFunction
title: Функция Жетженераторсистемфунктион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GetGeneratorSystemFunction
qsharp.summary: Retrieves the `GeneratorIndex` function in a `GeneratorSystem`.
ms.openlocfilehash: 60ebbdbd1020d41a54426377043fc0c84ceec504
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733536"
---
# <a name="getgeneratorsystemfunction-function"></a>Функция Жетженераторсистемфунктион

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакеты [](https://nuget.org/packages/)


Извлекает `GeneratorIndex` функцию в `GeneratorSystem` .

```qsharp
function GetGeneratorSystemFunction (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex)
```


## <a name="input"></a>Входные данные

### <a name="generatorsystem--generatorsystem"></a>Женераторсистем: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Необходимый объект `GeneratorSystem`.



## <a name="output--int---generatorindex"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int) -> [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Функция, которая индексирует каждый `GeneratorIndex` термин в хамилтониан.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. моделирование. Женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)
- [Microsoft. тактов. моделирование. Женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)