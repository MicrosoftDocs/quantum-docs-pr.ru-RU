---
uid: Microsoft.Quantum.Research.Chemistry.JWOptimizedFermionEvolutionFunction
title: Функция Жвоптимизедфермионеволутионфунктион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JWOptimizedFermionEvolutionFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the JWOptimized basis.
ms.openlocfilehash: d70bea8fcb5bd82ddad6dcd2b67c3eb178283bb3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857867"
---
# <a name="jwoptimizedfermionevolutionfunction-function"></a>Функция Жвоптимизедфермионеволутионфунктион

Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)

Пакет: [Microsoft. тактов. Research. Химия](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)


Представляет динамический генератор как набор моделирующих шлюзов и расширение на основе Жвоптимизед.

```qsharp
function JWOptimizedFermionEvolutionFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex, parityQubit : Qubit) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a>Входные данные

### <a name="generatorindex--generatorindex"></a>Женераториндекс: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Индекс генератора, который должен быть представлен как единое развитие на основе Жвоптимизед.


### <a name="parityqubit--qubit"></a>Паритикубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Кубит, определяющий знак времени — развитие.



## <a name="output--evolutionunitary"></a>Выходные данные: [еволутионунитари](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)

`EvolutionUnitary`Представление, представляющее время развития термина, на который ссылается "женераториндекс.