---
uid: Microsoft.Quantum.Canon.BoundCA
title: Функция Баундка
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundCA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `CA` indicates that all operations in the array are adjointable and controllable.
ms.openlocfilehash: 774a6f57566dce75b98290a7e81540b28afea1af
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216887"
---
# <a name="boundca-function"></a><span data-ttu-id="f2b2f-102">Функция Баундка</span><span class="sxs-lookup"><span data-stu-id="f2b2f-102">BoundCA function</span></span>

<span data-ttu-id="f2b2f-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f2b2f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f2b2f-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f2b2f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f2b2f-105">При наличии массива операций, исдействующих один вход, создает новую операцию, которая выполняет каждую заданную операцию последовательно.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="f2b2f-106">Модификатор `CA` указывает, что все операции в массиве являются аджоинтабле и управляемыми.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-106">The modifier `CA` indicates that all operations in the array are adjointable and controllable.</span></span>

```qsharp
function BoundCA<'T> (operations : ('T => Unit is Adj + Ctl)[]) : ('T => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="f2b2f-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f2b2f-107">Input</span></span>

### <a name="operations--t--unit--is-adj--ctl"></a><span data-ttu-id="f2b2f-108">Operations: t => [Unit](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL []"</span><span class="sxs-lookup"><span data-stu-id="f2b2f-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl[]</span></span>

<span data-ttu-id="f2b2f-109">Последовательность операций, выполняемых с заданным входом.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit--is-adj--ctl"></a><span data-ttu-id="f2b2f-110">Выходные данные: 'T => [единицы измерения](xref:microsoft.quantum.lang-ref.unit)  и CTL</span><span class="sxs-lookup"><span data-stu-id="f2b2f-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="f2b2f-111">Новая операция, которая выполняет каждую заданную операцию последовательно по входным данным.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f2b2f-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="f2b2f-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f2b2f-113">Е</span><span class="sxs-lookup"><span data-stu-id="f2b2f-113">'T</span></span>

<span data-ttu-id="f2b2f-114">Целевой объект, на котором выполняется каждая операция в массиве.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-114">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="f2b2f-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="f2b2f-115">See Also</span></span>

- [<span data-ttu-id="f2b2f-116">Microsoft. тактов. Canon. Bounds</span><span class="sxs-lookup"><span data-stu-id="f2b2f-116">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)