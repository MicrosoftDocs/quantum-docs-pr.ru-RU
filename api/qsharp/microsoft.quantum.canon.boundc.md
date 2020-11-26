---
uid: Microsoft.Quantum.Canon.BoundC
title: Функция Баундк
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundC
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `C` indicates that all operations in the array are controllable.
ms.openlocfilehash: 02e9b6a9676cdd1996d3a2413b2a6383e3a4e90e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207587"
---
# <a name="boundc-function"></a><span data-ttu-id="aa217-102">Функция Баундк</span><span class="sxs-lookup"><span data-stu-id="aa217-102">BoundC function</span></span>

<span data-ttu-id="aa217-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="aa217-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="aa217-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="aa217-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="aa217-105">При наличии массива операций, исдействующих один вход, создает новую операцию, которая выполняет каждую заданную операцию последовательно.</span><span class="sxs-lookup"><span data-stu-id="aa217-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="aa217-106">Модификатор `C` указывает, что все операции в массиве являются управляемыми.</span><span class="sxs-lookup"><span data-stu-id="aa217-106">The modifier `C` indicates that all operations in the array are controllable.</span></span>

```qsharp
function BoundC<'T> (operations : ('T => Unit is Ctl)[]) : ('T => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="aa217-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="aa217-107">Input</span></span>

### <a name="operations--t--unit--is-ctl"></a><span data-ttu-id="aa217-108">операции: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — CTL []</span><span class="sxs-lookup"><span data-stu-id="aa217-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl[]</span></span>

<span data-ttu-id="aa217-109">Последовательность операций, выполняемых с заданным входом.</span><span class="sxs-lookup"><span data-stu-id="aa217-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit--is-ctl"></a><span data-ttu-id="aa217-110">Выходные данные: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  является CTL</span><span class="sxs-lookup"><span data-stu-id="aa217-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="aa217-111">Новая операция, которая выполняет каждую заданную операцию последовательно по входным данным.</span><span class="sxs-lookup"><span data-stu-id="aa217-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="aa217-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="aa217-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="aa217-113">Е</span><span class="sxs-lookup"><span data-stu-id="aa217-113">'T</span></span>

<span data-ttu-id="aa217-114">Целевой объект, на котором выполняется каждая операция в массиве.</span><span class="sxs-lookup"><span data-stu-id="aa217-114">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="aa217-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="aa217-115">See Also</span></span>

- [<span data-ttu-id="aa217-116">Microsoft. тактов. Canon. Bounds</span><span class="sxs-lookup"><span data-stu-id="aa217-116">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)