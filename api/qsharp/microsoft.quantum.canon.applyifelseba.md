---
uid: Microsoft.Quantum.Canon.ApplyIfElseBA
title: Операция Апплифелсеба
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseBA
qsharp.summary: Applies one of two adjointable operations, depending on the value of a classical bit.
ms.openlocfilehash: a85567a49df1f261b95f3553da8dc789ce924e7a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844989"
---
# <a name="applyifelseba-operation"></a><span data-ttu-id="1424a-102">Операция Апплифелсеба</span><span class="sxs-lookup"><span data-stu-id="1424a-102">ApplyIfElseBA operation</span></span>

<span data-ttu-id="1424a-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1424a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1424a-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1424a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1424a-105">Применяет одну из двух операций аджоинтабле в зависимости от значения классического бита.</span><span class="sxs-lookup"><span data-stu-id="1424a-105">Applies one of two adjointable operations, depending on the value of a classical bit.</span></span>

```qsharp
operation ApplyIfElseBA<'T, 'U> (bit : Bool, (trueOp : ('T => Unit is Adj), trueInput : 'T), (falseOp : ('U => Unit is Adj), falseInput : 'U)) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="1424a-106">Описание</span><span class="sxs-lookup"><span data-stu-id="1424a-106">Description</span></span>

<span data-ttu-id="1424a-107">Учитывая бит `bit` , применяет операцию `trueOp` с в `trueInput` качестве входных данных `bit` , если имеет значение `true` , и применяется, `falseOp(falseInput)` Если `bit` имеет значение `false` .</span><span class="sxs-lookup"><span data-stu-id="1424a-107">Given a bit `bit`, applies the operation `trueOp` with `trueInput` as its input when `bit` is `true`, and applies `falseOp(falseInput)` when `bit` is `false`.</span></span>

## <a name="input"></a><span data-ttu-id="1424a-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="1424a-108">Input</span></span>

### <a name="bit--bool"></a><span data-ttu-id="1424a-109">bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="1424a-109">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="1424a-110">Логическое значение, используемое для определения того, применяется ли оператор `trueOp` или `falseOp` .</span><span class="sxs-lookup"><span data-stu-id="1424a-110">The boolean value used to determine whether `trueOp` or `falseOp` is applied.</span></span>


### <a name="trueop--t--unit--is-adj"></a><span data-ttu-id="1424a-111">Труеоп: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  Нагода</span><span class="sxs-lookup"><span data-stu-id="1424a-111">trueOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="1424a-112">Операция аджоинтабле, применяемая, если `bit` имеет значение `true` .</span><span class="sxs-lookup"><span data-stu-id="1424a-112">The adjointable operation to be applied when `bit` is `true`.</span></span>


### <a name="trueinput--t"></a><span data-ttu-id="1424a-113">Труеинпут: 'T</span><span class="sxs-lookup"><span data-stu-id="1424a-113">trueInput : 'T</span></span>

<span data-ttu-id="1424a-114">Входные данные, которые должны быть предоставлены, `trueOp` Если `bit` имеет значение `true` .</span><span class="sxs-lookup"><span data-stu-id="1424a-114">The input to be provided to `trueOp` when `bit` is `true`.</span></span>


### <a name="falseop--u--unit--is-adj"></a><span data-ttu-id="1424a-115">Фалсеоп: "U = [единица](xref:microsoft.quantum.lang-ref.unit) > является просуммой</span><span class="sxs-lookup"><span data-stu-id="1424a-115">falseOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="1424a-116">Операция аджоинтабле, применяемая, если `bit` имеет значение `false` .</span><span class="sxs-lookup"><span data-stu-id="1424a-116">The adjointable operation to be applied when `bit` is `false`.</span></span>


### <a name="falseinput--u"></a><span data-ttu-id="1424a-117">Фалсеинпут: ' U</span><span class="sxs-lookup"><span data-stu-id="1424a-117">falseInput : 'U</span></span>

<span data-ttu-id="1424a-118">Входные данные, которые должны быть предоставлены, `falseOp` Если `bit` имеет значение `false` .</span><span class="sxs-lookup"><span data-stu-id="1424a-118">The input to be provided to `falseOp` when `bit` is `false`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1424a-119">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1424a-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="1424a-120">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="1424a-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1424a-121">Е</span><span class="sxs-lookup"><span data-stu-id="1424a-121">'T</span></span>

<span data-ttu-id="1424a-122">Тип входных данных операции `trueOp` , которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="1424a-122">The input type of the operation `trueOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="1424a-123">' U</span><span class="sxs-lookup"><span data-stu-id="1424a-123">'U</span></span>

<span data-ttu-id="1424a-124">Тип входных данных операции `falseOp` , которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="1424a-124">The input type of the operation `falseOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="1424a-125">См. также:</span><span class="sxs-lookup"><span data-stu-id="1424a-125">See Also</span></span>

- [<span data-ttu-id="1424a-126">Microsoft. тактов. Canon. Апплифзеро</span><span class="sxs-lookup"><span data-stu-id="1424a-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="1424a-127">Microsoft. тактов. Canon. Апплифоне</span><span class="sxs-lookup"><span data-stu-id="1424a-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="1424a-128">Microsoft. тактов. Canon. Апплифелсерк</span><span class="sxs-lookup"><span data-stu-id="1424a-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="1424a-129">Microsoft. тактов. Canon. Апплифелсера</span><span class="sxs-lookup"><span data-stu-id="1424a-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="1424a-130">Microsoft. тактов. Canon. Апплифелсерка</span><span class="sxs-lookup"><span data-stu-id="1424a-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)