---
uid: Microsoft.Quantum.Canon.DelayA
title: Отложенная операция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayA
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: 77c40633824ccd9250252804b08d7400936515dd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716294"
---
# <a name="delaya-operation"></a><span data-ttu-id="c570b-102">Отложенная операция</span><span class="sxs-lookup"><span data-stu-id="c570b-102">DelayA operation</span></span>

<span data-ttu-id="c570b-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c570b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c570b-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c570b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c570b-105">Применяет заданную операцию с задержкой.</span><span class="sxs-lookup"><span data-stu-id="c570b-105">Applies a given operation with a delay.</span></span>

```qsharp
operation DelayA<'T> (op : ('T => Unit is Adj), arg : 'T, aux : Unit) : Unit
```


## <a name="description"></a><span data-ttu-id="c570b-106">Описание</span><span class="sxs-lookup"><span data-stu-id="c570b-106">Description</span></span>

<span data-ttu-id="c570b-107">При наличии операции и входных данных для этой операции применяет операцию, когда предоставляется дополнительный ввод.</span><span class="sxs-lookup"><span data-stu-id="c570b-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="c570b-108">В частности, выражение `Delay(op, arg, _)` является операцией, которая применяется `op` к `arg` при вызове.</span><span class="sxs-lookup"><span data-stu-id="c570b-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="c570b-109">Выражение `Delay(op,arg,_)` позволяет отложить применение `op` .</span><span class="sxs-lookup"><span data-stu-id="c570b-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="c570b-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c570b-110">Input</span></span>

### <a name="op--t--unit-adj"></a><span data-ttu-id="c570b-111">Op: 'T => [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c570b-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="c570b-112">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="c570b-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="c570b-113">ARG: 'T</span><span class="sxs-lookup"><span data-stu-id="c570b-113">arg : 'T</span></span>

<span data-ttu-id="c570b-114">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="c570b-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="c570b-115">AUX: [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c570b-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="c570b-116">Аргумент, используемый для задержки применения операции с помощью частичного приложения.</span><span class="sxs-lookup"><span data-stu-id="c570b-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c570b-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c570b-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c570b-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="c570b-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c570b-119">Е</span><span class="sxs-lookup"><span data-stu-id="c570b-119">'T</span></span>

<span data-ttu-id="c570b-120">Входной тип операции, которая должна быть отложена.</span><span class="sxs-lookup"><span data-stu-id="c570b-120">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="c570b-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="c570b-121">See Also</span></span>

- [<span data-ttu-id="c570b-122">Microsoft. тактов. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="c570b-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)
- [<span data-ttu-id="c570b-123">Microsoft. тактов. Canon. DELAYED</span><span class="sxs-lookup"><span data-stu-id="c570b-123">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)