---
uid: Microsoft.Quantum.Canon.ApplyToHeadA
title: Операция Апплитохеада
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadA
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 290347ff54492c4291db540e82cedcdd822a354e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850644"
---
# <a name="applytoheada-operation"></a><span data-ttu-id="11ba3-102">Операция Апплитохеада</span><span class="sxs-lookup"><span data-stu-id="11ba3-102">ApplyToHeadA operation</span></span>

<span data-ttu-id="11ba3-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="11ba3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="11ba3-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="11ba3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="11ba3-105">Применяет операцию к первому элементу массива.</span><span class="sxs-lookup"><span data-stu-id="11ba3-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHeadA<'T> (op : ('T => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="11ba3-106">Описание</span><span class="sxs-lookup"><span data-stu-id="11ba3-106">Description</span></span>

<span data-ttu-id="11ba3-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="11ba3-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="11ba3-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="11ba3-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="11ba3-109">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  является просуммой</span><span class="sxs-lookup"><span data-stu-id="11ba3-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="11ba3-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="11ba3-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="11ba3-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="11ba3-111">targets : 'T[]</span></span>

<span data-ttu-id="11ba3-112">Массив целевых объектов, к которым будет применен первый из них `op` .</span><span class="sxs-lookup"><span data-stu-id="11ba3-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="11ba3-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="11ba3-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="11ba3-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="11ba3-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="11ba3-115">Е</span><span class="sxs-lookup"><span data-stu-id="11ba3-115">'T</span></span>

<span data-ttu-id="11ba3-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="11ba3-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="11ba3-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="11ba3-117">See Also</span></span>

- [<span data-ttu-id="11ba3-118">Microsoft. тактов. Canon. Апплитохеад</span><span class="sxs-lookup"><span data-stu-id="11ba3-118">Microsoft.Quantum.Canon.ApplyToHead</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [<span data-ttu-id="11ba3-119">Microsoft. тактов. Canon. Апплитохеадк</span><span class="sxs-lookup"><span data-stu-id="11ba3-119">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)
- [<span data-ttu-id="11ba3-120">Microsoft. тактов. Canon. Апплитохеадка</span><span class="sxs-lookup"><span data-stu-id="11ba3-120">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)