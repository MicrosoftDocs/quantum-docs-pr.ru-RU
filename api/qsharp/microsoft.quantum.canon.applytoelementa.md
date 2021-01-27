---
uid: Microsoft.Quantum.Canon.ApplyToElementA
title: Операция Апплитоелемента
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementA
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: 57d870c7fbd099212b13f75bd85e57c046280d73
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850772"
---
# <a name="applytoelementa-operation"></a><span data-ttu-id="d4079-102">Операция Апплитоелемента</span><span class="sxs-lookup"><span data-stu-id="d4079-102">ApplyToElementA operation</span></span>

<span data-ttu-id="d4079-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d4079-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d4079-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d4079-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d4079-105">Применяет операцию к заданному элементу массива.</span><span class="sxs-lookup"><span data-stu-id="d4079-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElementA<'T> (op : ('T => Unit is Adj), index : Int, targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="d4079-106">Описание</span><span class="sxs-lookup"><span data-stu-id="d4079-106">Description</span></span>

<span data-ttu-id="d4079-107">При наличии операции `op` , индекса `index` и массива целевых объектов `targets` применяется `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="d4079-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="d4079-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d4079-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="d4079-109">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  является просуммой</span><span class="sxs-lookup"><span data-stu-id="d4079-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="d4079-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="d4079-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="d4079-111">Индекс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d4079-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d4079-112">Индекс в массиве целевых объектов.</span><span class="sxs-lookup"><span data-stu-id="d4079-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="d4079-113">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="d4079-113">targets : 'T[]</span></span>

<span data-ttu-id="d4079-114">Массив возможных целевых объектов для `op` .</span><span class="sxs-lookup"><span data-stu-id="d4079-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d4079-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d4079-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d4079-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="d4079-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d4079-117">Е</span><span class="sxs-lookup"><span data-stu-id="d4079-117">'T</span></span>

<span data-ttu-id="d4079-118">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="d4079-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4079-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="d4079-119">See Also</span></span>

- [<span data-ttu-id="d4079-120">Microsoft. тактов. Canon. Апплитоелемент</span><span class="sxs-lookup"><span data-stu-id="d4079-120">Microsoft.Quantum.Canon.ApplyToElement</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [<span data-ttu-id="d4079-121">Microsoft. тактов. Canon. Апплитоелементк</span><span class="sxs-lookup"><span data-stu-id="d4079-121">Microsoft.Quantum.Canon.ApplyToElementC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [<span data-ttu-id="d4079-122">Microsoft. тактов. Canon. Апплитоелементка</span><span class="sxs-lookup"><span data-stu-id="d4079-122">Microsoft.Quantum.Canon.ApplyToElementCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementCA)