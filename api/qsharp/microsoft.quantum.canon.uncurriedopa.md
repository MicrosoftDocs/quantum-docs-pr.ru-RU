---
uid: Microsoft.Quantum.Canon.UncurriedOpA
title: Функция Ункурриедопа
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `A` indicates that the operations are adjointable.
ms.openlocfilehash: feb5da771ee6cb6a750fa76f9ffd8f5a3e0b5734
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840054"
---
# <a name="uncurriedopa-function"></a><span data-ttu-id="70bf1-102">Функция Ункурриедопа</span><span class="sxs-lookup"><span data-stu-id="70bf1-102">UncurriedOpA function</span></span>

<span data-ttu-id="70bf1-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="70bf1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="70bf1-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="70bf1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="70bf1-105">При наличии функции, возвращающей операции, возвращает новую операцию, которая принимает оба входа как кортеж.</span><span class="sxs-lookup"><span data-stu-id="70bf1-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="70bf1-106">Модификатор `A` указывает, что операции являются аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="70bf1-106">The modifier `A` indicates that the operations are adjointable.</span></span>

```qsharp
function UncurriedOpA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Adj))) : (('T, 'U) => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="70bf1-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="70bf1-107">Input</span></span>

### <a name="curriedop--t---u--unit--is-adj"></a><span data-ttu-id="70bf1-108">Курриедоп: не> "U = [единица](xref:microsoft.quantum.lang-ref.unit) > является просуммой</span><span class="sxs-lookup"><span data-stu-id="70bf1-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="70bf1-109">Функция, возвращающая операции.</span><span class="sxs-lookup"><span data-stu-id="70bf1-109">A function which returns operations.</span></span>



## <a name="output--tu--unit--is-adj"></a><span data-ttu-id="70bf1-110">Выходные данные: ('T, ' U) => [единица](xref:microsoft.quantum.lang-ref.unit)  в сумме</span><span class="sxs-lookup"><span data-stu-id="70bf1-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="70bf1-111">Новая операция `op` , которая `op(t, u)` эквивалентна `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="70bf1-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="70bf1-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="70bf1-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="70bf1-113">Е</span><span class="sxs-lookup"><span data-stu-id="70bf1-113">'T</span></span>

<span data-ttu-id="70bf1-114">Тип первого аргумента каррированных функции.</span><span class="sxs-lookup"><span data-stu-id="70bf1-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="70bf1-115">' U</span><span class="sxs-lookup"><span data-stu-id="70bf1-115">'U</span></span>

<span data-ttu-id="70bf1-116">Тип второго аргумента каррированных функции.</span><span class="sxs-lookup"><span data-stu-id="70bf1-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="70bf1-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="70bf1-117">See Also</span></span>

- [<span data-ttu-id="70bf1-118">Microsoft. тактов. Canon. Ункурриедоп</span><span class="sxs-lookup"><span data-stu-id="70bf1-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)