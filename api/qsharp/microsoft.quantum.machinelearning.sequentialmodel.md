---
uid: Microsoft.Quantum.MachineLearning.SequentialModel
title: Определяемый пользователем тип Секуентиалмодел
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: SequentialModel
qsharp.summary: Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.
ms.openlocfilehash: 3afdb8dafe0179535fe5d8c3dff668f1f3de2f7d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196180"
---
# <a name="sequentialmodel-user-defined-type"></a><span data-ttu-id="287f8-102">Определяемый пользователем тип Секуентиалмодел</span><span class="sxs-lookup"><span data-stu-id="287f8-102">SequentialModel user defined type</span></span>

<span data-ttu-id="287f8-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="287f8-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="287f8-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="287f8-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="287f8-105">Описывает модель классификатора такта, состоящую из последовательности параметризованных и контролируемых поворотов, присваивания углов поворота и смещения между двумя классами, распознаваемыми моделью.</span><span class="sxs-lookup"><span data-stu-id="287f8-105">Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.</span></span>

```qsharp

newtype SequentialModel = (Structure : Microsoft.Quantum.MachineLearning.ControlledRotation[], Parameters : Double[], Bias : Double);
```



## <a name="named-items"></a><span data-ttu-id="287f8-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="287f8-106">Named Items</span></span>

### <a name="structure--controlledrotation"></a><span data-ttu-id="287f8-107">Структура: [контролледротатион](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="287f8-107">Structure : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="287f8-108">Последовательность управляемых поворотов, используемых для классификации входных данных.</span><span class="sxs-lookup"><span data-stu-id="287f8-108">The sequence of controlled rotations used to classify inputs.</span></span>
### <a name="parameters--double"></a><span data-ttu-id="287f8-109">Параметры: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="287f8-109">Parameters : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="287f8-110">Присваивание углов поворота к заданной структуре классификации.</span><span class="sxs-lookup"><span data-stu-id="287f8-110">An assignment of rotation angles to the given classification structure.</span></span>
### <a name="bias--double"></a><span data-ttu-id="287f8-111">Уровень смещения: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="287f8-111">Bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="287f8-112">Сдвиг между двумя классами, распознаваемыми этим классификатором.</span><span class="sxs-lookup"><span data-stu-id="287f8-112">The bias between the two classes recognized by this classifier.</span></span>

## <a name="references"></a><span data-ttu-id="287f8-113">Ссылки</span><span class="sxs-lookup"><span data-stu-id="287f8-113">References</span></span>

- [<span data-ttu-id="287f8-114">Арксив: 1804.00633</span><span class="sxs-lookup"><span data-stu-id="287f8-114">arXiv:1804.00633</span></span>](https://arxiv.org/abs/1804.00633)