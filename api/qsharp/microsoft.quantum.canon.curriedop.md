---
uid: Microsoft.Quantum.Canon.CurriedOp
title: Функция Курриедоп
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CurriedOp
qsharp.summary: >-
  Returns a curried version of an operation on two inputs.

  That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.
ms.openlocfilehash: 6c1917d6f1ee69cb29fed1ab173106af1e206533
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216631"
---
# <a name="curriedop-function"></a><span data-ttu-id="4426d-102">Функция Курриедоп</span><span class="sxs-lookup"><span data-stu-id="4426d-102">CurriedOp function</span></span>

<span data-ttu-id="4426d-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4426d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4426d-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4426d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4426d-105">Возвращает перекаррированных версию операции с двумя входными данными.</span><span class="sxs-lookup"><span data-stu-id="4426d-105">Returns a curried version of an operation on two inputs.</span></span>

<span data-ttu-id="4426d-106">Это значит, что при выполнении операции с двумя входными данными эта функция применяет карри исоморфисм $f (x, y) \екуив f (x) (y) $ для возврата операции одного входа, которая возвращает операцию одного входа.</span><span class="sxs-lookup"><span data-stu-id="4426d-106">That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.</span></span>

```qsharp
function CurriedOp<'T, 'U> (op : (('T, 'U) => Unit)) : ('T -> ('U => Unit))
```


## <a name="input"></a><span data-ttu-id="4426d-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4426d-107">Input</span></span>

### <a name="op--tu--unit"></a><span data-ttu-id="4426d-108">Op: (t, ' U) = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="4426d-108">op : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="4426d-109">Операция, входные данные которой являются парой.</span><span class="sxs-lookup"><span data-stu-id="4426d-109">An operation whose input is a pair.</span></span>



## <a name="output--t---u--unit"></a><span data-ttu-id="4426d-110">Выходные данные: не> "U = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="4426d-110">Output : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="4426d-111">Операция, которая принимает первый элемент пары и возвращает операцию, которая принимает в качестве входных данных второй элемент входных данных исходной операции.</span><span class="sxs-lookup"><span data-stu-id="4426d-111">An operation which accepts the first element of a pair and returns an operation which accepts as its input the second element of the original operation's input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="4426d-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="4426d-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4426d-113">Е</span><span class="sxs-lookup"><span data-stu-id="4426d-113">'T</span></span>

<span data-ttu-id="4426d-114">Тип первого компонента функции, определенной в парах.</span><span class="sxs-lookup"><span data-stu-id="4426d-114">The type of the first component of a function defined on pairs.</span></span>
### <a name="u"></a><span data-ttu-id="4426d-115">' U</span><span class="sxs-lookup"><span data-stu-id="4426d-115">'U</span></span>

<span data-ttu-id="4426d-116">Тип второго компонента функции, определенной в парах.</span><span class="sxs-lookup"><span data-stu-id="4426d-116">The type of the second component of a function defined on pairs.</span></span>

## <a name="remarks"></a><span data-ttu-id="4426d-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4426d-117">Remarks</span></span>

<span data-ttu-id="4426d-118">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="4426d-118">The following are equivalent:</span></span>

```qsharp
op(x, y);

let curried = CurriedOp(op);
let partial = curried(x);
partial(y);
```