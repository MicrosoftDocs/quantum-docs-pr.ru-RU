---
uid: Microsoft.Quantum.Research.Chemistry.JWOptimizedFermionEvolutionFunction
title: Функция Жвоптимизедфермионеволутионфунктион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JWOptimizedFermionEvolutionFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the JWOptimized basis.
ms.openlocfilehash: 952f3dc4ab0595ace0ee34c040cb21969afa111f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710805"
---
# <a name="jwoptimizedfermionevolutionfunction-function"></a>Функция Жвоптимизедфермионеволутионфунктион

Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)

Пакеты [](https://nuget.org/packages/)


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