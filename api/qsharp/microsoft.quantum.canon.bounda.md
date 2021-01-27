---
uid: Microsoft.Quantum.Canon.BoundA
title: Функция с ограничением
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `A` indicates that all operations in the array are adjointable.
ms.openlocfilehash: 3d0a5ba5d3d9c76289ed29e59a9c226358b83797
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844547"
---
# <a name="bounda-function"></a><span data-ttu-id="bb258-102">Функция с ограничением</span><span class="sxs-lookup"><span data-stu-id="bb258-102">BoundA function</span></span>

<span data-ttu-id="bb258-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="bb258-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="bb258-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bb258-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bb258-105">При наличии массива операций, исдействующих один вход, создает новую операцию, которая выполняет каждую заданную операцию последовательно.</span><span class="sxs-lookup"><span data-stu-id="bb258-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="bb258-106">Модификатор `A` указывает, что все операции в массиве являются аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="bb258-106">The modifier `A` indicates that all operations in the array are adjointable.</span></span>

```qsharp
function BoundA<'T> (operations : ('T => Unit is Adj)[]) : ('T => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="bb258-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bb258-107">Input</span></span>

### <a name="operations--t--unit--is-adj"></a><span data-ttu-id="bb258-108">операции: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  является суммой []</span><span class="sxs-lookup"><span data-stu-id="bb258-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj[]</span></span>

<span data-ttu-id="bb258-109">Последовательность операций, выполняемых с заданным входом.</span><span class="sxs-lookup"><span data-stu-id="bb258-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit--is-adj"></a><span data-ttu-id="bb258-110">Выходные данные: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  является прогода</span><span class="sxs-lookup"><span data-stu-id="bb258-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="bb258-111">Новая операция, которая выполняет каждую заданную операцию последовательно по входным данным.</span><span class="sxs-lookup"><span data-stu-id="bb258-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="bb258-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="bb258-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="bb258-113">Е</span><span class="sxs-lookup"><span data-stu-id="bb258-113">'T</span></span>

<span data-ttu-id="bb258-114">Целевой объект, на котором выполняется каждая операция в массиве.</span><span class="sxs-lookup"><span data-stu-id="bb258-114">The target on which each of the operations in the array act.</span></span>

## <a name="example"></a><span data-ttu-id="bb258-115">Пример</span><span class="sxs-lookup"><span data-stu-id="bb258-115">Example</span></span>

<span data-ttu-id="bb258-116">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="bb258-116">The following are equivalent:</span></span>

```qsharp
let bound = BoundA([U, V]);
bound(x);
```

<span data-ttu-id="bb258-117">и</span><span class="sxs-lookup"><span data-stu-id="bb258-117">and</span></span>

```qsharp
U(x); V(x);
```

## <a name="see-also"></a><span data-ttu-id="bb258-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="bb258-118">See Also</span></span>

- [<span data-ttu-id="bb258-119">Microsoft. тактов. Canon. Bounds</span><span class="sxs-lookup"><span data-stu-id="bb258-119">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)