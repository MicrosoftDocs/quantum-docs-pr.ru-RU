---
uid: Microsoft.Quantum.Canon.BoundA
title: Функция с ограничением
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `A` indicates that all operations in the array are adjointable.
ms.openlocfilehash: 3132bf198e98dd1a2b433f36b000060e7e721865
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216954"
---
# <a name="bounda-function"></a><span data-ttu-id="83493-102">Функция с ограничением</span><span class="sxs-lookup"><span data-stu-id="83493-102">BoundA function</span></span>

<span data-ttu-id="83493-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="83493-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="83493-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="83493-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="83493-105">При наличии массива операций, исдействующих один вход, создает новую операцию, которая выполняет каждую заданную операцию последовательно.</span><span class="sxs-lookup"><span data-stu-id="83493-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="83493-106">Модификатор `A` указывает, что все операции в массиве являются аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="83493-106">The modifier `A` indicates that all operations in the array are adjointable.</span></span>

```qsharp
function BoundA<'T> (operations : ('T => Unit is Adj)[]) : ('T => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="83493-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="83493-107">Input</span></span>

### <a name="operations--t--unit--is-adj"></a><span data-ttu-id="83493-108">операции: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  является суммой []</span><span class="sxs-lookup"><span data-stu-id="83493-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj[]</span></span>

<span data-ttu-id="83493-109">Последовательность операций, выполняемых с заданным входом.</span><span class="sxs-lookup"><span data-stu-id="83493-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit--is-adj"></a><span data-ttu-id="83493-110">Выходные данные: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  является прогода</span><span class="sxs-lookup"><span data-stu-id="83493-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="83493-111">Новая операция, которая выполняет каждую заданную операцию последовательно по входным данным.</span><span class="sxs-lookup"><span data-stu-id="83493-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="83493-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="83493-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="83493-113">Е</span><span class="sxs-lookup"><span data-stu-id="83493-113">'T</span></span>

<span data-ttu-id="83493-114">Целевой объект, на котором выполняется каждая операция в массиве.</span><span class="sxs-lookup"><span data-stu-id="83493-114">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="83493-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="83493-115">See Also</span></span>

- [<span data-ttu-id="83493-116">Microsoft. тактов. Canon. Bounds</span><span class="sxs-lookup"><span data-stu-id="83493-116">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)