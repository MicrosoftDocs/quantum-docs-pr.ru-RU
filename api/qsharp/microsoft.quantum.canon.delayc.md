---
uid: Microsoft.Quantum.Canon.DelayC
title: Операция Делайк
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayC
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: eba4c3bd9f472910e30e5ac8334f09471a685c5d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840638"
---
# <a name="delayc-operation"></a><span data-ttu-id="02e43-102">Операция Делайк</span><span class="sxs-lookup"><span data-stu-id="02e43-102">DelayC operation</span></span>

<span data-ttu-id="02e43-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="02e43-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="02e43-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="02e43-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="02e43-105">Применяет заданную операцию с задержкой.</span><span class="sxs-lookup"><span data-stu-id="02e43-105">Applies a given operation with a delay.</span></span>

```qsharp
operation DelayC<'T> (op : ('T => Unit is Ctl), arg : 'T, aux : Unit) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="02e43-106">Описание</span><span class="sxs-lookup"><span data-stu-id="02e43-106">Description</span></span>

<span data-ttu-id="02e43-107">При наличии операции и входных данных для этой операции применяет операцию, когда предоставляется дополнительный ввод.</span><span class="sxs-lookup"><span data-stu-id="02e43-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="02e43-108">В частности, выражение `Delay(op, arg, _)` является операцией, которая применяется `op` к `arg` при вызове.</span><span class="sxs-lookup"><span data-stu-id="02e43-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="02e43-109">Выражение `Delay(op,arg,_)` позволяет отложить применение `op` .</span><span class="sxs-lookup"><span data-stu-id="02e43-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="02e43-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="02e43-110">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="02e43-111">Op: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — CTL</span><span class="sxs-lookup"><span data-stu-id="02e43-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="02e43-112">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="02e43-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="02e43-113">ARG: 'T</span><span class="sxs-lookup"><span data-stu-id="02e43-113">arg : 'T</span></span>

<span data-ttu-id="02e43-114">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="02e43-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="02e43-115">AUX: [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="02e43-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="02e43-116">Аргумент, используемый для задержки применения операции с помощью частичного приложения.</span><span class="sxs-lookup"><span data-stu-id="02e43-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--unit"></a><span data-ttu-id="02e43-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="02e43-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="02e43-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="02e43-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="02e43-119">Е</span><span class="sxs-lookup"><span data-stu-id="02e43-119">'T</span></span>

<span data-ttu-id="02e43-120">Входной тип операции, которая должна быть отложена.</span><span class="sxs-lookup"><span data-stu-id="02e43-120">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="02e43-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="02e43-121">See Also</span></span>

- [<span data-ttu-id="02e43-122">Microsoft. тактов. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="02e43-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)
- [<span data-ttu-id="02e43-123">Microsoft. тактов. Canon. DELAYED</span><span class="sxs-lookup"><span data-stu-id="02e43-123">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)