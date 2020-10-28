---
uid: Microsoft.Quantum.Canon.ApplyToHead
title: Операция Апплитохеад
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHead
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 4e5fc439f48a5c7e527b7805c35cce18eca3ab36
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717273"
---
# <a name="applytohead-operation"></a><span data-ttu-id="0d990-102">Операция Апплитохеад</span><span class="sxs-lookup"><span data-stu-id="0d990-102">ApplyToHead operation</span></span>

<span data-ttu-id="0d990-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0d990-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0d990-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0d990-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0d990-105">Применяет операцию к первому элементу массива.</span><span class="sxs-lookup"><span data-stu-id="0d990-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHead<'T> (op : ('T => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="0d990-106">Описание</span><span class="sxs-lookup"><span data-stu-id="0d990-106">Description</span></span>

<span data-ttu-id="0d990-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="0d990-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="0d990-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0d990-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="0d990-109">Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="0d990-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="0d990-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="0d990-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="0d990-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="0d990-111">targets : 'T[]</span></span>

<span data-ttu-id="0d990-112">Массив целевых объектов, к которым будет применен первый из них `op` .</span><span class="sxs-lookup"><span data-stu-id="0d990-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0d990-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0d990-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="0d990-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="0d990-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0d990-115">Е</span><span class="sxs-lookup"><span data-stu-id="0d990-115">'T</span></span>

<span data-ttu-id="0d990-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="0d990-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d990-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="0d990-117">See Also</span></span>

- [<span data-ttu-id="0d990-118">Microsoft. тактов. Canon. Апплитохеада</span><span class="sxs-lookup"><span data-stu-id="0d990-118">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="0d990-119">Microsoft. тактов. Canon. Апплитохеадк</span><span class="sxs-lookup"><span data-stu-id="0d990-119">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)
- [<span data-ttu-id="0d990-120">Microsoft. тактов. Canon. Апплитохеадка</span><span class="sxs-lookup"><span data-stu-id="0d990-120">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)