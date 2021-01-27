---
uid: Microsoft.Quantum.Random.MaybeChooseElement
title: Операция Майбечусилемент
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: MaybeChooseElement
qsharp.summary: Given an array of data and an a distribution over its indices, attempts to choose an element at random.
ms.openlocfilehash: 86a69110fc92a2b6238cc757c09185c9fbcdb035
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856114"
---
# <a name="maybechooseelement-operation"></a><span data-ttu-id="d4562-102">Операция Майбечусилемент</span><span class="sxs-lookup"><span data-stu-id="d4562-102">MaybeChooseElement operation</span></span>

<span data-ttu-id="d4562-103">Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="d4562-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="d4562-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="d4562-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="d4562-105">При наличии массива данных и распределения по индексам пытается выбрать элемент в случайном порядке.</span><span class="sxs-lookup"><span data-stu-id="d4562-105">Given an array of data and an a distribution over its indices, attempts to choose an element at random.</span></span>

```qsharp
operation MaybeChooseElement<'T> (data : 'T[], indexDistribution : Microsoft.Quantum.Random.DiscreteDistribution) : (Bool, 'T)
```


## <a name="input"></a><span data-ttu-id="d4562-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d4562-106">Input</span></span>

### <a name="data--t"></a><span data-ttu-id="d4562-107">данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="d4562-107">data : 'T[]</span></span>

<span data-ttu-id="d4562-108">Массив, из которого должен быть выбран элемент.</span><span class="sxs-lookup"><span data-stu-id="d4562-108">The array from which an element should be chosen.</span></span>


### <a name="indexdistribution--discretedistribution"></a><span data-ttu-id="d4562-109">Индексдистрибутион: [дискретедистрибутион](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="d4562-109">indexDistribution : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="d4562-110">Распределение по индексам `data` .</span><span class="sxs-lookup"><span data-stu-id="d4562-110">A distribution over the indices of `data`.</span></span>



## <a name="output--boolt"></a><span data-ttu-id="d4562-111">Выходные данные: ([bool](xref:microsoft.quantum.lang-ref.bool), 't)</span><span class="sxs-lookup"><span data-stu-id="d4562-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d4562-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="d4562-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d4562-113">Е</span><span class="sxs-lookup"><span data-stu-id="d4562-113">'T</span></span>



## <a name="example"></a><span data-ttu-id="d4562-114">Пример</span><span class="sxs-lookup"><span data-stu-id="d4562-114">Example</span></span>

<span data-ttu-id="d4562-115">Следующий фрагмент Q # выбирает элемент случайным образом из массива:</span><span class="sxs-lookup"><span data-stu-id="d4562-115">The following Q# snippet chooses an element at random from an array:</span></span>

```qsharp
let (succeeded, element) = MaybeChooseElement(
    data,
    DiscreteUniformDistribution(0, Length(data) - 1)
);
Fact(succeeded, "Index chosen by MaybeChooseElement was not valid.");
```