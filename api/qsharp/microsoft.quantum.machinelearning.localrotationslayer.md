---
uid: Microsoft.Quantum.MachineLearning.LocalRotationsLayer
title: Функция Локалротатионслайер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LocalRotationsLayer
qsharp.summary: Returns an array of uncontrolled (single-qubit) rotations along a given axis, with one rotation for each qubit in a register, parameterized by distinct model parameters.
ms.openlocfilehash: 8a3557f76d5d7a7b6375e5640cf6d11172cd38a6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732913"
---
# <a name="localrotationslayer-function"></a>Функция Локалротатионслайер

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакеты [](https://nuget.org/packages/)


Возвращает массив неуправляемых (одинарных кубит) поворотов вдоль заданной оси с одним поворотом для каждого кубит в регистре, параметризованным разными параметрами модели.

```qsharp
function LocalRotationsLayer (nQubits : Int, axis : Pauli) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a>Входные данные

### <a name="nqubits--int"></a>Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)

Число Кубитс, обрабатываемых данным слоем.


### <a name="axis--pauli"></a>ось: [Паули](xref:microsoft.quantum.lang-ref.pauli)

Ось вращения для каждого вращения в заданном слое.



## <a name="output--controlledrotation"></a>Выходные данные: [контролледротатион](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]

Массив управляемых поворотов относительно заданной оси, по одному на каждый из `nQubits` Кубитс.