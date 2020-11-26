---
uid: Microsoft.Quantum.MachineLearning.CombinedStructure
title: Функция Комбинедструктуре
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CombinedStructure
qsharp.summary: Given one or more layers of controlled rotations, returns a single layer with model parameter index shifted such that distinct layers are parameterized by distinct model parameters.
ms.openlocfilehash: 0a7d66be8b45d6a9df95b425e66b9b6bba241136
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211973"
---
# <a name="combinedstructure-function"></a>Функция Комбинедструктуре

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


При наличии одного или нескольких уровней управляемых поворотов возвращает один слой с индексом параметра модели, смещенным таким, что отдельные слои параметризованы с помощью отдельных параметров модели.

```qsharp
function CombinedStructure (layers : Microsoft.Quantum.MachineLearning.ControlledRotation[][]) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a>Входные данные

### <a name="layers--controlledrotation"></a>слои: [контролледротатион](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[] []

Объединяемые слои.



## <a name="output--controlledrotation"></a>Выходные данные: [контролледротатион](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]

Один слой управляемых поворотов, представляющий объединение всех других слоев.