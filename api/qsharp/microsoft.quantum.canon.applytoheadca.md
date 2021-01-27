---
uid: Microsoft.Quantum.Canon.ApplyToHeadCA
title: Операция Апплитохеадка
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadCA
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 1bb24006a2d52167dfc7a7871cfbf5a4378d1cb7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850614"
---
# <a name="applytoheadca-operation"></a><span data-ttu-id="28a47-102">Операция Апплитохеадка</span><span class="sxs-lookup"><span data-stu-id="28a47-102">ApplyToHeadCA operation</span></span>

<span data-ttu-id="28a47-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="28a47-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="28a47-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="28a47-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="28a47-105">Применяет операцию к первому элементу массива.</span><span class="sxs-lookup"><span data-stu-id="28a47-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHeadCA<'T> (op : ('T => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="28a47-106">Описание</span><span class="sxs-lookup"><span data-stu-id="28a47-106">Description</span></span>

<span data-ttu-id="28a47-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="28a47-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="28a47-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="28a47-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="28a47-109">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="28a47-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="28a47-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="28a47-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="28a47-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="28a47-111">targets : 'T[]</span></span>

<span data-ttu-id="28a47-112">Массив целевых объектов, к которым будет применен первый из них `op` .</span><span class="sxs-lookup"><span data-stu-id="28a47-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="28a47-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="28a47-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="28a47-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="28a47-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="28a47-115">Е</span><span class="sxs-lookup"><span data-stu-id="28a47-115">'T</span></span>

<span data-ttu-id="28a47-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="28a47-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="28a47-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="28a47-117">See Also</span></span>

- [<span data-ttu-id="28a47-118">Microsoft. тактов. Canon. Апплитохеад</span><span class="sxs-lookup"><span data-stu-id="28a47-118">Microsoft.Quantum.Canon.ApplyToHead</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [<span data-ttu-id="28a47-119">Microsoft. тактов. Canon. Апплитохеада</span><span class="sxs-lookup"><span data-stu-id="28a47-119">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="28a47-120">Microsoft. тактов. Canon. Апплитохеадк</span><span class="sxs-lookup"><span data-stu-id="28a47-120">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)