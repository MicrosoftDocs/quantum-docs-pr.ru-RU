---
uid: Microsoft.Quantum.Canon.ApplyToElementC
title: Операция Апплитоелементк
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementC
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: bd466ff59e6e962be9a7e58b6d298c60b0d1d90d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717455"
---
# <a name="applytoelementc-operation"></a><span data-ttu-id="10166-102">Операция Апплитоелементк</span><span class="sxs-lookup"><span data-stu-id="10166-102">ApplyToElementC operation</span></span>

<span data-ttu-id="10166-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="10166-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="10166-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="10166-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="10166-105">Применяет операцию к заданному элементу массива.</span><span class="sxs-lookup"><span data-stu-id="10166-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElementC<'T> (op : ('T => Unit is Ctl), index : Int, targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="10166-106">Описание</span><span class="sxs-lookup"><span data-stu-id="10166-106">Description</span></span>

<span data-ttu-id="10166-107">При наличии операции `op` , индекса `index` и массива целевых объектов `targets` применяется `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="10166-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="10166-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="10166-108">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="10166-109">Op: 'T => [единицы](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="10166-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="10166-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="10166-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="10166-111">Индекс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="10166-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="10166-112">Индекс в массиве целевых объектов.</span><span class="sxs-lookup"><span data-stu-id="10166-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="10166-113">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="10166-113">targets : 'T[]</span></span>

<span data-ttu-id="10166-114">Массив возможных целевых объектов для `op` .</span><span class="sxs-lookup"><span data-stu-id="10166-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="10166-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="10166-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="10166-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="10166-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="10166-117">Е</span><span class="sxs-lookup"><span data-stu-id="10166-117">'T</span></span>

<span data-ttu-id="10166-118">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="10166-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="10166-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="10166-119">See Also</span></span>

- [<span data-ttu-id="10166-120">Microsoft. тактов. Canon. Апплитоелемент</span><span class="sxs-lookup"><span data-stu-id="10166-120">Microsoft.Quantum.Canon.ApplyToElement</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [<span data-ttu-id="10166-121">Microsoft. тактов. Canon. Апплитоелемента</span><span class="sxs-lookup"><span data-stu-id="10166-121">Microsoft.Quantum.Canon.ApplyToElementA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementA)
- [<span data-ttu-id="10166-122">Microsoft. тактов. Canon. Апплитоелементка</span><span class="sxs-lookup"><span data-stu-id="10166-122">Microsoft.Quantum.Canon.ApplyToElementCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementCA)