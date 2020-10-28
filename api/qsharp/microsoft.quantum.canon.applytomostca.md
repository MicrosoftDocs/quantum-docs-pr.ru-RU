---
uid: Microsoft.Quantum.Canon.ApplyToMostCA
title: Операция Апплитомостка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostCA
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: 797cbd835446f31b2df60dbb184f888e6d0356aa
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717162"
---
# <a name="applytomostca-operation"></a><span data-ttu-id="03e75-102">Операция Апплитомостка</span><span class="sxs-lookup"><span data-stu-id="03e75-102">ApplyToMostCA operation</span></span>

<span data-ttu-id="03e75-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="03e75-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="03e75-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="03e75-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="03e75-105">Применяет операцию ко всему элементу массива, кроме последнего.</span><span class="sxs-lookup"><span data-stu-id="03e75-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostCA<'T> (op : ('T[] => Unit is Adj + Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="03e75-106">Описание</span><span class="sxs-lookup"><span data-stu-id="03e75-106">Description</span></span>

<span data-ttu-id="03e75-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="03e75-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="03e75-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="03e75-108">Input</span></span>

### <a name="op--t--unit-adj--ctl"></a><span data-ttu-id="03e75-109">Op: 'T [] => [модульные](xref:microsoft.quantum.lang-ref.unit) года + CTL</span><span class="sxs-lookup"><span data-stu-id="03e75-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="03e75-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="03e75-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="03e75-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="03e75-111">targets : 'T[]</span></span>

<span data-ttu-id="03e75-112">Массив целевых объектов, к которым будут применены все, кроме последнего `op` .</span><span class="sxs-lookup"><span data-stu-id="03e75-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="03e75-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="03e75-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="03e75-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="03e75-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="03e75-115">Е</span><span class="sxs-lookup"><span data-stu-id="03e75-115">'T</span></span>

<span data-ttu-id="03e75-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="03e75-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="03e75-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="03e75-117">See Also</span></span>

- [<span data-ttu-id="03e75-118">Microsoft. тактов. Canon. Апплитомост</span><span class="sxs-lookup"><span data-stu-id="03e75-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="03e75-119">Microsoft. тактов. Canon. Апплитомоста</span><span class="sxs-lookup"><span data-stu-id="03e75-119">Microsoft.Quantum.Canon.ApplyToMostA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [<span data-ttu-id="03e75-120">Microsoft. тактов. Canon. Апплитомостк</span><span class="sxs-lookup"><span data-stu-id="03e75-120">Microsoft.Quantum.Canon.ApplyToMostC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostC)