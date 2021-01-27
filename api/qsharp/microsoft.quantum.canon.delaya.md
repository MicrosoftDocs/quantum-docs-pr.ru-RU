---
uid: Microsoft.Quantum.Canon.DelayA
title: Отложенная операция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayA
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: c7385cfcdf782347feb8d95311205a9311f4c929
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840667"
---
# <a name="delaya-operation"></a><span data-ttu-id="7f08f-102">Отложенная операция</span><span class="sxs-lookup"><span data-stu-id="7f08f-102">DelayA operation</span></span>

<span data-ttu-id="7f08f-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7f08f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7f08f-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7f08f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7f08f-105">Применяет заданную операцию с задержкой.</span><span class="sxs-lookup"><span data-stu-id="7f08f-105">Applies a given operation with a delay.</span></span>

```qsharp
operation DelayA<'T> (op : ('T => Unit is Adj), arg : 'T, aux : Unit) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="7f08f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="7f08f-106">Description</span></span>

<span data-ttu-id="7f08f-107">При наличии операции и входных данных для этой операции применяет операцию, когда предоставляется дополнительный ввод.</span><span class="sxs-lookup"><span data-stu-id="7f08f-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="7f08f-108">В частности, выражение `Delay(op, arg, _)` является операцией, которая применяется `op` к `arg` при вызове.</span><span class="sxs-lookup"><span data-stu-id="7f08f-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="7f08f-109">Выражение `Delay(op,arg,_)` позволяет отложить применение `op` .</span><span class="sxs-lookup"><span data-stu-id="7f08f-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="7f08f-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7f08f-110">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="7f08f-111">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  является просуммой</span><span class="sxs-lookup"><span data-stu-id="7f08f-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="7f08f-112">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="7f08f-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="7f08f-113">ARG: 'T</span><span class="sxs-lookup"><span data-stu-id="7f08f-113">arg : 'T</span></span>

<span data-ttu-id="7f08f-114">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="7f08f-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="7f08f-115">AUX: [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7f08f-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="7f08f-116">Аргумент, используемый для задержки применения операции с помощью частичного приложения.</span><span class="sxs-lookup"><span data-stu-id="7f08f-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7f08f-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7f08f-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="7f08f-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="7f08f-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7f08f-119">Е</span><span class="sxs-lookup"><span data-stu-id="7f08f-119">'T</span></span>

<span data-ttu-id="7f08f-120">Входной тип операции, которая должна быть отложена.</span><span class="sxs-lookup"><span data-stu-id="7f08f-120">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="7f08f-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="7f08f-121">See Also</span></span>

- [<span data-ttu-id="7f08f-122">Microsoft. тактов. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="7f08f-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)
- [<span data-ttu-id="7f08f-123">Microsoft. тактов. Canon. DELAYED</span><span class="sxs-lookup"><span data-stu-id="7f08f-123">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)