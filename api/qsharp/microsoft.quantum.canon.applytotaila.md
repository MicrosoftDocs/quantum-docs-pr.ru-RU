---
uid: Microsoft.Quantum.Canon.ApplyToTailA
title: Операция Апплитотаила
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailA
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: a84fa6c53f3e11bef82b8b83fffa1451a8299511
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716979"
---
# <a name="applytotaila-operation"></a><span data-ttu-id="a9533-102">Операция Апплитотаила</span><span class="sxs-lookup"><span data-stu-id="a9533-102">ApplyToTailA operation</span></span>

<span data-ttu-id="a9533-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a9533-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a9533-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a9533-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a9533-105">Применяет операцию к последнему элементу массива.</span><span class="sxs-lookup"><span data-stu-id="a9533-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailA<'T> (op : ('T => Unit is Adj), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="a9533-106">Описание</span><span class="sxs-lookup"><span data-stu-id="a9533-106">Description</span></span>

<span data-ttu-id="a9533-107">При наличии операции `op` и массива целевых объектов `targets` применяется `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="a9533-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="a9533-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a9533-108">Input</span></span>

### <a name="op--t--unit-adj"></a><span data-ttu-id="a9533-109">Op: 'T => [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a9533-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="a9533-110">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="a9533-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="a9533-111">targets: 'T []</span><span class="sxs-lookup"><span data-stu-id="a9533-111">targets : 'T[]</span></span>

<span data-ttu-id="a9533-112">Массив целевых объектов, к которым будет применен последний объект `op` .</span><span class="sxs-lookup"><span data-stu-id="a9533-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a9533-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a9533-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a9533-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="a9533-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a9533-115">Е</span><span class="sxs-lookup"><span data-stu-id="a9533-115">'T</span></span>

<span data-ttu-id="a9533-116">Тип входных данных операции, которая должна быть применена.</span><span class="sxs-lookup"><span data-stu-id="a9533-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="a9533-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="a9533-117">See Also</span></span>

- [<span data-ttu-id="a9533-118">Microsoft. тактов. Canon. Апплитотаил</span><span class="sxs-lookup"><span data-stu-id="a9533-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="a9533-119">Microsoft. тактов. Canon. Апплитотаилк</span><span class="sxs-lookup"><span data-stu-id="a9533-119">Microsoft.Quantum.Canon.ApplyToTailC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailC)
- [<span data-ttu-id="a9533-120">Microsoft. тактов. Canon. Апплитотаилка</span><span class="sxs-lookup"><span data-stu-id="a9533-120">Microsoft.Quantum.Canon.ApplyToTailCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailCA)