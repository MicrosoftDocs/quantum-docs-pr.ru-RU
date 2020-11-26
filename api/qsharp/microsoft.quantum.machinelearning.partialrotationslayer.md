---
uid: Microsoft.Quantum.MachineLearning.PartialRotationsLayer
title: Функция Партиалротатионслайер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: PartialRotationsLayer
qsharp.summary: Returns an array of single-qubit rotations along a given axis, parameterized by distinct model parameters.
ms.openlocfilehash: ade0640b07f633982e98d5d02239fa205909bcce
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196248"
---
# <a name="partialrotationslayer-function"></a>Функция Партиалротатионслайер

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Возвращает массив однокубитных поворотов вдоль заданной оси, параметризованных разными параметрами модели.

```qsharp
function PartialRotationsLayer (idxsQubits : Int[], axis : Pauli) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a>Входные данные

### <a name="idxsqubits--int"></a>Идксскубитс: [int](xref:microsoft.quantum.lang-ref.int)[]

Индексы для Кубитс, которые будут использоваться в качестве целевых объектов для каждого вращения.


### <a name="axis--pauli"></a>ось: [Паули](xref:microsoft.quantum.lang-ref.pauli)

Ось вращения для каждого вращения в заданном слое.



## <a name="output--controlledrotation"></a>Выходные данные: [контролледротатион](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]

Массив управляемых поворотов относительно заданной оси, по одному на каждый из `nQubits` Кубитс.