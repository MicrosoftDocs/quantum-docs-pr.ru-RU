---
uid: Microsoft.Quantum.Canon.DelayedCA
title: Функция Делайедка
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedCA
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: fe2babb87d716185286b0864745f7ff6e637f8a1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207022"
---
# <a name="delayedca-function"></a><span data-ttu-id="7fbb6-102">Функция Делайедка</span><span class="sxs-lookup"><span data-stu-id="7fbb6-102">DelayedCA function</span></span>

<span data-ttu-id="7fbb6-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7fbb6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7fbb6-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7fbb6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7fbb6-105">Возвращает операцию, которая применяет заданную операцию с заданным аргументом.</span><span class="sxs-lookup"><span data-stu-id="7fbb6-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T) : (Unit => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="7fbb6-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7fbb6-106">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="7fbb6-107">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="7fbb6-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="7fbb6-108">Операция, применяемая в результате применения возвращаемого значения</span><span class="sxs-lookup"><span data-stu-id="7fbb6-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="7fbb6-109">ARG: 'T</span><span class="sxs-lookup"><span data-stu-id="7fbb6-109">arg : 'T</span></span>

<span data-ttu-id="7fbb6-110">Входные данные, к которым `op` применяется операция.</span><span class="sxs-lookup"><span data-stu-id="7fbb6-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit--is-adj--ctl"></a><span data-ttu-id="7fbb6-111">Выходные данные: единица [измерения](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="7fbb6-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="7fbb6-112">Новая операция, которая применяется `op` с входными данными `arg`</span><span class="sxs-lookup"><span data-stu-id="7fbb6-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7fbb6-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="7fbb6-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7fbb6-114">Е</span><span class="sxs-lookup"><span data-stu-id="7fbb6-114">'T</span></span>

<span data-ttu-id="7fbb6-115">Входной тип операции, которая должна быть отложена.</span><span class="sxs-lookup"><span data-stu-id="7fbb6-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="7fbb6-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="7fbb6-116">See Also</span></span>

- [<span data-ttu-id="7fbb6-117">Microsoft. тактов. Canon. DELAYED</span><span class="sxs-lookup"><span data-stu-id="7fbb6-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="7fbb6-118">Microsoft. тактов. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="7fbb6-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)