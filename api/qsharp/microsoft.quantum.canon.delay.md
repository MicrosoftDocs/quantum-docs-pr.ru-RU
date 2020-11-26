---
uid: Microsoft.Quantum.Canon.Delay
title: Операция задержки
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delay
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: 4f45527faa49f79fccff3892e928fed09f9f0bc8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216512"
---
# <a name="delay-operation"></a><span data-ttu-id="73d5d-102">Операция задержки</span><span class="sxs-lookup"><span data-stu-id="73d5d-102">Delay operation</span></span>

<span data-ttu-id="73d5d-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="73d5d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="73d5d-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="73d5d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="73d5d-105">Применяет заданную операцию с задержкой.</span><span class="sxs-lookup"><span data-stu-id="73d5d-105">Applies a given operation with a delay.</span></span>

```qsharp
operation Delay<'T, 'U> (op : ('T => 'U), arg : 'T, aux : Unit) : 'U
```


## <a name="description"></a><span data-ttu-id="73d5d-106">Описание</span><span class="sxs-lookup"><span data-stu-id="73d5d-106">Description</span></span>

<span data-ttu-id="73d5d-107">При наличии операции и входных данных для этой операции применяет операцию, когда предоставляется дополнительный ввод.</span><span class="sxs-lookup"><span data-stu-id="73d5d-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="73d5d-108">В частности, выражение `Delay(op, arg, _)` является операцией, которая применяется `op` к `arg` при вызове.</span><span class="sxs-lookup"><span data-stu-id="73d5d-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="73d5d-109">Выражение `Delay(op,arg,_)` позволяет отложить применение `op` .</span><span class="sxs-lookup"><span data-stu-id="73d5d-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="73d5d-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="73d5d-110">Input</span></span>

### <a name="op--t--u"></a><span data-ttu-id="73d5d-111">Op: 'T => ' U</span><span class="sxs-lookup"><span data-stu-id="73d5d-111">op : 'T => 'U</span></span> 

<span data-ttu-id="73d5d-112">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="73d5d-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="73d5d-113">ARG: 'T</span><span class="sxs-lookup"><span data-stu-id="73d5d-113">arg : 'T</span></span>

<span data-ttu-id="73d5d-114">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="73d5d-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="73d5d-115">AUX: [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="73d5d-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="73d5d-116">Аргумент, используемый для задержки применения операции с помощью частичного приложения.</span><span class="sxs-lookup"><span data-stu-id="73d5d-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--u"></a><span data-ttu-id="73d5d-117">Выходные данные: ' U</span><span class="sxs-lookup"><span data-stu-id="73d5d-117">Output : 'U</span></span>



## <a name="type-parameters"></a><span data-ttu-id="73d5d-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="73d5d-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="73d5d-119">Е</span><span class="sxs-lookup"><span data-stu-id="73d5d-119">'T</span></span>

<span data-ttu-id="73d5d-120">Входной тип операции, которая должна быть отложена.</span><span class="sxs-lookup"><span data-stu-id="73d5d-120">The input type of the operation to be delayed.</span></span>
### <a name="u"></a><span data-ttu-id="73d5d-121">' U</span><span class="sxs-lookup"><span data-stu-id="73d5d-121">'U</span></span>

<span data-ttu-id="73d5d-122">Возвращаемый тип операции, которая должна быть отложена.</span><span class="sxs-lookup"><span data-stu-id="73d5d-122">The return type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="73d5d-123">См. также:</span><span class="sxs-lookup"><span data-stu-id="73d5d-123">See Also</span></span>

- [<span data-ttu-id="73d5d-124">Microsoft. тактов. Canon. Делайк</span><span class="sxs-lookup"><span data-stu-id="73d5d-124">Microsoft.Quantum.Canon.DelayC</span></span>](xref:Microsoft.Quantum.Canon.DelayC)
- [<span data-ttu-id="73d5d-125">Microsoft. тактов. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="73d5d-125">Microsoft.Quantum.Canon.DelayA</span></span>](xref:Microsoft.Quantum.Canon.DelayA)
- [<span data-ttu-id="73d5d-126">Microsoft. тактов. Canon. Делайка</span><span class="sxs-lookup"><span data-stu-id="73d5d-126">Microsoft.Quantum.Canon.DelayCA</span></span>](xref:Microsoft.Quantum.Canon.DelayCA)
- [<span data-ttu-id="73d5d-127">Microsoft. тактов. Canon. DELAYED</span><span class="sxs-lookup"><span data-stu-id="73d5d-127">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)