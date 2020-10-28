---
uid: Microsoft.Quantum.Canon.ApplyIf
title: Операция Апплиф
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIf
qsharp.summary: Applies an operation conditioned on a classical bit.
ms.openlocfilehash: c8f6860a7a3b8af86b0edb048baccbf057dd245a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729600"
---
# <a name="applyif-operation"></a><span data-ttu-id="7ee13-102">Операция Апплиф</span><span class="sxs-lookup"><span data-stu-id="7ee13-102">ApplyIf operation</span></span>

<span data-ttu-id="7ee13-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7ee13-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7ee13-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7ee13-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7ee13-105">Применяет операцию с условием на Классический бит.</span><span class="sxs-lookup"><span data-stu-id="7ee13-105">Applies an operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIf<'T> (op : ('T => Unit), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="7ee13-106">Описание</span><span class="sxs-lookup"><span data-stu-id="7ee13-106">Description</span></span>

<span data-ttu-id="7ee13-107">При наличии операции `op` и битового значения `bit` применяется `op` к, `target` Если имеет `bit` значение `true` .</span><span class="sxs-lookup"><span data-stu-id="7ee13-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="7ee13-108">Если значение `false` равно, то ничего не происходит с `target` .</span><span class="sxs-lookup"><span data-stu-id="7ee13-108">If `false`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="7ee13-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7ee13-109">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="7ee13-110">Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="7ee13-110">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="7ee13-111">Операция, применяемая к условию.</span><span class="sxs-lookup"><span data-stu-id="7ee13-111">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="7ee13-112">bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="7ee13-112">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="7ee13-113">Логическое значение, определяющее, применяется ли оператор Op.</span><span class="sxs-lookup"><span data-stu-id="7ee13-113">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="7ee13-114">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="7ee13-114">target : 'T</span></span>

<span data-ttu-id="7ee13-115">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="7ee13-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7ee13-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7ee13-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="7ee13-117">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="7ee13-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7ee13-118">Е</span><span class="sxs-lookup"><span data-stu-id="7ee13-118">'T</span></span>

<span data-ttu-id="7ee13-119">Тип входных данных операции, которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="7ee13-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="7ee13-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="7ee13-120">See Also</span></span>

- [<span data-ttu-id="7ee13-121">Microsoft. тактов. Canon. Апплифк</span><span class="sxs-lookup"><span data-stu-id="7ee13-121">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="7ee13-122">Microsoft. тактов. Canon. Апплифа</span><span class="sxs-lookup"><span data-stu-id="7ee13-122">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="7ee13-123">Microsoft. тактов. Canon. Апплифка</span><span class="sxs-lookup"><span data-stu-id="7ee13-123">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)