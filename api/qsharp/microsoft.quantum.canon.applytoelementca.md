---
uid: Microsoft.Quantum.Canon.ApplyToElementCA
title: Операция Апплитоелементка
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementCA
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: 8ae4ece0d3d56ea2be1ce494ab0c5ee7caacbbf8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208862"
---
# <a name="applytoelementca-operation"></a><span data-ttu-id="eae8c-102">Операция Апплитоелементка</span><span class="sxs-lookup"><span data-stu-id="eae8c-102">ApplyToElementCA operation</span></span>

<span data-ttu-id="eae8c-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="eae8c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="eae8c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="eae8c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="eae8c-105">Применяет операцию к заданному элементу массива.</span><span class="sxs-lookup"><span data-stu-id="eae8c-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElementCA<'T> (op : ('T => Unit is Adj + Ctl), index : Int, targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="eae8c-106">Описание</span><span class="sxs-lookup"><span data-stu-id="eae8c-106">Description</span></span>

<span data-ttu-id="eae8c-107">При наличии операции `op` , индекса `index` и массива целевых объектов `targets` применяется `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="eae8c-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="eae8c-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="eae8c-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="eae8c-109">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="eae8c-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="eae8c-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="eae8c-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="eae8c-111">Индекс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="eae8c-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="eae8c-112">Индекс в массиве целевых объектов.</span><span class="sxs-lookup"><span data-stu-id="eae8c-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="eae8c-113">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="eae8c-113">targets : 'T[]</span></span>

<span data-ttu-id="eae8c-114">Массив возможных целевых объектов для `op` .</span><span class="sxs-lookup"><span data-stu-id="eae8c-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="eae8c-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="eae8c-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="eae8c-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="eae8c-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="eae8c-117">Е</span><span class="sxs-lookup"><span data-stu-id="eae8c-117">'T</span></span>

<span data-ttu-id="eae8c-118">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="eae8c-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="eae8c-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="eae8c-119">See Also</span></span>

- [<span data-ttu-id="eae8c-120">Microsoft. тактов. Canon. Апплитоелемент</span><span class="sxs-lookup"><span data-stu-id="eae8c-120">Microsoft.Quantum.Canon.ApplyToElement</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [<span data-ttu-id="eae8c-121">Microsoft. тактов. Canon. Апплитоелементк</span><span class="sxs-lookup"><span data-stu-id="eae8c-121">Microsoft.Quantum.Canon.ApplyToElementC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [<span data-ttu-id="eae8c-122">Microsoft. тактов. Canon. Апплитоелемента</span><span class="sxs-lookup"><span data-stu-id="eae8c-122">Microsoft.Quantum.Canon.ApplyToElementA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementA)