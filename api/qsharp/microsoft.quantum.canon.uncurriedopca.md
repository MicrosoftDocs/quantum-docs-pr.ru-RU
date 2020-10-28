---
uid: Microsoft.Quantum.Canon.UncurriedOpCA
title: Функция Ункурриедопка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpCA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `CA` indicates that the operations are controllable and adjointable.
ms.openlocfilehash: 6a0f2e1b345d0ba3ac5c779c5dc2bfffaf659a0b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715202"
---
# <a name="uncurriedopca-function"></a><span data-ttu-id="88485-102">Функция Ункурриедопка</span><span class="sxs-lookup"><span data-stu-id="88485-102">UncurriedOpCA function</span></span>

<span data-ttu-id="88485-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="88485-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="88485-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="88485-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="88485-105">При наличии функции, возвращающей операции, возвращает новую операцию, которая принимает оба входа как кортеж.</span><span class="sxs-lookup"><span data-stu-id="88485-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="88485-106">Модификатор `CA` указывает, что операции являются управляемыми и аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="88485-106">The modifier `CA` indicates that the operations are controllable and adjointable.</span></span>

```qsharp
function UncurriedOpCA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl + Adj))) : (('T, 'U) => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="88485-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="88485-107">Input</span></span>

### <a name="curriedop--t---u--unit-ctl--adj"></a><span data-ttu-id="88485-108">Курриедоп: не> "U => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + прилагательные</span><span class="sxs-lookup"><span data-stu-id="88485-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="88485-109">Функция, возвращающая операции.</span><span class="sxs-lookup"><span data-stu-id="88485-109">A function which returns operations.</span></span>



## <a name="output--tu--unit-ctl--adj"></a><span data-ttu-id="88485-110">Выходные данные: ('T, "U" => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + прилагательные</span><span class="sxs-lookup"><span data-stu-id="88485-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="88485-111">Новая операция `op` , которая `op(t, u)` эквивалентна `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="88485-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="88485-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="88485-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="88485-113">Е</span><span class="sxs-lookup"><span data-stu-id="88485-113">'T</span></span>

<span data-ttu-id="88485-114">Тип первого аргумента каррированных функции.</span><span class="sxs-lookup"><span data-stu-id="88485-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="88485-115">' U</span><span class="sxs-lookup"><span data-stu-id="88485-115">'U</span></span>

<span data-ttu-id="88485-116">Тип второго аргумента каррированных функции.</span><span class="sxs-lookup"><span data-stu-id="88485-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="88485-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="88485-117">See Also</span></span>

- [<span data-ttu-id="88485-118">Microsoft. тактов. Canon. Ункурриедоп</span><span class="sxs-lookup"><span data-stu-id="88485-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)