---
uid: Microsoft.Quantum.Canon.BoundCA
title: Функция Баундка
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundCA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `CA` indicates that all operations in the array are adjointable and controllable.
ms.openlocfilehash: 391183829a3cc8b7aa8051767dcfc6bec9638223
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844528"
---
# <a name="boundca-function"></a><span data-ttu-id="7aaf6-102">Функция Баундка</span><span class="sxs-lookup"><span data-stu-id="7aaf6-102">BoundCA function</span></span>

<span data-ttu-id="7aaf6-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7aaf6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7aaf6-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7aaf6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7aaf6-105">При наличии массива операций, исдействующих один вход, создает новую операцию, которая выполняет каждую заданную операцию последовательно.</span><span class="sxs-lookup"><span data-stu-id="7aaf6-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="7aaf6-106">Модификатор `CA` указывает, что все операции в массиве являются аджоинтабле и управляемыми.</span><span class="sxs-lookup"><span data-stu-id="7aaf6-106">The modifier `CA` indicates that all operations in the array are adjointable and controllable.</span></span>

```qsharp
function BoundCA<'T> (operations : ('T => Unit is Adj + Ctl)[]) : ('T => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="7aaf6-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7aaf6-107">Input</span></span>

### <a name="operations--t--unit--is-adj--ctl"></a><span data-ttu-id="7aaf6-108">Operations: t => [Unit](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL []"</span><span class="sxs-lookup"><span data-stu-id="7aaf6-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl[]</span></span>

<span data-ttu-id="7aaf6-109">Последовательность операций, выполняемых с заданным входом.</span><span class="sxs-lookup"><span data-stu-id="7aaf6-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit--is-adj--ctl"></a><span data-ttu-id="7aaf6-110">Выходные данные: 'T => [единицы измерения](xref:microsoft.quantum.lang-ref.unit)  и CTL</span><span class="sxs-lookup"><span data-stu-id="7aaf6-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="7aaf6-111">Новая операция, которая выполняет каждую заданную операцию последовательно по входным данным.</span><span class="sxs-lookup"><span data-stu-id="7aaf6-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7aaf6-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="7aaf6-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7aaf6-113">Е</span><span class="sxs-lookup"><span data-stu-id="7aaf6-113">'T</span></span>

<span data-ttu-id="7aaf6-114">Целевой объект, на котором выполняется каждая операция в массиве.</span><span class="sxs-lookup"><span data-stu-id="7aaf6-114">The target on which each of the operations in the array act.</span></span>

## <a name="example"></a><span data-ttu-id="7aaf6-115">Пример</span><span class="sxs-lookup"><span data-stu-id="7aaf6-115">Example</span></span>

<span data-ttu-id="7aaf6-116">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="7aaf6-116">The following are equivalent:</span></span>

```qsharp
let bound = BoundCA([U, V]);
bound(x);
```

<span data-ttu-id="7aaf6-117">и</span><span class="sxs-lookup"><span data-stu-id="7aaf6-117">and</span></span>

```qsharp
U(x); V(x);
```

## <a name="see-also"></a><span data-ttu-id="7aaf6-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="7aaf6-118">See Also</span></span>

- [<span data-ttu-id="7aaf6-119">Microsoft. тактов. Canon. Bounds</span><span class="sxs-lookup"><span data-stu-id="7aaf6-119">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)