---
uid: Microsoft.Quantum.Canon.UncurriedOpC
title: Функция Ункурриедопк
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpC
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `C` indicates that the operations are controllable.
ms.openlocfilehash: f3e5ecf3f7df0393dfbb948f064c27505f04cfcf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715215"
---
# <a name="uncurriedopc-function"></a><span data-ttu-id="9099b-102">Функция Ункурриедопк</span><span class="sxs-lookup"><span data-stu-id="9099b-102">UncurriedOpC function</span></span>

<span data-ttu-id="9099b-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9099b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9099b-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9099b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9099b-105">При наличии функции, возвращающей операции, возвращает новую операцию, которая принимает оба входа как кортеж.</span><span class="sxs-lookup"><span data-stu-id="9099b-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="9099b-106">Модификатор `C` указывает, что операции являются управляемыми.</span><span class="sxs-lookup"><span data-stu-id="9099b-106">The modifier `C` indicates that the operations are controllable.</span></span>

```qsharp
function UncurriedOpC<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl))) : (('T, 'U) => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="9099b-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9099b-107">Input</span></span>

### <a name="curriedop--t---u--unit-ctl"></a><span data-ttu-id="9099b-108">Курриедоп: не> "U = список доверия для [единицы](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="9099b-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="9099b-109">Функция, возвращающая операции.</span><span class="sxs-lookup"><span data-stu-id="9099b-109">A function which returns operations.</span></span>



## <a name="output--tu--unit-ctl"></a><span data-ttu-id="9099b-110">Выходные данные: ('T, ' U) => [единицы](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="9099b-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="9099b-111">Новая операция `op` , которая `op(t, u)` эквивалентна `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="9099b-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9099b-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="9099b-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9099b-113">Е</span><span class="sxs-lookup"><span data-stu-id="9099b-113">'T</span></span>

<span data-ttu-id="9099b-114">Тип первого аргумента каррированных функции.</span><span class="sxs-lookup"><span data-stu-id="9099b-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="9099b-115">' U</span><span class="sxs-lookup"><span data-stu-id="9099b-115">'U</span></span>

<span data-ttu-id="9099b-116">Тип второго аргумента каррированных функции.</span><span class="sxs-lookup"><span data-stu-id="9099b-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="9099b-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="9099b-117">See Also</span></span>

- [<span data-ttu-id="9099b-118">Microsoft. тактов. Canon. Ункурриедоп</span><span class="sxs-lookup"><span data-stu-id="9099b-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)