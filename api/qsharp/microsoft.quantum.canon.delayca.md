---
uid: Microsoft.Quantum.Canon.DelayCA
title: Операция Делайка
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayCA
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: a32a4f4a3f5d0f253a4c4eaf28c67db8da978b0b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207094"
---
# <a name="delayca-operation"></a><span data-ttu-id="03718-102">Операция Делайка</span><span class="sxs-lookup"><span data-stu-id="03718-102">DelayCA operation</span></span>

<span data-ttu-id="03718-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="03718-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="03718-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="03718-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="03718-105">Применяет заданную операцию с задержкой.</span><span class="sxs-lookup"><span data-stu-id="03718-105">Applies a given operation with a delay.</span></span>

```qsharp
operation DelayCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T, aux : Unit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="03718-106">Описание</span><span class="sxs-lookup"><span data-stu-id="03718-106">Description</span></span>

<span data-ttu-id="03718-107">При наличии операции и входных данных для этой операции применяет операцию, когда предоставляется дополнительный ввод.</span><span class="sxs-lookup"><span data-stu-id="03718-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="03718-108">В частности, выражение `Delay(op, arg, _)` является операцией, которая применяется `op` к `arg` при вызове.</span><span class="sxs-lookup"><span data-stu-id="03718-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="03718-109">Выражение `Delay(op,arg,_)` позволяет отложить применение `op` .</span><span class="sxs-lookup"><span data-stu-id="03718-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="03718-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="03718-110">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="03718-111">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="03718-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="03718-112">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="03718-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="03718-113">ARG: 'T</span><span class="sxs-lookup"><span data-stu-id="03718-113">arg : 'T</span></span>

<span data-ttu-id="03718-114">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="03718-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="03718-115">AUX: [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="03718-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="03718-116">Аргумент, используемый для задержки применения операции с помощью частичного приложения.</span><span class="sxs-lookup"><span data-stu-id="03718-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--unit"></a><span data-ttu-id="03718-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="03718-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="03718-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="03718-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="03718-119">Е</span><span class="sxs-lookup"><span data-stu-id="03718-119">'T</span></span>

<span data-ttu-id="03718-120">Входной тип операции, которая должна быть отложена.</span><span class="sxs-lookup"><span data-stu-id="03718-120">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="03718-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="03718-121">See Also</span></span>

- [<span data-ttu-id="03718-122">Microsoft. тактов. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="03718-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)
- [<span data-ttu-id="03718-123">Microsoft. тактов. Canon. DELAYED</span><span class="sxs-lookup"><span data-stu-id="03718-123">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)