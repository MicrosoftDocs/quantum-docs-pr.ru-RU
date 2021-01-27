---
uid: Microsoft.Quantum.Simulation.GeneratorIndex
title: Определяемый пользователем тип Женераториндекс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GeneratorIndex
qsharp.summary: >-
  Represents a single primitive term in the set of all dynamical generators, e.g. Hermitian operators, for which there exists a map from that generator to time-evolution by that generator, through `EvolutionSet`.

  The first element (Int[], Double[]) is indexes that single term -- For instance, the Pauli string XXY with coefficient 0.5 would be indexed by ([1,1,2], [0.5]). Alternatively, Hamiltonians parameterized by a continuous variable, such as X cos φ + Y sin φ, might for instance be represented by ([], [φ]). The second element indexes the subsystem on which the generator acts on.
ms.openlocfilehash: 762dac81ea0963443f0338cea1b879856c84b0ff
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858379"
---
# <a name="generatorindex-user-defined-type"></a>Определяемый пользователем тип Женераториндекс

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Представляет один примитивный термин в наборе всех динамических генераторов, например операторы Хермитиан, для которых существует соответствие от этого генератора до времени развития этого генератора с помощью `EvolutionSet` .

Первый элемент (int [], double []) — это индексы, в которых один термин — например, Паули строка КСКСИ с коэффициентом 0,5 будет индексироваться по ([1, 1, 2], [0,5]). Кроме того, Хамилтонианс, параметризованный с помощью непрерывной переменной, например X cos φ + Y Sin φ, может представлять экземпляр ([], [φ]). Второй элемент индексирует подсистему, в которой работает генератор.

```qsharp

newtype GeneratorIndex = ((Int[], Double[]), Int[]);
```



## <a name="example"></a>Пример

С помощью  <xref:microsoft.quantum.simulation.paulievolutionset> оператор $ \пи X_2 X_5 Y_9 $ представляется следующим образом:

```qsharp
let index = GeneratorIndex(([1, 1, 2], [PI()]), [2, 5, 9]);
```

## <a name="remarks"></a>Remarks

> [!WARNING]
> Интерпретация `GeneratorIndex` не определена, за исключением ссылки на конкретный набор генераторов.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. моделирование. эволюционный](xref:Microsoft.Quantum.Simulation.EvolutionSet)
- [Microsoft. тактов. моделирование. Паулиеволутионсет](xref:Microsoft.Quantum.Simulation.PauliEvolutionSet)