---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNCallsCA
title: Операция Алловатмостнкаллска
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNCallsCA
qsharp.summary: Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.
ms.openlocfilehash: bb6ba2615b571b0d9d056b93f8e36d2dec0c4a21
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853538"
---
# <a name="allowatmostncallsca-operation"></a><span data-ttu-id="4db94-102">Операция Алловатмостнкаллска</span><span class="sxs-lookup"><span data-stu-id="4db94-102">AllowAtMostNCallsCA operation</span></span>

<span data-ttu-id="4db94-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="4db94-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="4db94-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4db94-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4db94-105">Между вызовом этой операции и ее прилегающим объектом утверждается, что данная операция вызывается не чаще определенного числа раз.</span><span class="sxs-lookup"><span data-stu-id="4db94-105">Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.</span></span>

```qsharp
operation AllowAtMostNCallsCA<'TInput, 'TOutput> (nTimes : Int, op : ('TInput => 'TOutput is Adj + Ctl), message : String) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="4db94-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4db94-106">Input</span></span>

### <a name="ntimes--int"></a><span data-ttu-id="4db94-107">Нтимес: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4db94-107">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4db94-108">Максимальное число вызовов, которое `op` может быть вызвано.</span><span class="sxs-lookup"><span data-stu-id="4db94-108">The maximum number of times that `op` may be called.</span></span>


### <a name="op--tinput--toutput--is-adj--ctl"></a><span data-ttu-id="4db94-109">Op: "Тинпут =>" Таутпут — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="4db94-109">op : 'TInput => 'TOutput  is Adj + Ctl</span></span>

<span data-ttu-id="4db94-110">Операция, вызовы которой должны быть ограничены.</span><span class="sxs-lookup"><span data-stu-id="4db94-110">An operation whose calls are to be restricted.</span></span>


### <a name="message--string"></a><span data-ttu-id="4db94-111">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="4db94-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="4db94-112">Сообщение, отображаемое при сбое.</span><span class="sxs-lookup"><span data-stu-id="4db94-112">A message to be displayed upon failure.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4db94-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4db94-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="4db94-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="4db94-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="4db94-115">' Тинпут</span><span class="sxs-lookup"><span data-stu-id="4db94-115">'TInput</span></span>


### <a name="toutput"></a><span data-ttu-id="4db94-116">' Таутпут</span><span class="sxs-lookup"><span data-stu-id="4db94-116">'TOutput</span></span>



## <a name="example"></a><span data-ttu-id="4db94-117">Пример</span><span class="sxs-lookup"><span data-stu-id="4db94-117">Example</span></span>

<span data-ttu-id="4db94-118">Следующий фрагмент кода завершится ошибкой при выполнении на компьютерах, поддерживающих эту диагностику:</span><span class="sxs-lookup"><span data-stu-id="4db94-118">The following snippet will fail when executed on machines which support this diagnostic:</span></span>

```qsharp
using (register = Qubit[4]) {
    within {
        AllowAtMostNCallsCA(3, H, "Too many calls to H.");
    } apply {
        // Fails since this calls H four times, rather than the
        // allowed maximum of three.
        ApplyToEach(H, register);
    }
}
```

## <a name="remarks"></a><span data-ttu-id="4db94-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="4db94-119">Remarks</span></span>

<span data-ttu-id="4db94-120">Эта операция может быть заменена на неработающие целевые объекты, которые не поддерживают эту операцию.</span><span class="sxs-lookup"><span data-stu-id="4db94-120">This operation may be replaced by a no-op on targets which do not support it.</span></span>