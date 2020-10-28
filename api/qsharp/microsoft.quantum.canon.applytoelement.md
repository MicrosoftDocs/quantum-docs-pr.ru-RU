---
uid: Microsoft.Quantum.Canon.ApplyToElement
title: Операция Апплитоелемент
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElement
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: 5c321d95c9b79bc50827c2b50c406b164e143dc6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717511"
---
# <a name="applytoelement-operation"></a><span data-ttu-id="ae0c9-102">Операция Апплитоелемент</span><span class="sxs-lookup"><span data-stu-id="ae0c9-102">ApplyToElement operation</span></span>

<span data-ttu-id="ae0c9-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ae0c9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ae0c9-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ae0c9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ae0c9-105">Применяет операцию к заданному элементу массива.</span><span class="sxs-lookup"><span data-stu-id="ae0c9-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElement<'T> (op : ('T => Unit), index : Int, targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="ae0c9-106">Описание</span><span class="sxs-lookup"><span data-stu-id="ae0c9-106">Description</span></span>

<span data-ttu-id="ae0c9-107">При наличии операции `op` , индекса `index` и массива целевых объектов `targets` применяется `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="ae0c9-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="ae0c9-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ae0c9-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="ae0c9-109">Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="ae0c9-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="ae0c9-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="ae0c9-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="ae0c9-111">Индекс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ae0c9-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ae0c9-112">Индекс в массиве целевых объектов.</span><span class="sxs-lookup"><span data-stu-id="ae0c9-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="ae0c9-113">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="ae0c9-113">targets : 'T[]</span></span>

<span data-ttu-id="ae0c9-114">Массив возможных целевых объектов для `op` .</span><span class="sxs-lookup"><span data-stu-id="ae0c9-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ae0c9-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ae0c9-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ae0c9-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="ae0c9-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ae0c9-117">Е</span><span class="sxs-lookup"><span data-stu-id="ae0c9-117">'T</span></span>

<span data-ttu-id="ae0c9-118">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="ae0c9-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="ae0c9-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="ae0c9-119">See Also</span></span>

- [<span data-ttu-id="ae0c9-120">Microsoft. тактов. Canon. Апплитоелементк</span><span class="sxs-lookup"><span data-stu-id="ae0c9-120">Microsoft.Quantum.Canon.ApplyToElementC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [<span data-ttu-id="ae0c9-121">Microsoft. тактов. Canon. Апплитоелемента</span><span class="sxs-lookup"><span data-stu-id="ae0c9-121">Microsoft.Quantum.Canon.ApplyToElementA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementA)
- [<span data-ttu-id="ae0c9-122">Microsoft. тактов. Canon. Апплитоелементка</span><span class="sxs-lookup"><span data-stu-id="ae0c9-122">Microsoft.Quantum.Canon.ApplyToElementCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementCA)