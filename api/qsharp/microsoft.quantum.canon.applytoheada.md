---
uid: Microsoft.Quantum.Canon.ApplyToHeadA
title: Операция Апплитохеада
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadA
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: ba060243cb01782fd8529e0b05ee7258a66314f5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717259"
---
# <a name="applytoheada-operation"></a><span data-ttu-id="1fc76-102">Операция Апплитохеада</span><span class="sxs-lookup"><span data-stu-id="1fc76-102">ApplyToHeadA operation</span></span>

<span data-ttu-id="1fc76-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1fc76-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1fc76-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1fc76-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1fc76-105">Применяет операцию к первому элементу массива.</span><span class="sxs-lookup"><span data-stu-id="1fc76-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHeadA<'T> (op : ('T => Unit is Adj), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="1fc76-106">Описание</span><span class="sxs-lookup"><span data-stu-id="1fc76-106">Description</span></span>

<span data-ttu-id="1fc76-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="1fc76-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="1fc76-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="1fc76-108">Input</span></span>

### <a name="op--t--unit-adj"></a><span data-ttu-id="1fc76-109">Op: 'T => [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1fc76-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="1fc76-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="1fc76-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="1fc76-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="1fc76-111">targets : 'T[]</span></span>

<span data-ttu-id="1fc76-112">Массив целевых объектов, к которым будет применен первый из них `op` .</span><span class="sxs-lookup"><span data-stu-id="1fc76-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1fc76-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1fc76-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="1fc76-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="1fc76-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1fc76-115">Е</span><span class="sxs-lookup"><span data-stu-id="1fc76-115">'T</span></span>

<span data-ttu-id="1fc76-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="1fc76-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="1fc76-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="1fc76-117">See Also</span></span>

- [<span data-ttu-id="1fc76-118">Microsoft. тактов. Canon. Апплитохеад</span><span class="sxs-lookup"><span data-stu-id="1fc76-118">Microsoft.Quantum.Canon.ApplyToHead</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [<span data-ttu-id="1fc76-119">Microsoft. тактов. Canon. Апплитохеадк</span><span class="sxs-lookup"><span data-stu-id="1fc76-119">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)
- [<span data-ttu-id="1fc76-120">Microsoft. тактов. Canon. Апплитохеадка</span><span class="sxs-lookup"><span data-stu-id="1fc76-120">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)