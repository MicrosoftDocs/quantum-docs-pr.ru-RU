---
uid: Microsoft.Quantum.Canon.DelayedCA
title: Функция Делайедка
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedCA
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: c44e3448c471f2a20f995d4546ee54f3affb726e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840551"
---
# <a name="delayedca-function"></a><span data-ttu-id="75c87-102">Функция Делайедка</span><span class="sxs-lookup"><span data-stu-id="75c87-102">DelayedCA function</span></span>

<span data-ttu-id="75c87-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="75c87-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="75c87-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="75c87-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="75c87-105">Возвращает операцию, которая применяет заданную операцию с заданным аргументом.</span><span class="sxs-lookup"><span data-stu-id="75c87-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T) : (Unit => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="75c87-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="75c87-106">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="75c87-107">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="75c87-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="75c87-108">Операция, применяемая в результате применения возвращаемого значения</span><span class="sxs-lookup"><span data-stu-id="75c87-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="75c87-109">ARG: 'T</span><span class="sxs-lookup"><span data-stu-id="75c87-109">arg : 'T</span></span>

<span data-ttu-id="75c87-110">Входные данные, к которым `op` применяется операция.</span><span class="sxs-lookup"><span data-stu-id="75c87-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit--is-adj--ctl"></a><span data-ttu-id="75c87-111">Выходные данные: единица [измерения](xref:microsoft.quantum.lang-ref.unit) => [](xref:microsoft.quantum.lang-ref.unit) — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="75c87-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="75c87-112">Новая операция, которая применяется `op` с входными данными `arg`</span><span class="sxs-lookup"><span data-stu-id="75c87-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="75c87-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="75c87-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="75c87-114">Е</span><span class="sxs-lookup"><span data-stu-id="75c87-114">'T</span></span>

<span data-ttu-id="75c87-115">Входной тип операции, которая должна быть отложена.</span><span class="sxs-lookup"><span data-stu-id="75c87-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="75c87-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="75c87-116">See Also</span></span>

- [<span data-ttu-id="75c87-117">Microsoft. тактов. Canon. DELAYED</span><span class="sxs-lookup"><span data-stu-id="75c87-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="75c87-118">Microsoft. тактов. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="75c87-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)