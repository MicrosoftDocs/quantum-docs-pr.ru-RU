---
uid: Microsoft.Quantum.Canon.ApplyToTailA
title: Операция Апплитотаила
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailA
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 2cacac14ad6e5003f1a50d9b84c4e0f96950dd7d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207927"
---
# <a name="applytotaila-operation"></a><span data-ttu-id="3e7fc-102">Операция Апплитотаила</span><span class="sxs-lookup"><span data-stu-id="3e7fc-102">ApplyToTailA operation</span></span>

<span data-ttu-id="3e7fc-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3e7fc-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3e7fc-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3e7fc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3e7fc-105">Применяет операцию к последнему элементу массива.</span><span class="sxs-lookup"><span data-stu-id="3e7fc-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailA<'T> (op : ('T => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="3e7fc-106">Описание</span><span class="sxs-lookup"><span data-stu-id="3e7fc-106">Description</span></span>

<span data-ttu-id="3e7fc-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="3e7fc-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="3e7fc-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3e7fc-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="3e7fc-109">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  является просуммой</span><span class="sxs-lookup"><span data-stu-id="3e7fc-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="3e7fc-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="3e7fc-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="3e7fc-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="3e7fc-111">targets : 'T[]</span></span>

<span data-ttu-id="3e7fc-112">Массив целевых объектов, к которым будет применен последний объект `op` .</span><span class="sxs-lookup"><span data-stu-id="3e7fc-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3e7fc-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3e7fc-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="3e7fc-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="3e7fc-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3e7fc-115">Е</span><span class="sxs-lookup"><span data-stu-id="3e7fc-115">'T</span></span>

<span data-ttu-id="3e7fc-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="3e7fc-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="3e7fc-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="3e7fc-117">See Also</span></span>

- [<span data-ttu-id="3e7fc-118">Microsoft. тактов. Canon. Апплитотаил</span><span class="sxs-lookup"><span data-stu-id="3e7fc-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="3e7fc-119">Microsoft. тактов. Canon. Апплитотаилк</span><span class="sxs-lookup"><span data-stu-id="3e7fc-119">Microsoft.Quantum.Canon.ApplyToTailC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailC)
- [<span data-ttu-id="3e7fc-120">Microsoft. тактов. Canon. Апплитотаилка</span><span class="sxs-lookup"><span data-stu-id="3e7fc-120">Microsoft.Quantum.Canon.ApplyToTailCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailCA)