---
uid: Microsoft.Quantum.Canon.ApplyToMostC
title: Операция Апплитомостк
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostC
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: 14de9f367aa7d19f64f13186d402239ae1fef3c1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850559"
---
# <a name="applytomostc-operation"></a><span data-ttu-id="a29f9-102">Операция Апплитомостк</span><span class="sxs-lookup"><span data-stu-id="a29f9-102">ApplyToMostC operation</span></span>

<span data-ttu-id="a29f9-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a29f9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a29f9-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a29f9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a29f9-105">Применяет операцию ко всему элементу массива, кроме последнего.</span><span class="sxs-lookup"><span data-stu-id="a29f9-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostC<'T> (op : ('T[] => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="a29f9-106">Описание</span><span class="sxs-lookup"><span data-stu-id="a29f9-106">Description</span></span>

<span data-ttu-id="a29f9-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="a29f9-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="a29f9-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a29f9-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="a29f9-109">Op: 'T [] => [единица](xref:microsoft.quantum.lang-ref.unit)  является CTL</span><span class="sxs-lookup"><span data-stu-id="a29f9-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="a29f9-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="a29f9-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="a29f9-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="a29f9-111">targets : 'T[]</span></span>

<span data-ttu-id="a29f9-112">Массив целевых объектов, к которым будут применены все, кроме последнего `op` .</span><span class="sxs-lookup"><span data-stu-id="a29f9-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a29f9-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a29f9-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a29f9-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="a29f9-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a29f9-115">Е</span><span class="sxs-lookup"><span data-stu-id="a29f9-115">'T</span></span>

<span data-ttu-id="a29f9-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="a29f9-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="a29f9-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="a29f9-117">See Also</span></span>

- [<span data-ttu-id="a29f9-118">Microsoft. тактов. Canon. Апплитомост</span><span class="sxs-lookup"><span data-stu-id="a29f9-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="a29f9-119">Microsoft. тактов. Canon. Апплитомоста</span><span class="sxs-lookup"><span data-stu-id="a29f9-119">Microsoft.Quantum.Canon.ApplyToMostA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [<span data-ttu-id="a29f9-120">Microsoft. тактов. Canon. Апплитомостка</span><span class="sxs-lookup"><span data-stu-id="a29f9-120">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)