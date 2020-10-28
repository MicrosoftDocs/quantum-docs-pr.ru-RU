---
uid: Microsoft.Quantum.Canon.UncurriedOpA
title: Функция Ункурриедопа
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `A` indicates that the operations are adjointable.
ms.openlocfilehash: 21df20354ad2388891f32b1bf1c7781287904983
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715216"
---
# <a name="uncurriedopa-function"></a><span data-ttu-id="ad59f-102">Функция Ункурриедопа</span><span class="sxs-lookup"><span data-stu-id="ad59f-102">UncurriedOpA function</span></span>

<span data-ttu-id="ad59f-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ad59f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ad59f-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ad59f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ad59f-105">При наличии функции, возвращающей операции, возвращает новую операцию, которая принимает оба входа как кортеж.</span><span class="sxs-lookup"><span data-stu-id="ad59f-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="ad59f-106">Модификатор `A` указывает, что операции являются аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="ad59f-106">The modifier `A` indicates that the operations are adjointable.</span></span>

```qsharp
function UncurriedOpA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Adj))) : (('T, 'U) => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="ad59f-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ad59f-107">Input</span></span>

### <a name="curriedop--t---u--unit-adj"></a><span data-ttu-id="ad59f-108">Курриедоп: не> "U [=>ные](xref:microsoft.quantum.lang-ref.unit) года</span><span class="sxs-lookup"><span data-stu-id="ad59f-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="ad59f-109">Функция, возвращающая операции.</span><span class="sxs-lookup"><span data-stu-id="ad59f-109">A function which returns operations.</span></span>



## <a name="output--tu--unit-adj"></a><span data-ttu-id="ad59f-110">Выходные данные: ('T, ' U) = [>ная](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="ad59f-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="ad59f-111">Новая операция `op` , которая `op(t, u)` эквивалентна `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="ad59f-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ad59f-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="ad59f-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ad59f-113">Е</span><span class="sxs-lookup"><span data-stu-id="ad59f-113">'T</span></span>

<span data-ttu-id="ad59f-114">Тип первого аргумента каррированных функции.</span><span class="sxs-lookup"><span data-stu-id="ad59f-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="ad59f-115">' U</span><span class="sxs-lookup"><span data-stu-id="ad59f-115">'U</span></span>

<span data-ttu-id="ad59f-116">Тип второго аргумента каррированных функции.</span><span class="sxs-lookup"><span data-stu-id="ad59f-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad59f-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="ad59f-117">See Also</span></span>

- [<span data-ttu-id="ad59f-118">Microsoft. тактов. Canon. Ункурриедоп</span><span class="sxs-lookup"><span data-stu-id="ad59f-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)