---
uid: Microsoft.Quantum.MachineLearning.ControlledRotation
title: Определяемый пользователем тип Контролледротатион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ControlledRotation
qsharp.summary: Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.
ms.openlocfilehash: 231afe65da3640218cbc97b9d49eae21bf6e1786
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847399"
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

## <a name="example"></a>Пример

Ниже представлен поворот $X $-AXIS первого кубит в регистре, управление вторым кубит, а также угол, заданный Четвертым параметром в последовательной модели.

```qsharp
let controlledRotation = ControlledRotation(
    (0, [1]),
    PauliX,
    3
)
```

## <a name="remarks"></a>Remarks

Неуправляемый поворот можно представить, задав `ControlIndices` для него пустой массив индексов, `new Int[0]` .