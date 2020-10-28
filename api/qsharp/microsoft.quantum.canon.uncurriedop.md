---
uid: Microsoft.Quantum.Canon.UncurriedOp
title: Функция Ункурриедоп
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOp
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple.
ms.openlocfilehash: 359c0b2a9dd56445fb39fadc6580809dd9fbf628
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715243"
---
# <a name="uncurriedop-function"></a><span data-ttu-id="12fb0-102">Функция Ункурриедоп</span><span class="sxs-lookup"><span data-stu-id="12fb0-102">UncurriedOp function</span></span>

<span data-ttu-id="12fb0-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="12fb0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="12fb0-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="12fb0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="12fb0-105">При наличии функции, возвращающей операции, возвращает новую операцию, которая принимает оба входа как кортеж.</span><span class="sxs-lookup"><span data-stu-id="12fb0-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>

```qsharp
function UncurriedOp<'T, 'U> (curriedOp : ('T -> ('U => Unit))) : (('T, 'U) => Unit)
```


## <a name="input"></a><span data-ttu-id="12fb0-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="12fb0-106">Input</span></span>

### <a name="curriedop--t---u--unit"></a><span data-ttu-id="12fb0-107">Курриедоп: не> "U = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="12fb0-107">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="12fb0-108">Функция, возвращающая операции.</span><span class="sxs-lookup"><span data-stu-id="12fb0-108">A function which returns operations.</span></span>



## <a name="output--tu--unit"></a><span data-ttu-id="12fb0-109">Выходные данные: ('T, ' U) = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="12fb0-109">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="12fb0-110">Новая операция `op` , которая `op(t, u)` эквивалентна `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="12fb0-110">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="12fb0-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="12fb0-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="12fb0-112">Е</span><span class="sxs-lookup"><span data-stu-id="12fb0-112">'T</span></span>

<span data-ttu-id="12fb0-113">Тип первого входного параметра для перекаррированных операции.</span><span class="sxs-lookup"><span data-stu-id="12fb0-113">The type of the first input to a curried operation.</span></span>
### <a name="u"></a><span data-ttu-id="12fb0-114">' U</span><span class="sxs-lookup"><span data-stu-id="12fb0-114">'U</span></span>

<span data-ttu-id="12fb0-115">Тип второго входного параметра для перекаррированных операции.</span><span class="sxs-lookup"><span data-stu-id="12fb0-115">The type of the second input to a curried operation.</span></span>

## <a name="see-also"></a><span data-ttu-id="12fb0-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="12fb0-116">See Also</span></span>

- [<span data-ttu-id="12fb0-117">Microsoft. тактов. Canon. Ункурриедопк</span><span class="sxs-lookup"><span data-stu-id="12fb0-117">Microsoft.Quantum.Canon.UncurriedOpC</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpC)
- [<span data-ttu-id="12fb0-118">Microsoft. тактов. Canon. Ункурриедопа</span><span class="sxs-lookup"><span data-stu-id="12fb0-118">Microsoft.Quantum.Canon.UncurriedOpA</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpA)
- [<span data-ttu-id="12fb0-119">Microsoft. тактов. Canon. Ункурриедопка</span><span class="sxs-lookup"><span data-stu-id="12fb0-119">Microsoft.Quantum.Canon.UncurriedOpCA</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpCA)