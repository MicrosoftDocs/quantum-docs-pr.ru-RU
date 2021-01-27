---
uid: Microsoft.Quantum.Canon.ApplyToElementC
title: Операция Апплитоелементк
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementC
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: bc63b6b591781a6283b872ef0c2509094a656b4c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850745"
---
# <a name="applytoelementc-operation"></a><span data-ttu-id="42a39-102">Операция Апплитоелементк</span><span class="sxs-lookup"><span data-stu-id="42a39-102">ApplyToElementC operation</span></span>

<span data-ttu-id="42a39-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="42a39-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="42a39-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="42a39-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="42a39-105">Применяет операцию к заданному элементу массива.</span><span class="sxs-lookup"><span data-stu-id="42a39-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElementC<'T> (op : ('T => Unit is Ctl), index : Int, targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="42a39-106">Описание</span><span class="sxs-lookup"><span data-stu-id="42a39-106">Description</span></span>

<span data-ttu-id="42a39-107">При наличии операции `op` , индекса `index` и массива целевых объектов `targets` применяется `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="42a39-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="42a39-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="42a39-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="42a39-109">Op: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — CTL</span><span class="sxs-lookup"><span data-stu-id="42a39-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="42a39-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="42a39-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="42a39-111">Индекс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="42a39-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="42a39-112">Индекс в массиве целевых объектов.</span><span class="sxs-lookup"><span data-stu-id="42a39-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="42a39-113">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="42a39-113">targets : 'T[]</span></span>

<span data-ttu-id="42a39-114">Массив возможных целевых объектов для `op` .</span><span class="sxs-lookup"><span data-stu-id="42a39-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="42a39-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="42a39-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="42a39-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="42a39-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="42a39-117">Е</span><span class="sxs-lookup"><span data-stu-id="42a39-117">'T</span></span>

<span data-ttu-id="42a39-118">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="42a39-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="42a39-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="42a39-119">See Also</span></span>

- [<span data-ttu-id="42a39-120">Microsoft. тактов. Canon. Апплитоелемент</span><span class="sxs-lookup"><span data-stu-id="42a39-120">Microsoft.Quantum.Canon.ApplyToElement</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [<span data-ttu-id="42a39-121">Microsoft. тактов. Canon. Апплитоелемента</span><span class="sxs-lookup"><span data-stu-id="42a39-121">Microsoft.Quantum.Canon.ApplyToElementA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementA)
- [<span data-ttu-id="42a39-122">Microsoft. тактов. Canon. Апплитоелементка</span><span class="sxs-lookup"><span data-stu-id="42a39-122">Microsoft.Quantum.Canon.ApplyToElementCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementCA)