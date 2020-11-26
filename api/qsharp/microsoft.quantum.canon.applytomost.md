---
uid: Microsoft.Quantum.Canon.ApplyToMost
title: Операция Апплитомост
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMost
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: 7e7824b431ccff644cf5cc53145163327eb8ad36
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208539"
---
# <a name="applytomost-operation"></a><span data-ttu-id="47182-102">Операция Апплитомост</span><span class="sxs-lookup"><span data-stu-id="47182-102">ApplyToMost operation</span></span>

<span data-ttu-id="47182-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="47182-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="47182-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="47182-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="47182-105">Применяет операцию ко всему элементу массива, кроме последнего.</span><span class="sxs-lookup"><span data-stu-id="47182-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMost<'T> (op : ('T[] => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="47182-106">Описание</span><span class="sxs-lookup"><span data-stu-id="47182-106">Description</span></span>

<span data-ttu-id="47182-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="47182-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="47182-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="47182-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="47182-109">Op: 'T [] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="47182-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="47182-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="47182-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="47182-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="47182-111">targets : 'T[]</span></span>

<span data-ttu-id="47182-112">Массив целевых объектов, к которым будут применены все, кроме последнего `op` .</span><span class="sxs-lookup"><span data-stu-id="47182-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="47182-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="47182-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="47182-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="47182-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="47182-115">Е</span><span class="sxs-lookup"><span data-stu-id="47182-115">'T</span></span>

<span data-ttu-id="47182-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="47182-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="47182-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="47182-117">See Also</span></span>

- [<span data-ttu-id="47182-118">Microsoft. тактов. Canon. Апплитомоста</span><span class="sxs-lookup"><span data-stu-id="47182-118">Microsoft.Quantum.Canon.ApplyToMostA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [<span data-ttu-id="47182-119">Microsoft. тактов. Canon. Апплитомостк</span><span class="sxs-lookup"><span data-stu-id="47182-119">Microsoft.Quantum.Canon.ApplyToMostC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostC)
- [<span data-ttu-id="47182-120">Microsoft. тактов. Canon. Апплитомостка</span><span class="sxs-lookup"><span data-stu-id="47182-120">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)