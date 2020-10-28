---
uid: Microsoft.Quantum.Canon.DelayCA
title: Операция Делайка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayCA
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: 4b4be55436d6619511a12c6fb7fbd0f23989152a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716266"
---
# <a name="delayca-operation"></a><span data-ttu-id="2e860-102">Операция Делайка</span><span class="sxs-lookup"><span data-stu-id="2e860-102">DelayCA operation</span></span>

<span data-ttu-id="2e860-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2e860-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2e860-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2e860-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2e860-105">Применяет заданную операцию с задержкой.</span><span class="sxs-lookup"><span data-stu-id="2e860-105">Applies a given operation with a delay.</span></span>

```qsharp
operation DelayCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T, aux : Unit) : Unit
```


## <a name="description"></a><span data-ttu-id="2e860-106">Описание</span><span class="sxs-lookup"><span data-stu-id="2e860-106">Description</span></span>

<span data-ttu-id="2e860-107">При наличии операции и входных данных для этой операции применяет операцию, когда предоставляется дополнительный ввод.</span><span class="sxs-lookup"><span data-stu-id="2e860-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="2e860-108">В частности, выражение `Delay(op, arg, _)` является операцией, которая применяется `op` к `arg` при вызове.</span><span class="sxs-lookup"><span data-stu-id="2e860-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="2e860-109">Выражение `Delay(op,arg,_)` позволяет отложить применение `op` .</span><span class="sxs-lookup"><span data-stu-id="2e860-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="2e860-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2e860-110">Input</span></span>

### <a name="op--t--unit-ctl--adj"></a><span data-ttu-id="2e860-111">Op: t => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + прилагательные</span><span class="sxs-lookup"><span data-stu-id="2e860-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="2e860-112">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="2e860-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="2e860-113">ARG: 'T</span><span class="sxs-lookup"><span data-stu-id="2e860-113">arg : 'T</span></span>

<span data-ttu-id="2e860-114">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="2e860-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="2e860-115">AUX: [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2e860-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="2e860-116">Аргумент, используемый для задержки применения операции с помощью частичного приложения.</span><span class="sxs-lookup"><span data-stu-id="2e860-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2e860-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2e860-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="2e860-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="2e860-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2e860-119">Е</span><span class="sxs-lookup"><span data-stu-id="2e860-119">'T</span></span>

<span data-ttu-id="2e860-120">Входной тип операции, которая должна быть отложена.</span><span class="sxs-lookup"><span data-stu-id="2e860-120">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e860-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="2e860-121">See Also</span></span>

- [<span data-ttu-id="2e860-122">Microsoft. тактов. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="2e860-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)
- [<span data-ttu-id="2e860-123">Microsoft. тактов. Canon. DELAYED</span><span class="sxs-lookup"><span data-stu-id="2e860-123">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)