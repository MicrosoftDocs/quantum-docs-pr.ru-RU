---
uid: Microsoft.Quantum.Canon.DelayedC
title: Функция Делайедк
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedC
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: a1f2582668131816b774bf4a8b7476d9f1ee8cad
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840564"
---
# <a name="delayedc-function"></a><span data-ttu-id="09a4d-102">Функция Делайедк</span><span class="sxs-lookup"><span data-stu-id="09a4d-102">DelayedC function</span></span>

<span data-ttu-id="09a4d-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="09a4d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="09a4d-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="09a4d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="09a4d-105">Возвращает операцию, которая применяет заданную операцию с заданным аргументом.</span><span class="sxs-lookup"><span data-stu-id="09a4d-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedC<'T> (op : ('T => Unit is Ctl), arg : 'T) : (Unit => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="09a4d-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="09a4d-106">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="09a4d-107">Op: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — CTL</span><span class="sxs-lookup"><span data-stu-id="09a4d-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="09a4d-108">Операция, применяемая в результате применения возвращаемого значения</span><span class="sxs-lookup"><span data-stu-id="09a4d-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="09a4d-109">ARG: 'T</span><span class="sxs-lookup"><span data-stu-id="09a4d-109">arg : 'T</span></span>

<span data-ttu-id="09a4d-110">Входные данные, к которым `op` применяется операция.</span><span class="sxs-lookup"><span data-stu-id="09a4d-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit--is-ctl"></a><span data-ttu-id="09a4d-111">Выходные данные [](xref:microsoft.quantum.lang-ref.unit) : => [единица](xref:microsoft.quantum.lang-ref.unit) измерения — CTL</span><span class="sxs-lookup"><span data-stu-id="09a4d-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="09a4d-112">Новая операция, которая применяется `op` с входными данными `arg`</span><span class="sxs-lookup"><span data-stu-id="09a4d-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="09a4d-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="09a4d-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="09a4d-114">Е</span><span class="sxs-lookup"><span data-stu-id="09a4d-114">'T</span></span>

<span data-ttu-id="09a4d-115">Входной тип операции, которая должна быть отложена.</span><span class="sxs-lookup"><span data-stu-id="09a4d-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="09a4d-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="09a4d-116">See Also</span></span>

- [<span data-ttu-id="09a4d-117">Microsoft. тактов. Canon. DELAYED</span><span class="sxs-lookup"><span data-stu-id="09a4d-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="09a4d-118">Microsoft. тактов. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="09a4d-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)