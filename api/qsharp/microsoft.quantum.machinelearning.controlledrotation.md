---
uid: Microsoft.Quantum.MachineLearning.ControlledRotation
title: Определяемый пользователем тип Контролледротатион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ControlledRotation
qsharp.summary: Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.
ms.openlocfilehash: afc425c16ab550fd414e656484c9ff6f0f8f3ef4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711365"
---
# <a name="controlledrotation-user-defined-type"></a>Определяемый пользователем тип Контролледротатион

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакеты [](https://nuget.org/packages/)


Описывает управляемый поворот в терминах целевого объекта и индексов управления, ось вращения и индекс в векторе параметров модели.

```qsharp

newtype ControlledRotation = ((TargetIndex : Int, ControlIndices : Int[]), Axis : Pauli, ParameterIndex : Int);
```



## <a name="named-items"></a>Именованные элементы

### <a name="targetindex--int"></a>Таржетиндекс: [int](xref:microsoft.quantum.lang-ref.int)

Индекс целевого кубит для этого управляемого вращения.
### <a name="controlindices--int"></a>Контролиндицес: [int](xref:microsoft.quantum.lang-ref.int)[]

Массив элементов управления, кубит индексы для этого вращения.
### <a name="axis--pauli"></a>Ось: [Паули](xref:microsoft.quantum.lang-ref.pauli)

Ось для этого вращения.
### <a name="parameterindex--int"></a>ParameterIndex: [int](xref:microsoft.quantum.lang-ref.int)

Индекс в векторе параметра модели, описывающий угол для этого вращения.

## <a name="remarks"></a>Remarks

Неуправляемый поворот можно представить, задав `ControlIndices` для него пустой массив индексов, `new Int[0]` .