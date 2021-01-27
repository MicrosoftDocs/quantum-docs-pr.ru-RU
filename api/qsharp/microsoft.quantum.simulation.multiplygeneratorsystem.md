---
uid: Microsoft.Quantum.Simulation.MultiplyGeneratorSystem
title: Функция Мултиплиженераторсистем
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: MultiplyGeneratorSystem
qsharp.summary: Multiplies the coefficient of all terms in a `GeneratorSystem`.
ms.openlocfilehash: cebd08c86ad8a3793ba7d0e9ce241d7a1ef046ae
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858495"
---
# <a name="multiplygeneratorsystem-function"></a>Функция Мултиплиженераторсистем

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Умножает коэффициент всех терминов в `GeneratorSystem` .

```qsharp
function MultiplyGeneratorSystem (multiplier : Double, generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>Входные данные

### <a name="multiplier--double"></a>множитель: [Double](xref:microsoft.quantum.lang-ref.double)

Коэффициент коэффициента.


### <a name="generatorsystem--generatorsystem"></a>Женераторсистем: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Умножаемый `GeneratorSystem`.



## <a name="output--generatorsystem"></a>Выходные данные: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Объект, `GeneratorSystem` представляющий систему с коэффициентами `multiplier` увеличения.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. моделирование. Женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)