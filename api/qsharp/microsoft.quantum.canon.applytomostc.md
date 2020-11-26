---
uid: Microsoft.Quantum.Canon.ApplyToMostC
title: Операция Апплитомостк
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostC
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: af55093e44ce023c9e8b7e478730f4c527cf6d32
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208471"
---
# <a name="applytomostc-operation"></a><span data-ttu-id="7b046-102">Операция Апплитомостк</span><span class="sxs-lookup"><span data-stu-id="7b046-102">ApplyToMostC operation</span></span>

<span data-ttu-id="7b046-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7b046-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7b046-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7b046-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7b046-105">Применяет операцию ко всему элементу массива, кроме последнего.</span><span class="sxs-lookup"><span data-stu-id="7b046-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostC<'T> (op : ('T[] => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="7b046-106">Описание</span><span class="sxs-lookup"><span data-stu-id="7b046-106">Description</span></span>

<span data-ttu-id="7b046-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="7b046-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="7b046-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7b046-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="7b046-109">Op: 'T [] => [единица](xref:microsoft.quantum.lang-ref.unit)  является CTL</span><span class="sxs-lookup"><span data-stu-id="7b046-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="7b046-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="7b046-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="7b046-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="7b046-111">targets : 'T[]</span></span>

<span data-ttu-id="7b046-112">Массив целевых объектов, к которым будут применены все, кроме последнего `op` .</span><span class="sxs-lookup"><span data-stu-id="7b046-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7b046-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7b046-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="7b046-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="7b046-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7b046-115">Е</span><span class="sxs-lookup"><span data-stu-id="7b046-115">'T</span></span>

<span data-ttu-id="7b046-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="7b046-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="7b046-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="7b046-117">See Also</span></span>

- [<span data-ttu-id="7b046-118">Microsoft. тактов. Canon. Апплитомост</span><span class="sxs-lookup"><span data-stu-id="7b046-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="7b046-119">Microsoft. тактов. Canon. Апплитомоста</span><span class="sxs-lookup"><span data-stu-id="7b046-119">Microsoft.Quantum.Canon.ApplyToMostA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [<span data-ttu-id="7b046-120">Microsoft. тактов. Canon. Апплитомостка</span><span class="sxs-lookup"><span data-stu-id="7b046-120">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)