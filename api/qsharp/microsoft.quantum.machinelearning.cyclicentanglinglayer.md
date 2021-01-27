---
uid: Microsoft.Quantum.MachineLearning.CyclicEntanglingLayer
title: Функция Циклицентанглинглайер
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CyclicEntanglingLayer
qsharp.summary: Returns an array of singly controlled rotations along a given axis, arranged cyclically across a register of qubits, and parameterized by distinct model parameters.
ms.openlocfilehash: 5d0af0a60217b69dc7eb8ece8952f2a7f0c09280
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847381"
---
# <a name="cyclicentanglinglayer-function"></a>Функция Циклицентанглинглайер

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Возвращает массив однонаправленных поворотов вдоль заданной оси, организованных циклически по регистру Кубитс и параметризованных с помощью отдельных параметров модели.

```qsharp
function CyclicEntanglingLayer (nQubits : Int, axis : Pauli, stride : Int) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a>Входные данные

### <a name="nqubits--int"></a>Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)

Число Кубитс, обрабатываемых данным слоем.


### <a name="axis--pauli"></a>ось: [Паули](xref:microsoft.quantum.lang-ref.pauli)

Ось вращения для каждого вращения в заданном слое.


### <a name="stride--int"></a>шаг: [int](xref:microsoft.quantum.lang-ref.int)

Разделение между целевым индексом и элементами управления для каждого вращения.



## <a name="output--controlledrotation"></a>Выходные данные: [контролледротатион](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]

Массив кубит управляемых поворотов, которые циклически располагаются в регистре `nQubits` Кубитс.

## <a name="example"></a>Пример

Следующие эквивалентны:

```qsharp
let layer = CyclicEntanglingLayer(3, PauliX, 2);
let layer = [
    ControlledRotation((0, [2]), PauliX, 0),
    ControlledRotation((1, [0]), PauliX, 1),
    ControlledRotation((2, [1]), PauliX, 2)
];
```