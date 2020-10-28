---
uid: Microsoft.Quantum.Canon.DelayedCA
title: Функция Делайедка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedCA
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 8ee55e2ca7ec2cff9618b5dc66e19d88779d39ce
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716223"
---
# <a name="delayedca-function"></a><span data-ttu-id="3a06a-102">Функция Делайедка</span><span class="sxs-lookup"><span data-stu-id="3a06a-102">DelayedCA function</span></span>

<span data-ttu-id="3a06a-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3a06a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3a06a-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3a06a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3a06a-105">Возвращает операцию, которая применяет заданную операцию с заданным аргументом.</span><span class="sxs-lookup"><span data-stu-id="3a06a-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T) : (Unit => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="3a06a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3a06a-106">Input</span></span>

### <a name="op--t--unit-ctl--adj"></a><span data-ttu-id="3a06a-107">Op: t => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + прилагательные</span><span class="sxs-lookup"><span data-stu-id="3a06a-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="3a06a-108">Операция, применяемая в результате применения возвращаемого значения</span><span class="sxs-lookup"><span data-stu-id="3a06a-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="3a06a-109">ARG: 'T</span><span class="sxs-lookup"><span data-stu-id="3a06a-109">arg : 'T</span></span>

<span data-ttu-id="3a06a-110">Входные данные, к которым `op` применяется операция.</span><span class="sxs-lookup"><span data-stu-id="3a06a-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit-ctl--adj"></a><span data-ttu-id="3a06a-111">Выходные данные [:](xref:microsoft.quantum.lang-ref.unit) => [Units](xref:microsoft.quantum.lang-ref.unit) CTL + прилагательный</span><span class="sxs-lookup"><span data-stu-id="3a06a-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="3a06a-112">Новая операция, которая применяется `op` с входными данными `arg`</span><span class="sxs-lookup"><span data-stu-id="3a06a-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="3a06a-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="3a06a-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3a06a-114">Е</span><span class="sxs-lookup"><span data-stu-id="3a06a-114">'T</span></span>

<span data-ttu-id="3a06a-115">Входной тип операции, которая должна быть отложена.</span><span class="sxs-lookup"><span data-stu-id="3a06a-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="3a06a-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="3a06a-116">See Also</span></span>

- [<span data-ttu-id="3a06a-117">Microsoft. тактов. Canon. DELAYED</span><span class="sxs-lookup"><span data-stu-id="3a06a-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="3a06a-118">Microsoft. тактов. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="3a06a-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)