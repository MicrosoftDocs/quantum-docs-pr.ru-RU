---
uid: Microsoft.Quantum.Random.MaybeChooseElement
title: Операция Майбечусилемент
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: MaybeChooseElement
qsharp.summary: Given an array of data and an a distribution over its indices, attempts to choose an element at random.
ms.openlocfilehash: 1a69c8d5a6ae022ceda9269e17434b740809b107
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192865"
---
# <a name="maybechooseelement-operation"></a><span data-ttu-id="b1438-102">Операция Майбечусилемент</span><span class="sxs-lookup"><span data-stu-id="b1438-102">MaybeChooseElement operation</span></span>

<span data-ttu-id="b1438-103">Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="b1438-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="b1438-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="b1438-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="b1438-105">При наличии массива данных и распределения по индексам пытается выбрать элемент в случайном порядке.</span><span class="sxs-lookup"><span data-stu-id="b1438-105">Given an array of data and an a distribution over its indices, attempts to choose an element at random.</span></span>

```qsharp
operation MaybeChooseElement<'T> (data : 'T[], indexDistribution : Microsoft.Quantum.Random.DiscreteDistribution) : (Bool, 'T)
```


## <a name="input"></a><span data-ttu-id="b1438-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b1438-106">Input</span></span>

### <a name="data--t"></a><span data-ttu-id="b1438-107">данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="b1438-107">data : 'T[]</span></span>

<span data-ttu-id="b1438-108">Массив, из которого должен быть выбран элемент.</span><span class="sxs-lookup"><span data-stu-id="b1438-108">The array from which an element should be chosen.</span></span>


### <a name="indexdistribution--discretedistribution"></a><span data-ttu-id="b1438-109">Индексдистрибутион: [дискретедистрибутион](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="b1438-109">indexDistribution : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="b1438-110">Распределение по индексам `data` .</span><span class="sxs-lookup"><span data-stu-id="b1438-110">A distribution over the indices of `data`.</span></span>



## <a name="output--boolt"></a><span data-ttu-id="b1438-111">Выходные данные: ([bool](xref:microsoft.quantum.lang-ref.bool), 't)</span><span class="sxs-lookup"><span data-stu-id="b1438-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="b1438-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="b1438-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b1438-113">Е</span><span class="sxs-lookup"><span data-stu-id="b1438-113">'T</span></span>

