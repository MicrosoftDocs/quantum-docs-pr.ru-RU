---
uid: Microsoft.Quantum.Canon.Bound
title: Связанная функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Bound
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.
ms.openlocfilehash: 041f654c14f6e926d60038fee698b2b829fab8b3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841052"
---
# <a name="bound-function"></a><span data-ttu-id="f32b6-102">Связанная функция</span><span class="sxs-lookup"><span data-stu-id="f32b6-102">Bound function</span></span>

<span data-ttu-id="f32b6-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f32b6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f32b6-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f32b6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f32b6-105">При наличии массива операций, исдействующих один вход, создает новую операцию, которая выполняет каждую заданную операцию последовательно.</span><span class="sxs-lookup"><span data-stu-id="f32b6-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>

```qsharp
function Bound<'T> (operations : ('T => Unit)[]) : ('T => Unit)
```


## <a name="input"></a><span data-ttu-id="f32b6-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f32b6-106">Input</span></span>

### <a name="operations--t--unit-"></a><span data-ttu-id="f32b6-107">операции: t => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="f32b6-107">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span></span>

<span data-ttu-id="f32b6-108">Последовательность операций, выполняемых с заданным входом.</span><span class="sxs-lookup"><span data-stu-id="f32b6-108">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit"></a><span data-ttu-id="f32b6-109">Выходные данные: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f32b6-109">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="f32b6-110">Новая операция, которая выполняет каждую заданную операцию последовательно по входным данным.</span><span class="sxs-lookup"><span data-stu-id="f32b6-110">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f32b6-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="f32b6-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f32b6-112">Е</span><span class="sxs-lookup"><span data-stu-id="f32b6-112">'T</span></span>

<span data-ttu-id="f32b6-113">Целевой объект, на котором выполняется каждая операция в массиве.</span><span class="sxs-lookup"><span data-stu-id="f32b6-113">The target on which each of the operations in the array act.</span></span>

## <a name="example"></a><span data-ttu-id="f32b6-114">Пример</span><span class="sxs-lookup"><span data-stu-id="f32b6-114">Example</span></span>

<span data-ttu-id="f32b6-115">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="f32b6-115">The following are equivalent:</span></span>

```qsharp
let bound = Bound([U, V]);
bound(x);
```

<span data-ttu-id="f32b6-116">и</span><span class="sxs-lookup"><span data-stu-id="f32b6-116">and</span></span>

```qsharp
U(x); V(x);
```

## <a name="see-also"></a><span data-ttu-id="f32b6-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="f32b6-117">See Also</span></span>

- [<span data-ttu-id="f32b6-118">Microsoft. тактов. Canon. Баундк</span><span class="sxs-lookup"><span data-stu-id="f32b6-118">Microsoft.Quantum.Canon.BoundC</span></span>](xref:Microsoft.Quantum.Canon.BoundC)
- [<span data-ttu-id="f32b6-119">Microsoft. тактов. Canon. Bounds</span><span class="sxs-lookup"><span data-stu-id="f32b6-119">Microsoft.Quantum.Canon.BoundA</span></span>](xref:Microsoft.Quantum.Canon.BoundA)
- [<span data-ttu-id="f32b6-120">Microsoft. тактов. Canon. Баундка</span><span class="sxs-lookup"><span data-stu-id="f32b6-120">Microsoft.Quantum.Canon.BoundCA</span></span>](xref:Microsoft.Quantum.Canon.BoundCA)