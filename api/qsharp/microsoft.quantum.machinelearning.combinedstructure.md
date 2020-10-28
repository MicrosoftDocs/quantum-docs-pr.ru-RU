---
uid: Microsoft.Quantum.MachineLearning.CombinedStructure
title: Функция Комбинедструктуре
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CombinedStructure
qsharp.summary: Given one or more layers of controlled rotations, returns a single layer with model parameter index shifted such that distinct layers are parameterized by distinct model parameters.
ms.openlocfilehash: fbfd87761a40abe350e5f955fb53d8024eeb614e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731113"
---
# <a name="combinedstructure-function"></a>Функция Комбинедструктуре

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакеты [](https://nuget.org/packages/)


При наличии одного или нескольких уровней управляемых поворотов возвращает один слой с индексом параметра модели, смещенным таким, что отдельные слои параметризованы с помощью отдельных параметров модели.

```qsharp
function CombinedStructure (layers : Microsoft.Quantum.MachineLearning.ControlledRotation[][]) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a>Входные данные

### <a name="layers--controlledrotation"></a>слои: [контролледротатион](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[] []

Объединяемые слои.



## <a name="output--controlledrotation"></a>Выходные данные: [контролледротатион](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]

Один слой управляемых поворотов, представляющий объединение всех других слоев.