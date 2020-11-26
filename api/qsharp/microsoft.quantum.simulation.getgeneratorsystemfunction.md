---
uid: Microsoft.Quantum.Simulation.GetGeneratorSystemFunction
title: Функция Жетженераторсистемфунктион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GetGeneratorSystemFunction
qsharp.summary: Retrieves the `GeneratorIndex` function in a `GeneratorSystem`.
ms.openlocfilehash: 28e3c12d0ae0b08fc368c25eeb6f38d2834ca912
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229313"
---
# <a name="getgeneratorsystemfunction-function"></a>Функция Жетженераторсистемфунктион

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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