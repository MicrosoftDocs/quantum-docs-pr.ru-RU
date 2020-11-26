---
uid: Microsoft.Quantum.Canon.ApplyToHeadA
title: Операция Апплитохеада
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadA
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 3397c059706c48ff8ca47dd2312cfa9565aacaba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208641"
---
# <a name="applytoheada-operation"></a><span data-ttu-id="7c33f-102">Операция Апплитохеада</span><span class="sxs-lookup"><span data-stu-id="7c33f-102">ApplyToHeadA operation</span></span>

<span data-ttu-id="7c33f-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7c33f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7c33f-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7c33f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7c33f-105">Применяет операцию к первому элементу массива.</span><span class="sxs-lookup"><span data-stu-id="7c33f-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHeadA<'T> (op : ('T => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="7c33f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="7c33f-106">Description</span></span>

<span data-ttu-id="7c33f-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="7c33f-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="7c33f-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7c33f-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="7c33f-109">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  является просуммой</span><span class="sxs-lookup"><span data-stu-id="7c33f-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="7c33f-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="7c33f-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="7c33f-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="7c33f-111">targets : 'T[]</span></span>

<span data-ttu-id="7c33f-112">Массив целевых объектов, к которым будет применен первый из них `op` .</span><span class="sxs-lookup"><span data-stu-id="7c33f-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7c33f-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7c33f-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="7c33f-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="7c33f-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7c33f-115">Е</span><span class="sxs-lookup"><span data-stu-id="7c33f-115">'T</span></span>

<span data-ttu-id="7c33f-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="7c33f-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="7c33f-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="7c33f-117">See Also</span></span>

- [<span data-ttu-id="7c33f-118">Microsoft. тактов. Canon. Апплитохеад</span><span class="sxs-lookup"><span data-stu-id="7c33f-118">Microsoft.Quantum.Canon.ApplyToHead</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [<span data-ttu-id="7c33f-119">Microsoft. тактов. Canon. Апплитохеадк</span><span class="sxs-lookup"><span data-stu-id="7c33f-119">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)
- [<span data-ttu-id="7c33f-120">Microsoft. тактов. Canon. Апплитохеадка</span><span class="sxs-lookup"><span data-stu-id="7c33f-120">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)