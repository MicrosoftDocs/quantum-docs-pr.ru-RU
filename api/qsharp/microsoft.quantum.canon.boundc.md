---
uid: Microsoft.Quantum.Canon.BoundC
title: Функция Баундк
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundC
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `C` indicates that all operations in the array are controllable.
ms.openlocfilehash: 04dca4ff317bf3cee053f7c3903112f4e05a3973
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716671"
---
# <a name="boundc-function"></a><span data-ttu-id="2aa17-102">Функция Баундк</span><span class="sxs-lookup"><span data-stu-id="2aa17-102">BoundC function</span></span>

<span data-ttu-id="2aa17-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2aa17-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2aa17-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2aa17-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2aa17-105">При наличии массива операций, исдействующих один вход, создает новую операцию, которая выполняет каждую заданную операцию последовательно.</span><span class="sxs-lookup"><span data-stu-id="2aa17-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="2aa17-106">Модификатор `C` указывает, что все операции в массиве являются управляемыми.</span><span class="sxs-lookup"><span data-stu-id="2aa17-106">The modifier `C` indicates that all operations in the array are controllable.</span></span>

```qsharp
function BoundC<'T> (operations : ('T => Unit is Ctl)[]) : ('T => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="2aa17-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2aa17-107">Input</span></span>

### <a name="operations--t--unit-ctl"></a><span data-ttu-id="2aa17-108">операции: # => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL []</span><span class="sxs-lookup"><span data-stu-id="2aa17-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl[]</span></span>

<span data-ttu-id="2aa17-109">Последовательность операций, выполняемых с заданным входом.</span><span class="sxs-lookup"><span data-stu-id="2aa17-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit-ctl"></a><span data-ttu-id="2aa17-110">Выходные данные: 'T => [единицы](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="2aa17-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="2aa17-111">Новая операция, которая выполняет каждую заданную операцию последовательно по входным данным.</span><span class="sxs-lookup"><span data-stu-id="2aa17-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="2aa17-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="2aa17-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2aa17-113">Е</span><span class="sxs-lookup"><span data-stu-id="2aa17-113">'T</span></span>

<span data-ttu-id="2aa17-114">Целевой объект, на котором выполняется каждая операция в массиве.</span><span class="sxs-lookup"><span data-stu-id="2aa17-114">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="2aa17-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="2aa17-115">See Also</span></span>

- [<span data-ttu-id="2aa17-116">Microsoft. тактов. Canon. Bounds</span><span class="sxs-lookup"><span data-stu-id="2aa17-116">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)