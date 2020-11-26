---
uid: Microsoft.Quantum.Canon.UncurriedOpCA
title: Функция Ункурриедопка
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpCA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `CA` indicates that the operations are controllable and adjointable.
ms.openlocfilehash: 45526c0202e417213aab3fe7819827588e794e23
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216393"
---
# <a name="uncurriedopca-function"></a><span data-ttu-id="2a6eb-102">Функция Ункурриедопка</span><span class="sxs-lookup"><span data-stu-id="2a6eb-102">UncurriedOpCA function</span></span>

<span data-ttu-id="2a6eb-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2a6eb-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2a6eb-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2a6eb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2a6eb-105">При наличии функции, возвращающей операции, возвращает новую операцию, которая принимает оба входа как кортеж.</span><span class="sxs-lookup"><span data-stu-id="2a6eb-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="2a6eb-106">Модификатор `CA` указывает, что операции являются управляемыми и аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="2a6eb-106">The modifier `CA` indicates that the operations are controllable and adjointable.</span></span>

```qsharp
function UncurriedOpCA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl + Adj))) : (('T, 'U) => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="2a6eb-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2a6eb-107">Input</span></span>

### <a name="curriedop--t---u--unit--is-adj--ctl"></a><span data-ttu-id="2a6eb-108">Курриедоп: не> "U = [единица](xref:microsoft.quantum.lang-ref.unit) > является" суммой + CTL "</span><span class="sxs-lookup"><span data-stu-id="2a6eb-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="2a6eb-109">Функция, возвращающая операции.</span><span class="sxs-lookup"><span data-stu-id="2a6eb-109">A function which returns operations.</span></span>



## <a name="output--tu--unit--is-adj--ctl"></a><span data-ttu-id="2a6eb-110">Выходные данные: ('T, ' U) => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="2a6eb-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="2a6eb-111">Новая операция `op` , которая `op(t, u)` эквивалентна `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="2a6eb-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="2a6eb-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="2a6eb-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2a6eb-113">Е</span><span class="sxs-lookup"><span data-stu-id="2a6eb-113">'T</span></span>

<span data-ttu-id="2a6eb-114">Тип первого аргумента каррированных функции.</span><span class="sxs-lookup"><span data-stu-id="2a6eb-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="2a6eb-115">' U</span><span class="sxs-lookup"><span data-stu-id="2a6eb-115">'U</span></span>

<span data-ttu-id="2a6eb-116">Тип второго аргумента каррированных функции.</span><span class="sxs-lookup"><span data-stu-id="2a6eb-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="2a6eb-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="2a6eb-117">See Also</span></span>

- [<span data-ttu-id="2a6eb-118">Microsoft. тактов. Canon. Ункурриедоп</span><span class="sxs-lookup"><span data-stu-id="2a6eb-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)