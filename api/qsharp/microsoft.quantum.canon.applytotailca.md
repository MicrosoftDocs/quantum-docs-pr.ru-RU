---
uid: Microsoft.Quantum.Canon.ApplyToTailCA
title: Операция Апплитотаилка
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailCA
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: afb9eaa277814d7434b00a5c853a0c002190c1ae
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207859"
---
# <a name="applytotailca-operation"></a><span data-ttu-id="40c68-102">Операция Апплитотаилка</span><span class="sxs-lookup"><span data-stu-id="40c68-102">ApplyToTailCA operation</span></span>

<span data-ttu-id="40c68-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="40c68-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="40c68-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="40c68-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="40c68-105">Применяет операцию к последнему элементу массива.</span><span class="sxs-lookup"><span data-stu-id="40c68-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailCA<'T> (op : ('T => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="40c68-106">Описание</span><span class="sxs-lookup"><span data-stu-id="40c68-106">Description</span></span>

<span data-ttu-id="40c68-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="40c68-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="40c68-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="40c68-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="40c68-109">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="40c68-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="40c68-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="40c68-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="40c68-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="40c68-111">targets : 'T[]</span></span>

<span data-ttu-id="40c68-112">Массив целевых объектов, к которым будет применен последний объект `op` .</span><span class="sxs-lookup"><span data-stu-id="40c68-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="40c68-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="40c68-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="40c68-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="40c68-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="40c68-115">Е</span><span class="sxs-lookup"><span data-stu-id="40c68-115">'T</span></span>

<span data-ttu-id="40c68-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="40c68-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="40c68-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="40c68-117">See Also</span></span>

- [<span data-ttu-id="40c68-118">Microsoft. тактов. Canon. Апплитотаил</span><span class="sxs-lookup"><span data-stu-id="40c68-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="40c68-119">Microsoft. тактов. Canon. Апплитотаила</span><span class="sxs-lookup"><span data-stu-id="40c68-119">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="40c68-120">Microsoft. тактов. Canon. Апплитотаилк</span><span class="sxs-lookup"><span data-stu-id="40c68-120">Microsoft.Quantum.Canon.ApplyToTailC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailC)