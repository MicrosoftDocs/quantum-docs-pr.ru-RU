---
uid: Microsoft.Quantum.Canon.ApplyToElementC
title: Операция Апплитоелементк
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementC
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: c8d7841e3846ab435671f7959c724f987d8ad5a0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217583"
---
# <a name="applytoelementc-operation"></a><span data-ttu-id="43210-102">Операция Апплитоелементк</span><span class="sxs-lookup"><span data-stu-id="43210-102">ApplyToElementC operation</span></span>

<span data-ttu-id="43210-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="43210-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="43210-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="43210-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="43210-105">Применяет операцию к заданному элементу массива.</span><span class="sxs-lookup"><span data-stu-id="43210-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElementC<'T> (op : ('T => Unit is Ctl), index : Int, targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="43210-106">Описание</span><span class="sxs-lookup"><span data-stu-id="43210-106">Description</span></span>

<span data-ttu-id="43210-107">При наличии операции `op` , индекса `index` и массива целевых объектов `targets` применяется `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="43210-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="43210-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="43210-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="43210-109">Op: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — CTL</span><span class="sxs-lookup"><span data-stu-id="43210-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="43210-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="43210-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="43210-111">Индекс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="43210-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="43210-112">Индекс в массиве целевых объектов.</span><span class="sxs-lookup"><span data-stu-id="43210-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="43210-113">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="43210-113">targets : 'T[]</span></span>

<span data-ttu-id="43210-114">Массив возможных целевых объектов для `op` .</span><span class="sxs-lookup"><span data-stu-id="43210-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="43210-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="43210-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="43210-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="43210-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="43210-117">Е</span><span class="sxs-lookup"><span data-stu-id="43210-117">'T</span></span>

<span data-ttu-id="43210-118">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="43210-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="43210-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="43210-119">See Also</span></span>

- [<span data-ttu-id="43210-120">Microsoft. тактов. Canon. Апплитоелемент</span><span class="sxs-lookup"><span data-stu-id="43210-120">Microsoft.Quantum.Canon.ApplyToElement</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [<span data-ttu-id="43210-121">Microsoft. тактов. Canon. Апплитоелемента</span><span class="sxs-lookup"><span data-stu-id="43210-121">Microsoft.Quantum.Canon.ApplyToElementA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementA)
- [<span data-ttu-id="43210-122">Microsoft. тактов. Canon. Апплитоелементка</span><span class="sxs-lookup"><span data-stu-id="43210-122">Microsoft.Quantum.Canon.ApplyToElementCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementCA)