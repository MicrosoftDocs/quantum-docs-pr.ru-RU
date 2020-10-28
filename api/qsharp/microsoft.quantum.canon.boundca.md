---
uid: Microsoft.Quantum.Canon.BoundCA
title: Функция Баундка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundCA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `CA` indicates that all operations in the array are adjointable and controllable.
ms.openlocfilehash: d96d33781def10940479ba2eafdcc6711a0c05a5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716630"
---
# <a name="boundca-function"></a><span data-ttu-id="e8b7e-102">Функция Баундка</span><span class="sxs-lookup"><span data-stu-id="e8b7e-102">BoundCA function</span></span>

<span data-ttu-id="e8b7e-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e8b7e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e8b7e-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e8b7e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e8b7e-105">При наличии массива операций, исдействующих один вход, создает новую операцию, которая выполняет каждую заданную операцию последовательно.</span><span class="sxs-lookup"><span data-stu-id="e8b7e-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="e8b7e-106">Модификатор `CA` указывает, что все операции в массиве являются аджоинтабле и управляемыми.</span><span class="sxs-lookup"><span data-stu-id="e8b7e-106">The modifier `CA` indicates that all operations in the array are adjointable and controllable.</span></span>

```qsharp
function BoundCA<'T> (operations : ('T => Unit is Adj + Ctl)[]) : ('T => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="e8b7e-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e8b7e-107">Input</span></span>

### <a name="operations--t--unit-adj--ctl"></a><span data-ttu-id="e8b7e-108">операции: 'T => [модульные](xref:microsoft.quantum.lang-ref.unit) года + CTL []</span><span class="sxs-lookup"><span data-stu-id="e8b7e-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl[]</span></span>

<span data-ttu-id="e8b7e-109">Последовательность операций, выполняемых с заданным входом.</span><span class="sxs-lookup"><span data-stu-id="e8b7e-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit-adj--ctl"></a><span data-ttu-id="e8b7e-110">Выходные данные: 'T => [единицы](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="e8b7e-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="e8b7e-111">Новая операция, которая выполняет каждую заданную операцию последовательно по входным данным.</span><span class="sxs-lookup"><span data-stu-id="e8b7e-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e8b7e-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="e8b7e-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e8b7e-113">Е</span><span class="sxs-lookup"><span data-stu-id="e8b7e-113">'T</span></span>

<span data-ttu-id="e8b7e-114">Целевой объект, на котором выполняется каждая операция в массиве.</span><span class="sxs-lookup"><span data-stu-id="e8b7e-114">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8b7e-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="e8b7e-115">See Also</span></span>

- [<span data-ttu-id="e8b7e-116">Microsoft. тактов. Canon. Bounds</span><span class="sxs-lookup"><span data-stu-id="e8b7e-116">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)