---
uid: Microsoft.Quantum.Canon.Delayed
title: Отложенная функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delayed
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 820a38c2b4de2e0151d55bd88fb4f69567182f6b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716252"
---
# <a name="delayed-function"></a><span data-ttu-id="853f0-102">Отложенная функция</span><span class="sxs-lookup"><span data-stu-id="853f0-102">Delayed function</span></span>

<span data-ttu-id="853f0-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="853f0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="853f0-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="853f0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="853f0-105">Возвращает операцию, которая применяет заданную операцию с заданным аргументом.</span><span class="sxs-lookup"><span data-stu-id="853f0-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function Delayed<'T, 'U> (op : ('T => 'U), arg : 'T) : (Unit => 'U)
```


## <a name="input"></a><span data-ttu-id="853f0-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="853f0-106">Input</span></span>

### <a name="op--t--u"></a><span data-ttu-id="853f0-107">Op: 'T => ' U</span><span class="sxs-lookup"><span data-stu-id="853f0-107">op : 'T => 'U</span></span> 

<span data-ttu-id="853f0-108">Операция, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="853f0-108">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="853f0-109">ARG: 'T</span><span class="sxs-lookup"><span data-stu-id="853f0-109">arg : 'T</span></span>

<span data-ttu-id="853f0-110">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="853f0-110">The input to which the operation is applied.</span></span>



## <a name="output--unit--u"></a><span data-ttu-id="853f0-111">Выходные данные: [Unit](xref:microsoft.quantum.lang-ref.unit) => ' U</span><span class="sxs-lookup"><span data-stu-id="853f0-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => 'U</span></span> 

<span data-ttu-id="853f0-112">Новая операция, которая применяется `op` с входными данными `arg`</span><span class="sxs-lookup"><span data-stu-id="853f0-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="853f0-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="853f0-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="853f0-114">Е</span><span class="sxs-lookup"><span data-stu-id="853f0-114">'T</span></span>

<span data-ttu-id="853f0-115">Входной тип операции, которая должна быть отложена.</span><span class="sxs-lookup"><span data-stu-id="853f0-115">The input type of the operation to be delayed.</span></span>
### <a name="u"></a><span data-ttu-id="853f0-116">' U</span><span class="sxs-lookup"><span data-stu-id="853f0-116">'U</span></span>

<span data-ttu-id="853f0-117">Возвращаемый тип операции, которая должна быть отложена.</span><span class="sxs-lookup"><span data-stu-id="853f0-117">The return type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="853f0-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="853f0-118">See Also</span></span>

- [<span data-ttu-id="853f0-119">Microsoft. тактов. Canon. Делайедк</span><span class="sxs-lookup"><span data-stu-id="853f0-119">Microsoft.Quantum.Canon.DelayedC</span></span>](xref:Microsoft.Quantum.Canon.DelayedC)
- [<span data-ttu-id="853f0-120">Microsoft. тактов. Canon. DELAYED</span><span class="sxs-lookup"><span data-stu-id="853f0-120">Microsoft.Quantum.Canon.DelayedA</span></span>](xref:Microsoft.Quantum.Canon.DelayedA)
- [<span data-ttu-id="853f0-121">Microsoft. тактов. Canon. Делайедка</span><span class="sxs-lookup"><span data-stu-id="853f0-121">Microsoft.Quantum.Canon.DelayedCA</span></span>](xref:Microsoft.Quantum.Canon.DelayedCA)
- [<span data-ttu-id="853f0-122">Microsoft. тактов. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="853f0-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)