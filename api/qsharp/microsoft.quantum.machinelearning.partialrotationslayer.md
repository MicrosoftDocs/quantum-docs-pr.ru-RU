---
uid: Microsoft.Quantum.MachineLearning.PartialRotationsLayer
title: Функция Партиалротатионслайер
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: PartialRotationsLayer
qsharp.summary: Returns an array of single-qubit rotations along a given axis, parameterized by distinct model parameters.
ms.openlocfilehash: e230df9b28c59e1d532d5b36adf90efa01f0f33e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852921"
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