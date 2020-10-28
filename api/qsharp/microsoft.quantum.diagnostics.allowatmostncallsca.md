---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNCallsCA
title: Операция Алловатмостнкаллска
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNCallsCA
qsharp.summary: Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.
ms.openlocfilehash: 1a9975d2d2026749238430b247cf47738de545cd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713060"
---
# <a name="allowatmostncallsca-operation"></a><span data-ttu-id="c3ab2-102">Операция Алловатмостнкаллска</span><span class="sxs-lookup"><span data-stu-id="c3ab2-102">AllowAtMostNCallsCA operation</span></span>

<span data-ttu-id="c3ab2-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="c3ab2-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="c3ab2-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c3ab2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c3ab2-105">Между вызовом этой операции и ее прилегающим объектом утверждается, что данная операция вызывается не чаще определенного числа раз.</span><span class="sxs-lookup"><span data-stu-id="c3ab2-105">Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.</span></span>

```qsharp
operation AllowAtMostNCallsCA<'TInput, 'TOutput> (nTimes : Int, op : ('TInput => 'TOutput is Adj + Ctl), message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="c3ab2-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c3ab2-106">Input</span></span>

### <a name="ntimes--int"></a><span data-ttu-id="c3ab2-107">Нтимес: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c3ab2-107">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c3ab2-108">Максимальное число вызовов, которое `op` может быть вызвано.</span><span class="sxs-lookup"><span data-stu-id="c3ab2-108">The maximum number of times that `op` may be called.</span></span>


### <a name="op--tinput--toutput-adj--ctl"></a><span data-ttu-id="c3ab2-109">Op: ' Тинпут => ' Таутпут года + CTL</span><span class="sxs-lookup"><span data-stu-id="c3ab2-109">op : 'TInput => 'TOutput Adj + Ctl</span></span>

<span data-ttu-id="c3ab2-110">Операция, вызовы которой должны быть ограничены.</span><span class="sxs-lookup"><span data-stu-id="c3ab2-110">An operation whose calls are to be restricted.</span></span>


### <a name="message--string"></a><span data-ttu-id="c3ab2-111">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="c3ab2-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="c3ab2-112">Сообщение, отображаемое при сбое.</span><span class="sxs-lookup"><span data-stu-id="c3ab2-112">A message to be displayed upon failure.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c3ab2-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c3ab2-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c3ab2-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="c3ab2-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="c3ab2-115">' Тинпут</span><span class="sxs-lookup"><span data-stu-id="c3ab2-115">'TInput</span></span>


### <a name="toutput"></a><span data-ttu-id="c3ab2-116">' Таутпут</span><span class="sxs-lookup"><span data-stu-id="c3ab2-116">'TOutput</span></span>



## <a name="remarks"></a><span data-ttu-id="c3ab2-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="c3ab2-117">Remarks</span></span>

<span data-ttu-id="c3ab2-118">Эта операция может быть заменена на неработающие целевые объекты, которые не поддерживают эту операцию.</span><span class="sxs-lookup"><span data-stu-id="c3ab2-118">This operation may be replaced by a no-op on targets which do not support it.</span></span>