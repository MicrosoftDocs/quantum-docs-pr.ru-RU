---
uid: Microsoft.Quantum.Canon.ApplyIfElseBA
title: Операция Апплифелсеба
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseBA
qsharp.summary: Applies one of two adjointable operations, depending on the value of a classical bit.
ms.openlocfilehash: 74d43344481c5a808e84ce9c9e36fa3e83cd0d89
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218671"
---
# <a name="applyifelseba-operation"></a><span data-ttu-id="9b607-102">Операция Апплифелсеба</span><span class="sxs-lookup"><span data-stu-id="9b607-102">ApplyIfElseBA operation</span></span>

<span data-ttu-id="9b607-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9b607-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9b607-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9b607-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9b607-105">Применяет одну из двух операций аджоинтабле в зависимости от значения классического бита.</span><span class="sxs-lookup"><span data-stu-id="9b607-105">Applies one of two adjointable operations, depending on the value of a classical bit.</span></span>

```qsharp
operation ApplyIfElseBA<'T, 'U> (bit : Bool, (trueOp : ('T => Unit is Adj), trueInput : 'T), (falseOp : ('U => Unit is Adj), falseInput : 'U)) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="9b607-106">Описание</span><span class="sxs-lookup"><span data-stu-id="9b607-106">Description</span></span>

<span data-ttu-id="9b607-107">Учитывая бит `bit` , применяет операцию `trueOp` с в `trueInput` качестве входных данных `bit` , если имеет значение `true` , и применяется, `falseOp(falseInput)` Если `bit` имеет значение `false` .</span><span class="sxs-lookup"><span data-stu-id="9b607-107">Given a bit `bit`, applies the operation `trueOp` with `trueInput` as its input when `bit` is `true`, and applies `falseOp(falseInput)` when `bit` is `false`.</span></span>

## <a name="input"></a><span data-ttu-id="9b607-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9b607-108">Input</span></span>

### <a name="bit--bool"></a><span data-ttu-id="9b607-109">bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="9b607-109">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="9b607-110">Логическое значение, используемое для определения того, применяется ли оператор `trueOp` или `falseOp` .</span><span class="sxs-lookup"><span data-stu-id="9b607-110">The boolean value used to determine whether `trueOp` or `falseOp` is applied.</span></span>


### <a name="trueop--t--unit--is-adj"></a><span data-ttu-id="9b607-111">Труеоп: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  Нагода</span><span class="sxs-lookup"><span data-stu-id="9b607-111">trueOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="9b607-112">Операция аджоинтабле, применяемая, если `bit` имеет значение `true` .</span><span class="sxs-lookup"><span data-stu-id="9b607-112">The adjointable operation to be applied when `bit` is `true`.</span></span>


### <a name="trueinput--t"></a><span data-ttu-id="9b607-113">Труеинпут: 'T</span><span class="sxs-lookup"><span data-stu-id="9b607-113">trueInput : 'T</span></span>

<span data-ttu-id="9b607-114">Входные данные, которые должны быть предоставлены, `trueOp` Если `bit` имеет значение `true` .</span><span class="sxs-lookup"><span data-stu-id="9b607-114">The input to be provided to `trueOp` when `bit` is `true`.</span></span>


### <a name="falseop--u--unit--is-adj"></a><span data-ttu-id="9b607-115">Фалсеоп: "U = [единица](xref:microsoft.quantum.lang-ref.unit) > является просуммой</span><span class="sxs-lookup"><span data-stu-id="9b607-115">falseOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="9b607-116">Операция аджоинтабле, применяемая, если `bit` имеет значение `false` .</span><span class="sxs-lookup"><span data-stu-id="9b607-116">The adjointable operation to be applied when `bit` is `false`.</span></span>


### <a name="falseinput--u"></a><span data-ttu-id="9b607-117">Фалсеинпут: ' U</span><span class="sxs-lookup"><span data-stu-id="9b607-117">falseInput : 'U</span></span>

<span data-ttu-id="9b607-118">Входные данные, которые должны быть предоставлены, `falseOp` Если `bit` имеет значение `false` .</span><span class="sxs-lookup"><span data-stu-id="9b607-118">The input to be provided to `falseOp` when `bit` is `false`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9b607-119">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9b607-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="9b607-120">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="9b607-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9b607-121">Е</span><span class="sxs-lookup"><span data-stu-id="9b607-121">'T</span></span>

<span data-ttu-id="9b607-122">Тип входных данных операции `trueOp` , которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="9b607-122">The input type of the operation `trueOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="9b607-123">' U</span><span class="sxs-lookup"><span data-stu-id="9b607-123">'U</span></span>

<span data-ttu-id="9b607-124">Тип входных данных операции `falseOp` , которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="9b607-124">The input type of the operation `falseOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="9b607-125">См. также:</span><span class="sxs-lookup"><span data-stu-id="9b607-125">See Also</span></span>

- [<span data-ttu-id="9b607-126">Microsoft. тактов. Canon. Апплифзеро</span><span class="sxs-lookup"><span data-stu-id="9b607-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="9b607-127">Microsoft. тактов. Canon. Апплифоне</span><span class="sxs-lookup"><span data-stu-id="9b607-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="9b607-128">Microsoft. тактов. Canon. Апплифелсерк</span><span class="sxs-lookup"><span data-stu-id="9b607-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="9b607-129">Microsoft. тактов. Canon. Апплифелсера</span><span class="sxs-lookup"><span data-stu-id="9b607-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="9b607-130">Microsoft. тактов. Canon. Апплифелсерка</span><span class="sxs-lookup"><span data-stu-id="9b607-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)