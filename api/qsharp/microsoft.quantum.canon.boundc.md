---
uid: Microsoft.Quantum.Canon.BoundC
title: Функция Баундк
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundC
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `C` indicates that all operations in the array are controllable.
ms.openlocfilehash: 6b640c0dab14778336f42098e699e7e68cc726df
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841050"
---
# <a name="boundc-function"></a><span data-ttu-id="5f8a5-102">Функция Баундк</span><span class="sxs-lookup"><span data-stu-id="5f8a5-102">BoundC function</span></span>

<span data-ttu-id="5f8a5-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5f8a5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5f8a5-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5f8a5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5f8a5-105">При наличии массива операций, исдействующих один вход, создает новую операцию, которая выполняет каждую заданную операцию последовательно.</span><span class="sxs-lookup"><span data-stu-id="5f8a5-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="5f8a5-106">Модификатор `C` указывает, что все операции в массиве являются управляемыми.</span><span class="sxs-lookup"><span data-stu-id="5f8a5-106">The modifier `C` indicates that all operations in the array are controllable.</span></span>

```qsharp
function BoundC<'T> (operations : ('T => Unit is Ctl)[]) : ('T => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="5f8a5-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5f8a5-107">Input</span></span>

### <a name="operations--t--unit--is-ctl"></a><span data-ttu-id="5f8a5-108">операции: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — CTL []</span><span class="sxs-lookup"><span data-stu-id="5f8a5-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl[]</span></span>

<span data-ttu-id="5f8a5-109">Последовательность операций, выполняемых с заданным входом.</span><span class="sxs-lookup"><span data-stu-id="5f8a5-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit--is-ctl"></a><span data-ttu-id="5f8a5-110">Выходные данные: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  является CTL</span><span class="sxs-lookup"><span data-stu-id="5f8a5-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="5f8a5-111">Новая операция, которая выполняет каждую заданную операцию последовательно по входным данным.</span><span class="sxs-lookup"><span data-stu-id="5f8a5-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5f8a5-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="5f8a5-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5f8a5-113">Е</span><span class="sxs-lookup"><span data-stu-id="5f8a5-113">'T</span></span>

<span data-ttu-id="5f8a5-114">Целевой объект, на котором выполняется каждая операция в массиве.</span><span class="sxs-lookup"><span data-stu-id="5f8a5-114">The target on which each of the operations in the array act.</span></span>

## <a name="example"></a><span data-ttu-id="5f8a5-115">Пример</span><span class="sxs-lookup"><span data-stu-id="5f8a5-115">Example</span></span>

<span data-ttu-id="5f8a5-116">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="5f8a5-116">The following are equivalent:</span></span>

```qsharp
let bound = BoundC([U, V]);
bound(x);
```

<span data-ttu-id="5f8a5-117">и</span><span class="sxs-lookup"><span data-stu-id="5f8a5-117">and</span></span>

```qsharp
U(x); V(x);
```

## <a name="see-also"></a><span data-ttu-id="5f8a5-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="5f8a5-118">See Also</span></span>

- [<span data-ttu-id="5f8a5-119">Microsoft. тактов. Canon. Bounds</span><span class="sxs-lookup"><span data-stu-id="5f8a5-119">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)