---
uid: Microsoft.Quantum.Canon.ApplyToRest
title: Операция Апплиторест
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRest
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 29bf080d693c668421181f10faef50f5681683be
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717106"
---
# <a name="applytorest-operation"></a><span data-ttu-id="b6598-102">Операция Апплиторест</span><span class="sxs-lookup"><span data-stu-id="b6598-102">ApplyToRest operation</span></span>

<span data-ttu-id="b6598-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b6598-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b6598-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b6598-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b6598-105">Применяет операцию ко всему элементу массива, кроме первого элемента.</span><span class="sxs-lookup"><span data-stu-id="b6598-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRest<'T> (op : ('T[] => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="b6598-106">Описание</span><span class="sxs-lookup"><span data-stu-id="b6598-106">Description</span></span>

<span data-ttu-id="b6598-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="b6598-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="b6598-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b6598-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="b6598-109">Op: 'T [] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="b6598-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="b6598-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="b6598-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="b6598-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="b6598-111">targets : 'T[]</span></span>

<span data-ttu-id="b6598-112">Массив целевых объектов, к которым будут применяться все, кроме первого `op` .</span><span class="sxs-lookup"><span data-stu-id="b6598-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b6598-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b6598-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="b6598-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="b6598-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b6598-115">Е</span><span class="sxs-lookup"><span data-stu-id="b6598-115">'T</span></span>

<span data-ttu-id="b6598-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="b6598-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="b6598-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="b6598-117">See Also</span></span>

- [<span data-ttu-id="b6598-118">Microsoft. тактов. Canon. Апплитореста</span><span class="sxs-lookup"><span data-stu-id="b6598-118">Microsoft.Quantum.Canon.ApplyToRestA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [<span data-ttu-id="b6598-119">Microsoft. тактов. Canon. Апплиторестк</span><span class="sxs-lookup"><span data-stu-id="b6598-119">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)
- [<span data-ttu-id="b6598-120">Microsoft. тактов. Canon. Апплиторестка</span><span class="sxs-lookup"><span data-stu-id="b6598-120">Microsoft.Quantum.Canon.ApplyToRestCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestCA)