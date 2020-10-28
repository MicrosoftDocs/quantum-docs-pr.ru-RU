---
uid: Microsoft.Quantum.Canon.NoOp
title: Операция NoOp
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: NoOp
qsharp.summary: Performs the identity operation (no-op) on an argument.
ms.openlocfilehash: 987e39577c3b736418234431ed7a915ae461f763
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715761"
---
# <a name="noop-operation"></a><span data-ttu-id="bd6b9-102">Операция NoOp</span><span class="sxs-lookup"><span data-stu-id="bd6b9-102">NoOp operation</span></span>

<span data-ttu-id="bd6b9-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="bd6b9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="bd6b9-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bd6b9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bd6b9-105">Выполняет операцию идентификации (No-op) для аргумента.</span><span class="sxs-lookup"><span data-stu-id="bd6b9-105">Performs the identity operation (no-op) on an argument.</span></span>

```qsharp
operation NoOp<'T> (input : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="bd6b9-106">Описание</span><span class="sxs-lookup"><span data-stu-id="bd6b9-106">Description</span></span>

<span data-ttu-id="bd6b9-107">Эта операция принимает значение любого типа и не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="bd6b9-107">This operation takes a value of any type and does nothing to it.</span></span>
<span data-ttu-id="bd6b9-108">Это может быть полезно, если ожидается входные данные типа операции, но никакие действия не выполняются.</span><span class="sxs-lookup"><span data-stu-id="bd6b9-108">This can be useful whenever an input of an operation type is expected, but no action should be taken.</span></span>
<span data-ttu-id="bd6b9-109">Например, если определенная ошибка исправления ошибки синдром указывает на отсутствие ошибок, `NoOp<Qubit[]>` может быть правильной процедурой восстановления.</span><span class="sxs-lookup"><span data-stu-id="bd6b9-109">For instance, if a particular error correction syndrome indicates that no error has occurred, `NoOp<Qubit[]>` may be the correct recovery procedure.</span></span>
<span data-ttu-id="bd6b9-110">Аналогично, если в качестве входных данных для операции требуется процедура подготовки состояния, `NoOp<Qubit[]>` можно использовать для подготовки состояния $ \ket{0 \кдотс 0} $.</span><span class="sxs-lookup"><span data-stu-id="bd6b9-110">Similarly, if an operation expects a state preparation procedure as input, `NoOp<Qubit[]>` can be used to prepare the state $\ket{0 \cdots 0}$.</span></span>

## <a name="input"></a><span data-ttu-id="bd6b9-111">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bd6b9-111">Input</span></span>

### <a name="input--t"></a><span data-ttu-id="bd6b9-112">входные данные: 'T</span><span class="sxs-lookup"><span data-stu-id="bd6b9-112">input : 'T</span></span>

<span data-ttu-id="bd6b9-113">Значение, которое необходимо пропускать.</span><span class="sxs-lookup"><span data-stu-id="bd6b9-113">A value to be ignored.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bd6b9-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bd6b9-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="bd6b9-115">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="bd6b9-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="bd6b9-116">Е</span><span class="sxs-lookup"><span data-stu-id="bd6b9-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="bd6b9-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="bd6b9-117">Remarks</span></span>

<span data-ttu-id="bd6b9-118">Почти во всех случаях параметр типа для `NoOp` должен быть указан явным образом.</span><span class="sxs-lookup"><span data-stu-id="bd6b9-118">In almost all cases, the type parameter for `NoOp` needs to be specified explicitly.</span></span> <span data-ttu-id="bd6b9-119">Например, `NoOp<Qubit>` идентично <xref:microsoft.quantum.intrinsic.i> .</span><span class="sxs-lookup"><span data-stu-id="bd6b9-119">For instance, `NoOp<Qubit>` is identical to <xref:microsoft.quantum.intrinsic.i>.</span></span>

## <a name="see-also"></a><span data-ttu-id="bd6b9-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="bd6b9-120">See Also</span></span>

- [<span data-ttu-id="bd6b9-121">Microsoft. тактов. внутренний. I</span><span class="sxs-lookup"><span data-stu-id="bd6b9-121">Microsoft.Quantum.Intrinsic.I</span></span>](xref:Microsoft.Quantum.Intrinsic.I)