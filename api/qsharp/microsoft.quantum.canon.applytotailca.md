---
uid: Microsoft.Quantum.Canon.ApplyToTailCA
title: Операция Апплитотаилка
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailCA
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 4c702a9d310adae7a4ec404f3cf12893547623b0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841200"
---
# <a name="applytotailca-operation"></a><span data-ttu-id="79fa6-102">Операция Апплитотаилка</span><span class="sxs-lookup"><span data-stu-id="79fa6-102">ApplyToTailCA operation</span></span>

<span data-ttu-id="79fa6-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="79fa6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="79fa6-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="79fa6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="79fa6-105">Применяет операцию к последнему элементу массива.</span><span class="sxs-lookup"><span data-stu-id="79fa6-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailCA<'T> (op : ('T => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="79fa6-106">Описание</span><span class="sxs-lookup"><span data-stu-id="79fa6-106">Description</span></span>

<span data-ttu-id="79fa6-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="79fa6-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="79fa6-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="79fa6-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="79fa6-109">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="79fa6-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="79fa6-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="79fa6-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="79fa6-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="79fa6-111">targets : 'T[]</span></span>

<span data-ttu-id="79fa6-112">Массив целевых объектов, к которым будет применен последний объект `op` .</span><span class="sxs-lookup"><span data-stu-id="79fa6-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="79fa6-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="79fa6-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="79fa6-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="79fa6-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="79fa6-115">Е</span><span class="sxs-lookup"><span data-stu-id="79fa6-115">'T</span></span>

<span data-ttu-id="79fa6-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="79fa6-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="79fa6-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="79fa6-117">See Also</span></span>

- [<span data-ttu-id="79fa6-118">Microsoft. тактов. Canon. Апплитотаил</span><span class="sxs-lookup"><span data-stu-id="79fa6-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="79fa6-119">Microsoft. тактов. Canon. Апплитотаила</span><span class="sxs-lookup"><span data-stu-id="79fa6-119">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="79fa6-120">Microsoft. тактов. Canon. Апплитотаилк</span><span class="sxs-lookup"><span data-stu-id="79fa6-120">Microsoft.Quantum.Canon.ApplyToTailC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailC)