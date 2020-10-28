---
uid: Microsoft.Quantum.MachineLearning.CyclicEntanglingLayer
title: Функция Циклицентанглинглайер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CyclicEntanglingLayer
qsharp.summary: Returns an array of singly controlled rotations along a given axis, arranged cyclically across a register of qubits, and parameterized by distinct model parameters.
ms.openlocfilehash: 6e0f5057b35baefe2677126ba70ee4fddde7d4db
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731112"
---
# <a name="cyclicentanglinglayer-function"></a>Функция Циклицентанглинглайер

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакеты [](https://nuget.org/packages/)


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