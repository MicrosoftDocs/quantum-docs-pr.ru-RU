---
uid: Microsoft.Quantum.Canon.ApplyToHeadCA
title: Операция Апплитохеадка
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadCA
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: f28cff599e06090145fac860dbaf8274c966f80a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208556"
---
# <a name="applytoheadca-operation"></a><span data-ttu-id="cdb38-102">Операция Апплитохеадка</span><span class="sxs-lookup"><span data-stu-id="cdb38-102">ApplyToHeadCA operation</span></span>

<span data-ttu-id="cdb38-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="cdb38-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="cdb38-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cdb38-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cdb38-105">Применяет операцию к первому элементу массива.</span><span class="sxs-lookup"><span data-stu-id="cdb38-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHeadCA<'T> (op : ('T => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="cdb38-106">Описание</span><span class="sxs-lookup"><span data-stu-id="cdb38-106">Description</span></span>

<span data-ttu-id="cdb38-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="cdb38-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="cdb38-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="cdb38-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="cdb38-109">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="cdb38-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="cdb38-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="cdb38-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="cdb38-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="cdb38-111">targets : 'T[]</span></span>

<span data-ttu-id="cdb38-112">Массив целевых объектов, к которым будет применен первый из них `op` .</span><span class="sxs-lookup"><span data-stu-id="cdb38-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="cdb38-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cdb38-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="cdb38-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="cdb38-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="cdb38-115">Е</span><span class="sxs-lookup"><span data-stu-id="cdb38-115">'T</span></span>

<span data-ttu-id="cdb38-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="cdb38-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="cdb38-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="cdb38-117">See Also</span></span>

- [<span data-ttu-id="cdb38-118">Microsoft. тактов. Canon. Апплитохеад</span><span class="sxs-lookup"><span data-stu-id="cdb38-118">Microsoft.Quantum.Canon.ApplyToHead</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [<span data-ttu-id="cdb38-119">Microsoft. тактов. Canon. Апплитохеада</span><span class="sxs-lookup"><span data-stu-id="cdb38-119">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="cdb38-120">Microsoft. тактов. Canon. Апплитохеадк</span><span class="sxs-lookup"><span data-stu-id="cdb38-120">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)