---
uid: Microsoft.Quantum.Canon.ApplyToHeadC
title: Операция Апплитохеадк
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadC
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 3ff6c25837f1219dd456bf1739a2953ff72e2df9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717246"
---
# <a name="applytoheadc-operation"></a><span data-ttu-id="86916-102">Операция Апплитохеадк</span><span class="sxs-lookup"><span data-stu-id="86916-102">ApplyToHeadC operation</span></span>

<span data-ttu-id="86916-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="86916-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="86916-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="86916-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="86916-105">Применяет операцию к первому элементу массива.</span><span class="sxs-lookup"><span data-stu-id="86916-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHeadC<'T> (op : ('T => Unit is Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="86916-106">Описание</span><span class="sxs-lookup"><span data-stu-id="86916-106">Description</span></span>

<span data-ttu-id="86916-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="86916-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="86916-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="86916-108">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="86916-109">Op: 'T => [единицы](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="86916-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="86916-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="86916-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="86916-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="86916-111">targets : 'T[]</span></span>

<span data-ttu-id="86916-112">Массив целевых объектов, к которым будет применен первый из них `op` .</span><span class="sxs-lookup"><span data-stu-id="86916-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="86916-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="86916-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="86916-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="86916-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="86916-115">Е</span><span class="sxs-lookup"><span data-stu-id="86916-115">'T</span></span>

<span data-ttu-id="86916-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="86916-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="86916-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="86916-117">See Also</span></span>

- [<span data-ttu-id="86916-118">Microsoft. тактов. Canon. Апплитохеад</span><span class="sxs-lookup"><span data-stu-id="86916-118">Microsoft.Quantum.Canon.ApplyToHead</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [<span data-ttu-id="86916-119">Microsoft. тактов. Canon. Апплитохеада</span><span class="sxs-lookup"><span data-stu-id="86916-119">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="86916-120">Microsoft. тактов. Canon. Апплитохеадка</span><span class="sxs-lookup"><span data-stu-id="86916-120">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)