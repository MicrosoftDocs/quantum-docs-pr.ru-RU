---
uid: Microsoft.Quantum.Canon.UncurriedOpC
title: Функция Ункурриедопк
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpC
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `C` indicates that the operations are controllable.
ms.openlocfilehash: 05df99dce8b167f32078ce256748647ceb94d0fe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851988"
---
# <a name="uncurriedopc-function"></a><span data-ttu-id="b3a3f-102">Функция Ункурриедопк</span><span class="sxs-lookup"><span data-stu-id="b3a3f-102">UncurriedOpC function</span></span>

<span data-ttu-id="b3a3f-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b3a3f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b3a3f-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b3a3f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b3a3f-105">При наличии функции, возвращающей операции, возвращает новую операцию, которая принимает оба входа как кортеж.</span><span class="sxs-lookup"><span data-stu-id="b3a3f-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="b3a3f-106">Модификатор `C` указывает, что операции являются управляемыми.</span><span class="sxs-lookup"><span data-stu-id="b3a3f-106">The modifier `C` indicates that the operations are controllable.</span></span>

```qsharp
function UncurriedOpC<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl))) : (('T, 'U) => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="b3a3f-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b3a3f-107">Input</span></span>

### <a name="curriedop--t---u--unit--is-ctl"></a><span data-ttu-id="b3a3f-108">Курриедоп: не> "U = [единица](xref:microsoft.quantum.lang-ref.unit) > является CTL</span><span class="sxs-lookup"><span data-stu-id="b3a3f-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="b3a3f-109">Функция, возвращающая операции.</span><span class="sxs-lookup"><span data-stu-id="b3a3f-109">A function which returns operations.</span></span>



## <a name="output--tu--unit--is-ctl"></a><span data-ttu-id="b3a3f-110">Выходные данные: ('T, ' U) => [единица](xref:microsoft.quantum.lang-ref.unit)  является CTL</span><span class="sxs-lookup"><span data-stu-id="b3a3f-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="b3a3f-111">Новая операция `op` , которая `op(t, u)` эквивалентна `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="b3a3f-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="b3a3f-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="b3a3f-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b3a3f-113">Е</span><span class="sxs-lookup"><span data-stu-id="b3a3f-113">'T</span></span>

<span data-ttu-id="b3a3f-114">Тип первого аргумента каррированных функции.</span><span class="sxs-lookup"><span data-stu-id="b3a3f-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="b3a3f-115">' U</span><span class="sxs-lookup"><span data-stu-id="b3a3f-115">'U</span></span>

<span data-ttu-id="b3a3f-116">Тип второго аргумента каррированных функции.</span><span class="sxs-lookup"><span data-stu-id="b3a3f-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3a3f-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="b3a3f-117">See Also</span></span>

- [<span data-ttu-id="b3a3f-118">Microsoft. тактов. Canon. Ункурриедоп</span><span class="sxs-lookup"><span data-stu-id="b3a3f-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)