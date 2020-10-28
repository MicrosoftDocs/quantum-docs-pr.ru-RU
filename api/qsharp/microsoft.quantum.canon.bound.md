---
uid: Microsoft.Quantum.Canon.Bound
title: Связанная функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Bound
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.
ms.openlocfilehash: 34ca2b79d0ee09bd3b5b5b3f0c0b20420d5b3882
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716700"
---
# <a name="bound-function"></a><span data-ttu-id="5d295-102">Связанная функция</span><span class="sxs-lookup"><span data-stu-id="5d295-102">Bound function</span></span>

<span data-ttu-id="5d295-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5d295-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5d295-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5d295-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5d295-105">При наличии массива операций, исдействующих один вход, создает новую операцию, которая выполняет каждую заданную операцию последовательно.</span><span class="sxs-lookup"><span data-stu-id="5d295-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>

```qsharp
function Bound<'T> (operations : ('T => Unit)[]) : ('T => Unit)
```


## <a name="input"></a><span data-ttu-id="5d295-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5d295-106">Input</span></span>

### <a name="operations--t--unit-"></a><span data-ttu-id="5d295-107">операции: t => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="5d295-107">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span></span>

<span data-ttu-id="5d295-108">Последовательность операций, выполняемых с заданным входом.</span><span class="sxs-lookup"><span data-stu-id="5d295-108">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit"></a><span data-ttu-id="5d295-109">Выходные данные: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5d295-109">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="5d295-110">Новая операция, которая выполняет каждую заданную операцию последовательно по входным данным.</span><span class="sxs-lookup"><span data-stu-id="5d295-110">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5d295-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="5d295-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5d295-112">Е</span><span class="sxs-lookup"><span data-stu-id="5d295-112">'T</span></span>

<span data-ttu-id="5d295-113">Целевой объект, на котором выполняется каждая операция в массиве.</span><span class="sxs-lookup"><span data-stu-id="5d295-113">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="5d295-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="5d295-114">See Also</span></span>

- [<span data-ttu-id="5d295-115">Microsoft. тактов. Canon. Баундк</span><span class="sxs-lookup"><span data-stu-id="5d295-115">Microsoft.Quantum.Canon.BoundC</span></span>](xref:Microsoft.Quantum.Canon.BoundC)
- [<span data-ttu-id="5d295-116">Microsoft. тактов. Canon. Bounds</span><span class="sxs-lookup"><span data-stu-id="5d295-116">Microsoft.Quantum.Canon.BoundA</span></span>](xref:Microsoft.Quantum.Canon.BoundA)
- [<span data-ttu-id="5d295-117">Microsoft. тактов. Canon. Баундка</span><span class="sxs-lookup"><span data-stu-id="5d295-117">Microsoft.Quantum.Canon.BoundCA</span></span>](xref:Microsoft.Quantum.Canon.BoundCA)