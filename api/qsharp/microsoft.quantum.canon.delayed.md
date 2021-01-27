---
uid: Microsoft.Quantum.Canon.Delayed
title: Отложенная функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delayed
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 40fcc7d0a178fdb18437b4d6c96542db593347b4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840591"
---
# <a name="delayed-function"></a><span data-ttu-id="e7edd-102">Отложенная функция</span><span class="sxs-lookup"><span data-stu-id="e7edd-102">Delayed function</span></span>

<span data-ttu-id="e7edd-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e7edd-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e7edd-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e7edd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e7edd-105">Возвращает операцию, которая применяет заданную операцию с заданным аргументом.</span><span class="sxs-lookup"><span data-stu-id="e7edd-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function Delayed<'T, 'U> (op : ('T => 'U), arg : 'T) : (Unit => 'U)
```


## <a name="input"></a><span data-ttu-id="e7edd-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e7edd-106">Input</span></span>

### <a name="op--t--u"></a><span data-ttu-id="e7edd-107">Op: 'T => ' U</span><span class="sxs-lookup"><span data-stu-id="e7edd-107">op : 'T => 'U</span></span> 

<span data-ttu-id="e7edd-108">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="e7edd-108">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="e7edd-109">ARG: 'T</span><span class="sxs-lookup"><span data-stu-id="e7edd-109">arg : 'T</span></span>

<span data-ttu-id="e7edd-110">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="e7edd-110">The input to which the operation is applied.</span></span>



## <a name="output--unit--u"></a><span data-ttu-id="e7edd-111">Выходные данные: [Unit](xref:microsoft.quantum.lang-ref.unit) => ' U</span><span class="sxs-lookup"><span data-stu-id="e7edd-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => 'U</span></span> 

<span data-ttu-id="e7edd-112">Новая операция, которая применяется `op` с входными данными `arg`</span><span class="sxs-lookup"><span data-stu-id="e7edd-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e7edd-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="e7edd-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e7edd-114">Е</span><span class="sxs-lookup"><span data-stu-id="e7edd-114">'T</span></span>

<span data-ttu-id="e7edd-115">Входной тип операции, которая должна быть отложена.</span><span class="sxs-lookup"><span data-stu-id="e7edd-115">The input type of the operation to be delayed.</span></span>
### <a name="u"></a><span data-ttu-id="e7edd-116">' U</span><span class="sxs-lookup"><span data-stu-id="e7edd-116">'U</span></span>

<span data-ttu-id="e7edd-117">Возвращаемый тип операции, которая должна быть отложена.</span><span class="sxs-lookup"><span data-stu-id="e7edd-117">The return type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7edd-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="e7edd-118">See Also</span></span>

- [<span data-ttu-id="e7edd-119">Microsoft. тактов. Canon. Делайедк</span><span class="sxs-lookup"><span data-stu-id="e7edd-119">Microsoft.Quantum.Canon.DelayedC</span></span>](xref:Microsoft.Quantum.Canon.DelayedC)
- [<span data-ttu-id="e7edd-120">Microsoft. тактов. Canon. DELAYED</span><span class="sxs-lookup"><span data-stu-id="e7edd-120">Microsoft.Quantum.Canon.DelayedA</span></span>](xref:Microsoft.Quantum.Canon.DelayedA)
- [<span data-ttu-id="e7edd-121">Microsoft. тактов. Canon. Делайедка</span><span class="sxs-lookup"><span data-stu-id="e7edd-121">Microsoft.Quantum.Canon.DelayedCA</span></span>](xref:Microsoft.Quantum.Canon.DelayedCA)
- [<span data-ttu-id="e7edd-122">Microsoft. тактов. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="e7edd-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)