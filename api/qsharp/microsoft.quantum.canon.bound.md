---
uid: Microsoft.Quantum.Canon.Bound
title: Связанная функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Bound
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.
ms.openlocfilehash: c12ce37054ddde1b98778888e90916c6e4725814
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207604"
---
# <a name="bound-function"></a><span data-ttu-id="6c2cb-102">Связанная функция</span><span class="sxs-lookup"><span data-stu-id="6c2cb-102">Bound function</span></span>

<span data-ttu-id="6c2cb-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6c2cb-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6c2cb-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6c2cb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6c2cb-105">При наличии массива операций, исдействующих один вход, создает новую операцию, которая выполняет каждую заданную операцию последовательно.</span><span class="sxs-lookup"><span data-stu-id="6c2cb-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>

```qsharp
function Bound<'T> (operations : ('T => Unit)[]) : ('T => Unit)
```


## <a name="input"></a><span data-ttu-id="6c2cb-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6c2cb-106">Input</span></span>

### <a name="operations--t--unit-"></a><span data-ttu-id="6c2cb-107">операции: t => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="6c2cb-107">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span></span>

<span data-ttu-id="6c2cb-108">Последовательность операций, выполняемых с заданным входом.</span><span class="sxs-lookup"><span data-stu-id="6c2cb-108">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit"></a><span data-ttu-id="6c2cb-109">Выходные данные: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6c2cb-109">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="6c2cb-110">Новая операция, которая выполняет каждую заданную операцию последовательно по входным данным.</span><span class="sxs-lookup"><span data-stu-id="6c2cb-110">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="6c2cb-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="6c2cb-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6c2cb-112">Е</span><span class="sxs-lookup"><span data-stu-id="6c2cb-112">'T</span></span>

<span data-ttu-id="6c2cb-113">Целевой объект, на котором выполняется каждая операция в массиве.</span><span class="sxs-lookup"><span data-stu-id="6c2cb-113">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c2cb-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="6c2cb-114">See Also</span></span>

- [<span data-ttu-id="6c2cb-115">Microsoft. тактов. Canon. Баундк</span><span class="sxs-lookup"><span data-stu-id="6c2cb-115">Microsoft.Quantum.Canon.BoundC</span></span>](xref:Microsoft.Quantum.Canon.BoundC)
- [<span data-ttu-id="6c2cb-116">Microsoft. тактов. Canon. Bounds</span><span class="sxs-lookup"><span data-stu-id="6c2cb-116">Microsoft.Quantum.Canon.BoundA</span></span>](xref:Microsoft.Quantum.Canon.BoundA)
- [<span data-ttu-id="6c2cb-117">Microsoft. тактов. Canon. Баундка</span><span class="sxs-lookup"><span data-stu-id="6c2cb-117">Microsoft.Quantum.Canon.BoundCA</span></span>](xref:Microsoft.Quantum.Canon.BoundCA)