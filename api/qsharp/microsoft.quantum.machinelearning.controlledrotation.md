---
uid: Microsoft.Quantum.MachineLearning.ControlledRotation
title: Определяемый пользователем тип Контролледротатион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ControlledRotation
qsharp.summary: Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.
ms.openlocfilehash: 1e664b470caeba656ea4a73f70bbc0ef5fe76f7e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196571"
---
# <a name="controlledrotation-user-defined-type"></a>Определяемый пользователем тип Контролледротатион

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


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

## <a name="remarks"></a>Комментарии

Неуправляемый поворот можно представить, задав `ControlIndices` для него пустой массив индексов, `new Int[0]` .