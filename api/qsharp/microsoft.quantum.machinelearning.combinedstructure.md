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
# <a name="combinedstructure-function"></a><span data-ttu-id="0d41b-102">Функция Комбинедструктуре</span><span class="sxs-lookup"><span data-stu-id="0d41b-102">CombinedStructure function</span></span>

<span data-ttu-id="0d41b-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="0d41b-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="0d41b-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0d41b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0d41b-105">При наличии одного или нескольких уровней управляемых поворотов возвращает один слой с индексом параметра модели, смещенным таким, что отдельные слои параметризованы с помощью отдельных параметров модели.</span><span class="sxs-lookup"><span data-stu-id="0d41b-105">Given one or more layers of controlled rotations, returns a single layer with model parameter index shifted such that distinct layers are parameterized by distinct model parameters.</span></span>

```qsharp
function CombinedStructure (layers : Microsoft.Quantum.MachineLearning.ControlledRotation[][]) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="0d41b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0d41b-106">Input</span></span>

### <a name="layers--controlledrotation"></a><span data-ttu-id="0d41b-107">слои: [контролледротатион](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[] []</span><span class="sxs-lookup"><span data-stu-id="0d41b-107">layers : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[][]</span></span>

<span data-ttu-id="0d41b-108">Объединяемые слои.</span><span class="sxs-lookup"><span data-stu-id="0d41b-108">The layers to be combined.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="0d41b-109">Выходные данные: [контролледротатион](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="0d41b-109">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="0d41b-110">Один слой управляемых поворотов, представляющий объединение всех других слоев.</span><span class="sxs-lookup"><span data-stu-id="0d41b-110">A single layer of controlled rotations, representing the concatenation of all other layers.</span></span>