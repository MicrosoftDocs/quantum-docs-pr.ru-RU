---
uid: Microsoft.Quantum.Canon.ApplyToHeadC
title: Операция Апплитохеадк
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadC
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 3a65ad52e0b2f8b3a921fc549c35311f24d0e189
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850630"
---
# <a name="applytoheadc-operation"></a><span data-ttu-id="47290-102">Операция Апплитохеадк</span><span class="sxs-lookup"><span data-stu-id="47290-102">ApplyToHeadC operation</span></span>

<span data-ttu-id="47290-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="47290-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="47290-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="47290-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="47290-105">Применяет операцию к первому элементу массива.</span><span class="sxs-lookup"><span data-stu-id="47290-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHeadC<'T> (op : ('T => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="47290-106">Описание</span><span class="sxs-lookup"><span data-stu-id="47290-106">Description</span></span>

<span data-ttu-id="47290-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="47290-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="47290-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="47290-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="47290-109">Op: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — CTL</span><span class="sxs-lookup"><span data-stu-id="47290-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="47290-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="47290-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="47290-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="47290-111">targets : 'T[]</span></span>

<span data-ttu-id="47290-112">Массив целевых объектов, к которым будет применен первый из них `op` .</span><span class="sxs-lookup"><span data-stu-id="47290-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="47290-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="47290-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="47290-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="47290-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="47290-115">Е</span><span class="sxs-lookup"><span data-stu-id="47290-115">'T</span></span>

<span data-ttu-id="47290-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="47290-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="47290-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="47290-117">See Also</span></span>

- [<span data-ttu-id="47290-118">Microsoft. тактов. Canon. Апплитохеад</span><span class="sxs-lookup"><span data-stu-id="47290-118">Microsoft.Quantum.Canon.ApplyToHead</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [<span data-ttu-id="47290-119">Microsoft. тактов. Canon. Апплитохеада</span><span class="sxs-lookup"><span data-stu-id="47290-119">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="47290-120">Microsoft. тактов. Canon. Апплитохеадка</span><span class="sxs-lookup"><span data-stu-id="47290-120">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)