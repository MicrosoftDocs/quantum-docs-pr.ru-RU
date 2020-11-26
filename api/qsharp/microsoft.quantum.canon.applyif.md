---
uid: Microsoft.Quantum.Canon.ApplyIf
title: Операция Апплиф
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIf
qsharp.summary: Applies an operation conditioned on a classical bit.
ms.openlocfilehash: c5a1012328fa012ee02707aa59c94ac9c44b8e87
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218841"
---
# <a name="applyif-operation"></a><span data-ttu-id="7b6c3-102">Операция Апплиф</span><span class="sxs-lookup"><span data-stu-id="7b6c3-102">ApplyIf operation</span></span>

<span data-ttu-id="7b6c3-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7b6c3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7b6c3-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7b6c3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7b6c3-105">Применяет операцию с условием на Классический бит.</span><span class="sxs-lookup"><span data-stu-id="7b6c3-105">Applies an operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIf<'T> (op : ('T => Unit), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="7b6c3-106">Описание</span><span class="sxs-lookup"><span data-stu-id="7b6c3-106">Description</span></span>

<span data-ttu-id="7b6c3-107">При наличии операции `op` и битового значения `bit` применяется `op` к, `target` Если имеет `bit` значение `true` .</span><span class="sxs-lookup"><span data-stu-id="7b6c3-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="7b6c3-108">Если значение `false` равно, то ничего не происходит с `target` .</span><span class="sxs-lookup"><span data-stu-id="7b6c3-108">If `false`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="7b6c3-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7b6c3-109">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="7b6c3-110">Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="7b6c3-110">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="7b6c3-111">Операция, применяемая к условию.</span><span class="sxs-lookup"><span data-stu-id="7b6c3-111">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="7b6c3-112">bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="7b6c3-112">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="7b6c3-113">Логическое значение, определяющее, применяется ли оператор Op.</span><span class="sxs-lookup"><span data-stu-id="7b6c3-113">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="7b6c3-114">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="7b6c3-114">target : 'T</span></span>

<span data-ttu-id="7b6c3-115">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="7b6c3-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7b6c3-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7b6c3-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="7b6c3-117">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="7b6c3-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7b6c3-118">Е</span><span class="sxs-lookup"><span data-stu-id="7b6c3-118">'T</span></span>

<span data-ttu-id="7b6c3-119">Тип входных данных операции, которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="7b6c3-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="7b6c3-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="7b6c3-120">See Also</span></span>

- [<span data-ttu-id="7b6c3-121">Microsoft. тактов. Canon. Апплифк</span><span class="sxs-lookup"><span data-stu-id="7b6c3-121">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="7b6c3-122">Microsoft. тактов. Canon. Апплифа</span><span class="sxs-lookup"><span data-stu-id="7b6c3-122">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="7b6c3-123">Microsoft. тактов. Canon. Апплифка</span><span class="sxs-lookup"><span data-stu-id="7b6c3-123">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)