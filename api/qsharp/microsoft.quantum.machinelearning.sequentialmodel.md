---
uid: Microsoft.Quantum.MachineLearning.SequentialModel
title: Определяемый пользователем тип Секуентиалмодел
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: SequentialModel
qsharp.summary: Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.
ms.openlocfilehash: a425d2155489384ca81ef1c00a5e842bcfb40ae7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732297"
---
# <a name="sequentialmodel-user-defined-type"></a><span data-ttu-id="69974-102">Определяемый пользователем тип Секуентиалмодел</span><span class="sxs-lookup"><span data-stu-id="69974-102">SequentialModel user defined type</span></span>

<span data-ttu-id="69974-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="69974-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="69974-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="69974-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="69974-105">Описывает модель классификатора такта, состоящую из последовательности параметризованных и контролируемых поворотов, присваивания углов поворота и смещения между двумя классами, распознаваемыми моделью.</span><span class="sxs-lookup"><span data-stu-id="69974-105">Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.</span></span>

```qsharp

newtype SequentialModel = (Structure : Microsoft.Quantum.MachineLearning.ControlledRotation[], Parameters : Double[], Bias : Double);
```



## <a name="named-items"></a><span data-ttu-id="69974-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="69974-106">Named Items</span></span>

### <a name="structure--controlledrotation"></a><span data-ttu-id="69974-107">Структура: [контролледротатион](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="69974-107">Structure : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="69974-108">Последовательность управляемых поворотов, используемых для классификации входных данных.</span><span class="sxs-lookup"><span data-stu-id="69974-108">The sequence of controlled rotations used to classify inputs.</span></span>
### <a name="parameters--double"></a><span data-ttu-id="69974-109">Параметры: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="69974-109">Parameters : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="69974-110">Присваивание углов поворота к заданной структуре классификации.</span><span class="sxs-lookup"><span data-stu-id="69974-110">An assignment of rotation angles to the given classification structure.</span></span>
### <a name="bias--double"></a><span data-ttu-id="69974-111">Уровень смещения: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="69974-111">Bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="69974-112">Сдвиг между двумя классами, распознаваемыми этим классификатором.</span><span class="sxs-lookup"><span data-stu-id="69974-112">The bias between the two classes recognized by this classifier.</span></span>

## <a name="references"></a><span data-ttu-id="69974-113">Ссылки</span><span class="sxs-lookup"><span data-stu-id="69974-113">References</span></span>

- [<span data-ttu-id="69974-114">Арксив: 1804.00633</span><span class="sxs-lookup"><span data-stu-id="69974-114">arXiv:1804.00633</span></span>](https://arxiv.org/abs/1804.00633)