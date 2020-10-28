---
uid: Microsoft.Quantum.Canon.DelayedC
title: Функция Делайедк
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedC
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 7cfd77b0bb2d91c5a1c4bb5bc84e052421d733a9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716210"
---
# <a name="delayedc-function"></a><span data-ttu-id="13c3b-102">Функция Делайедк</span><span class="sxs-lookup"><span data-stu-id="13c3b-102">DelayedC function</span></span>

<span data-ttu-id="13c3b-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="13c3b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="13c3b-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="13c3b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="13c3b-105">Возвращает операцию, которая применяет заданную операцию с заданным аргументом.</span><span class="sxs-lookup"><span data-stu-id="13c3b-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedC<'T> (op : ('T => Unit is Ctl), arg : 'T) : (Unit => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="13c3b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="13c3b-106">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="13c3b-107">Op: 'T => [единицы](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="13c3b-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="13c3b-108">Операция, применяемая в результате применения возвращаемого значения</span><span class="sxs-lookup"><span data-stu-id="13c3b-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="13c3b-109">ARG: 'T</span><span class="sxs-lookup"><span data-stu-id="13c3b-109">arg : 'T</span></span>

<span data-ttu-id="13c3b-110">Входные данные, к которым `op` применяется операция.</span><span class="sxs-lookup"><span data-stu-id="13c3b-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit-ctl"></a><span data-ttu-id="13c3b-111">Выходные данные [Unit](xref:microsoft.quantum.lang-ref.unit) : => список доверия [единиц](xref:microsoft.quantum.lang-ref.unit) измерения</span><span class="sxs-lookup"><span data-stu-id="13c3b-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="13c3b-112">Новая операция, которая применяется `op` с входными данными `arg`</span><span class="sxs-lookup"><span data-stu-id="13c3b-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="13c3b-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="13c3b-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="13c3b-114">Е</span><span class="sxs-lookup"><span data-stu-id="13c3b-114">'T</span></span>

<span data-ttu-id="13c3b-115">Входной тип операции, которая должна быть отложена.</span><span class="sxs-lookup"><span data-stu-id="13c3b-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="13c3b-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="13c3b-116">See Also</span></span>

- [<span data-ttu-id="13c3b-117">Microsoft. тактов. Canon. DELAYED</span><span class="sxs-lookup"><span data-stu-id="13c3b-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="13c3b-118">Microsoft. тактов. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="13c3b-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)