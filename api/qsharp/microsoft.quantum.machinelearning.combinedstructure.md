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
# <a name="combinedstructure-function"></a><span data-ttu-id="4e023-102">Функция Комбинедструктуре</span><span class="sxs-lookup"><span data-stu-id="4e023-102">CombinedStructure function</span></span>

<span data-ttu-id="4e023-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="4e023-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="4e023-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="4e023-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="4e023-105">При наличии одного или нескольких уровней управляемых поворотов возвращает один слой с индексом параметра модели, смещенным таким, что отдельные слои параметризованы с помощью отдельных параметров модели.</span><span class="sxs-lookup"><span data-stu-id="4e023-105">Given one or more layers of controlled rotations, returns a single layer with model parameter index shifted such that distinct layers are parameterized by distinct model parameters.</span></span>

```qsharp
function CombinedStructure (layers : Microsoft.Quantum.MachineLearning.ControlledRotation[][]) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="4e023-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4e023-106">Input</span></span>

### <a name="layers--controlledrotation"></a><span data-ttu-id="4e023-107">слои: [контролледротатион](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[] []</span><span class="sxs-lookup"><span data-stu-id="4e023-107">layers : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[][]</span></span>

<span data-ttu-id="4e023-108">Объединяемые слои.</span><span class="sxs-lookup"><span data-stu-id="4e023-108">The layers to be combined.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="4e023-109">Выходные данные: [контролледротатион](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="4e023-109">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="4e023-110">Один слой управляемых поворотов, представляющий объединение всех других слоев.</span><span class="sxs-lookup"><span data-stu-id="4e023-110">A single layer of controlled rotations, representing the concatenation of all other layers.</span></span>