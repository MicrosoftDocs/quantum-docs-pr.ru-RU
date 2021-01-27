---
uid: Microsoft.Quantum.Canon.ApplyToElement
title: Операция Апплитоелемент
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElement
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: 5159eee07f7398cc6194c9907a37b78a63aaf263
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850775"
---
# <a name="applytoelement-operation"></a><span data-ttu-id="078f4-102">Операция Апплитоелемент</span><span class="sxs-lookup"><span data-stu-id="078f4-102">ApplyToElement operation</span></span>

<span data-ttu-id="078f4-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="078f4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="078f4-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="078f4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="078f4-105">Применяет операцию к заданному элементу массива.</span><span class="sxs-lookup"><span data-stu-id="078f4-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElement<'T> (op : ('T => Unit), index : Int, targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="078f4-106">Описание</span><span class="sxs-lookup"><span data-stu-id="078f4-106">Description</span></span>

<span data-ttu-id="078f4-107">При наличии операции `op` , индекса `index` и массива целевых объектов `targets` применяется `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="078f4-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="078f4-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="078f4-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="078f4-109">Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="078f4-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="078f4-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="078f4-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="078f4-111">Индекс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="078f4-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="078f4-112">Индекс в массиве целевых объектов.</span><span class="sxs-lookup"><span data-stu-id="078f4-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="078f4-113">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="078f4-113">targets : 'T[]</span></span>

<span data-ttu-id="078f4-114">Массив возможных целевых объектов для `op` .</span><span class="sxs-lookup"><span data-stu-id="078f4-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="078f4-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="078f4-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="078f4-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="078f4-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="078f4-117">Е</span><span class="sxs-lookup"><span data-stu-id="078f4-117">'T</span></span>

<span data-ttu-id="078f4-118">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="078f4-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="078f4-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="078f4-119">See Also</span></span>

- [<span data-ttu-id="078f4-120">Microsoft. тактов. Canon. Апплитоелементк</span><span class="sxs-lookup"><span data-stu-id="078f4-120">Microsoft.Quantum.Canon.ApplyToElementC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [<span data-ttu-id="078f4-121">Microsoft. тактов. Canon. Апплитоелемента</span><span class="sxs-lookup"><span data-stu-id="078f4-121">Microsoft.Quantum.Canon.ApplyToElementA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementA)
- [<span data-ttu-id="078f4-122">Microsoft. тактов. Canon. Апплитоелементка</span><span class="sxs-lookup"><span data-stu-id="078f4-122">Microsoft.Quantum.Canon.ApplyToElementCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementCA)