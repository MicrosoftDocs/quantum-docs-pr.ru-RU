---
uid: Microsoft.Quantum.Canon.UncurriedOp
title: Функция Ункурриедоп
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOp
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple.
ms.openlocfilehash: cad508f166d4af805cb98cd21a0260d9babb6a4c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204646"
---
# <a name="uncurriedop-function"></a><span data-ttu-id="7834b-102">Функция Ункурриедоп</span><span class="sxs-lookup"><span data-stu-id="7834b-102">UncurriedOp function</span></span>

<span data-ttu-id="7834b-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7834b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7834b-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7834b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7834b-105">При наличии функции, возвращающей операции, возвращает новую операцию, которая принимает оба входа как кортеж.</span><span class="sxs-lookup"><span data-stu-id="7834b-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>

```qsharp
function UncurriedOp<'T, 'U> (curriedOp : ('T -> ('U => Unit))) : (('T, 'U) => Unit)
```


## <a name="input"></a><span data-ttu-id="7834b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7834b-106">Input</span></span>

### <a name="curriedop--t---u--unit"></a><span data-ttu-id="7834b-107">Курриедоп: не> "U = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="7834b-107">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="7834b-108">Функция, возвращающая операции.</span><span class="sxs-lookup"><span data-stu-id="7834b-108">A function which returns operations.</span></span>



## <a name="output--tu--unit"></a><span data-ttu-id="7834b-109">Выходные данные: ('T, ' U) = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="7834b-109">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="7834b-110">Новая операция `op` , которая `op(t, u)` эквивалентна `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="7834b-110">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7834b-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="7834b-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7834b-112">Е</span><span class="sxs-lookup"><span data-stu-id="7834b-112">'T</span></span>

<span data-ttu-id="7834b-113">Тип первого входного параметра для перекаррированных операции.</span><span class="sxs-lookup"><span data-stu-id="7834b-113">The type of the first input to a curried operation.</span></span>
### <a name="u"></a><span data-ttu-id="7834b-114">' U</span><span class="sxs-lookup"><span data-stu-id="7834b-114">'U</span></span>

<span data-ttu-id="7834b-115">Тип второго входного параметра для перекаррированных операции.</span><span class="sxs-lookup"><span data-stu-id="7834b-115">The type of the second input to a curried operation.</span></span>

## <a name="see-also"></a><span data-ttu-id="7834b-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="7834b-116">See Also</span></span>

- [<span data-ttu-id="7834b-117">Microsoft. тактов. Canon. Ункурриедопк</span><span class="sxs-lookup"><span data-stu-id="7834b-117">Microsoft.Quantum.Canon.UncurriedOpC</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpC)
- [<span data-ttu-id="7834b-118">Microsoft. тактов. Canon. Ункурриедопа</span><span class="sxs-lookup"><span data-stu-id="7834b-118">Microsoft.Quantum.Canon.UncurriedOpA</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpA)
- [<span data-ttu-id="7834b-119">Microsoft. тактов. Canon. Ункурриедопка</span><span class="sxs-lookup"><span data-stu-id="7834b-119">Microsoft.Quantum.Canon.UncurriedOpCA</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpCA)