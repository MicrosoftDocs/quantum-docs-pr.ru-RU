---
uid: Microsoft.Quantum.Canon.BoundA
title: Функция с ограничением
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `A` indicates that all operations in the array are adjointable.
ms.openlocfilehash: 40c112d0572dc4eebfc284c9ef29f43706e20c64
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716686"
---
# <a name="bounda-function"></a><span data-ttu-id="8ce50-102">Функция с ограничением</span><span class="sxs-lookup"><span data-stu-id="8ce50-102">BoundA function</span></span>

<span data-ttu-id="8ce50-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8ce50-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8ce50-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8ce50-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8ce50-105">При наличии массива операций, исдействующих один вход, создает новую операцию, которая выполняет каждую заданную операцию последовательно.</span><span class="sxs-lookup"><span data-stu-id="8ce50-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="8ce50-106">Модификатор `A` указывает, что все операции в массиве являются аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="8ce50-106">The modifier `A` indicates that all operations in the array are adjointable.</span></span>

```qsharp
function BoundA<'T> (operations : ('T => Unit is Adj)[]) : ('T => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="8ce50-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8ce50-107">Input</span></span>

### <a name="operations--t--unit-adj"></a><span data-ttu-id="8ce50-108">операции: 'T => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="8ce50-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj[]</span></span>

<span data-ttu-id="8ce50-109">Последовательность операций, выполняемых с заданным входом.</span><span class="sxs-lookup"><span data-stu-id="8ce50-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit-adj"></a><span data-ttu-id="8ce50-110">Выходные данные: 'T => [единица](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="8ce50-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="8ce50-111">Новая операция, которая выполняет каждую заданную операцию последовательно по входным данным.</span><span class="sxs-lookup"><span data-stu-id="8ce50-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8ce50-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="8ce50-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8ce50-113">Е</span><span class="sxs-lookup"><span data-stu-id="8ce50-113">'T</span></span>

<span data-ttu-id="8ce50-114">Целевой объект, на котором выполняется каждая операция в массиве.</span><span class="sxs-lookup"><span data-stu-id="8ce50-114">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="8ce50-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="8ce50-115">See Also</span></span>

- [<span data-ttu-id="8ce50-116">Microsoft. тактов. Canon. Bounds</span><span class="sxs-lookup"><span data-stu-id="8ce50-116">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)