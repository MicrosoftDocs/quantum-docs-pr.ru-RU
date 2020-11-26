---
uid: Microsoft.Quantum.Canon.UncurriedOpC
title: Функция Ункурриедопк
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpC
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `C` indicates that the operations are controllable.
ms.openlocfilehash: 35be5425fcd76eae9e0a6fde6a689a5db00da52f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204595"
---
# <a name="uncurriedopc-function"></a><span data-ttu-id="8e29c-102">Функция Ункурриедопк</span><span class="sxs-lookup"><span data-stu-id="8e29c-102">UncurriedOpC function</span></span>

<span data-ttu-id="8e29c-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8e29c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8e29c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8e29c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8e29c-105">При наличии функции, возвращающей операции, возвращает новую операцию, которая принимает оба входа как кортеж.</span><span class="sxs-lookup"><span data-stu-id="8e29c-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="8e29c-106">Модификатор `C` указывает, что операции являются управляемыми.</span><span class="sxs-lookup"><span data-stu-id="8e29c-106">The modifier `C` indicates that the operations are controllable.</span></span>

```qsharp
function UncurriedOpC<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl))) : (('T, 'U) => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="8e29c-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8e29c-107">Input</span></span>

### <a name="curriedop--t---u--unit--is-ctl"></a><span data-ttu-id="8e29c-108">Курриедоп: не> "U = [единица](xref:microsoft.quantum.lang-ref.unit) > является CTL</span><span class="sxs-lookup"><span data-stu-id="8e29c-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="8e29c-109">Функция, возвращающая операции.</span><span class="sxs-lookup"><span data-stu-id="8e29c-109">A function which returns operations.</span></span>



## <a name="output--tu--unit--is-ctl"></a><span data-ttu-id="8e29c-110">Выходные данные: ('T, ' U) => [единица](xref:microsoft.quantum.lang-ref.unit)  является CTL</span><span class="sxs-lookup"><span data-stu-id="8e29c-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="8e29c-111">Новая операция `op` , которая `op(t, u)` эквивалентна `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="8e29c-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8e29c-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="8e29c-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8e29c-113">Е</span><span class="sxs-lookup"><span data-stu-id="8e29c-113">'T</span></span>

<span data-ttu-id="8e29c-114">Тип первого аргумента каррированных функции.</span><span class="sxs-lookup"><span data-stu-id="8e29c-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="8e29c-115">' U</span><span class="sxs-lookup"><span data-stu-id="8e29c-115">'U</span></span>

<span data-ttu-id="8e29c-116">Тип второго аргумента каррированных функции.</span><span class="sxs-lookup"><span data-stu-id="8e29c-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e29c-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="8e29c-117">See Also</span></span>

- [<span data-ttu-id="8e29c-118">Microsoft. тактов. Canon. Ункурриедоп</span><span class="sxs-lookup"><span data-stu-id="8e29c-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)