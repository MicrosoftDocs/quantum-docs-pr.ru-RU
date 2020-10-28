---
uid: Microsoft.Quantum.Random.MaybeChooseElement
title: Операция Майбечусилемент
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: MaybeChooseElement
qsharp.summary: Given an array of data and an a distribution over its indices, attempts to choose an element at random.
ms.openlocfilehash: 12640d9dc3aad301146eff7bcbbaae33d3ccd420
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732169"
---
# <a name="maybechooseelement-operation"></a><span data-ttu-id="e1567-102">Операция Майбечусилемент</span><span class="sxs-lookup"><span data-stu-id="e1567-102">MaybeChooseElement operation</span></span>

<span data-ttu-id="e1567-103">Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="e1567-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="e1567-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e1567-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e1567-105">При наличии массива данных и распределения по индексам пытается выбрать элемент в случайном порядке.</span><span class="sxs-lookup"><span data-stu-id="e1567-105">Given an array of data and an a distribution over its indices, attempts to choose an element at random.</span></span>

```qsharp
operation MaybeChooseElement<'T> (data : 'T[], indexDistribution : Microsoft.Quantum.Random.DiscreteDistribution) : (Bool, 'T)
```


## <a name="input"></a><span data-ttu-id="e1567-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e1567-106">Input</span></span>

### <a name="data--t"></a><span data-ttu-id="e1567-107">данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="e1567-107">data : 'T[]</span></span>

<span data-ttu-id="e1567-108">Массив, из которого должен быть выбран элемент.</span><span class="sxs-lookup"><span data-stu-id="e1567-108">The array from which an element should be chosen.</span></span>


### <a name="indexdistribution--discretedistribution"></a><span data-ttu-id="e1567-109">Индексдистрибутион: [дискретедистрибутион](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="e1567-109">indexDistribution : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="e1567-110">Распределение по индексам `data` .</span><span class="sxs-lookup"><span data-stu-id="e1567-110">A distribution over the indices of `data`.</span></span>



## <a name="output--boolt"></a><span data-ttu-id="e1567-111">Выходные данные: ([bool](xref:microsoft.quantum.lang-ref.bool), 't)</span><span class="sxs-lookup"><span data-stu-id="e1567-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e1567-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="e1567-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e1567-113">Е</span><span class="sxs-lookup"><span data-stu-id="e1567-113">'T</span></span>

