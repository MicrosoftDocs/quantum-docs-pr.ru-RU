---
uid: Microsoft.Quantum.Canon.ApplyToMostCA
title: Операция Апплитомостка
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostCA
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: 0a80c23e0c6ff45083c192579dd8301d2277cef2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841310"
---
# <a name="applytomostca-operation"></a><span data-ttu-id="bc8b1-102">Операция Апплитомостка</span><span class="sxs-lookup"><span data-stu-id="bc8b1-102">ApplyToMostCA operation</span></span>

<span data-ttu-id="bc8b1-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="bc8b1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="bc8b1-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bc8b1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bc8b1-105">Применяет операцию ко всему элементу массива, кроме последнего.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostCA<'T> (op : ('T[] => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="bc8b1-106">Описание</span><span class="sxs-lookup"><span data-stu-id="bc8b1-106">Description</span></span>

<span data-ttu-id="bc8b1-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="bc8b1-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="bc8b1-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bc8b1-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="bc8b1-109">Op: 'T [] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="bc8b1-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="bc8b1-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="bc8b1-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="bc8b1-111">targets : 'T[]</span></span>

<span data-ttu-id="bc8b1-112">Массив целевых объектов, к которым будут применены все, кроме последнего `op` .</span><span class="sxs-lookup"><span data-stu-id="bc8b1-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bc8b1-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bc8b1-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="bc8b1-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="bc8b1-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="bc8b1-115">Е</span><span class="sxs-lookup"><span data-stu-id="bc8b1-115">'T</span></span>

<span data-ttu-id="bc8b1-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc8b1-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="bc8b1-117">See Also</span></span>

- [<span data-ttu-id="bc8b1-118">Microsoft. тактов. Canon. Апплитомост</span><span class="sxs-lookup"><span data-stu-id="bc8b1-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="bc8b1-119">Microsoft. тактов. Canon. Апплитомоста</span><span class="sxs-lookup"><span data-stu-id="bc8b1-119">Microsoft.Quantum.Canon.ApplyToMostA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [<span data-ttu-id="bc8b1-120">Microsoft. тактов. Canon. Апплитомостк</span><span class="sxs-lookup"><span data-stu-id="bc8b1-120">Microsoft.Quantum.Canon.ApplyToMostC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostC)