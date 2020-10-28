---
uid: Microsoft.Quantum.Canon.ApplyIfElseBCA
title: Операция Апплифелсебка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseBCA
qsharp.summary: Applies one of two unitary operations, depending on the value of a classical bit.
ms.openlocfilehash: 0ebd086f4c8166a8d6b593200b0a3354c1420c6e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718197"
---
# <a name="applyifelsebca-operation"></a><span data-ttu-id="13973-102">Операция Апплифелсебка</span><span class="sxs-lookup"><span data-stu-id="13973-102">ApplyIfElseBCA operation</span></span>

<span data-ttu-id="13973-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="13973-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="13973-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="13973-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="13973-105">Применяет одну из двух операций в зависимости от значения классического бита.</span><span class="sxs-lookup"><span data-stu-id="13973-105">Applies one of two unitary operations, depending on the value of a classical bit.</span></span>

```qsharp
operation ApplyIfElseBCA<'T, 'U> (bit : Bool, (trueOp : ('T => Unit is Adj + Ctl), trueInput : 'T), (falseOp : ('U => Unit is Adj + Ctl), falseInput : 'U)) : Unit
```


## <a name="description"></a><span data-ttu-id="13973-106">Описание</span><span class="sxs-lookup"><span data-stu-id="13973-106">Description</span></span>

<span data-ttu-id="13973-107">Учитывая бит `bit` , применяет операцию `trueOp` с в `trueInput` качестве входных данных `bit` , если имеет значение `true` , и применяется, `falseOp(falseInput)` Если `bit` имеет значение `false` .</span><span class="sxs-lookup"><span data-stu-id="13973-107">Given a bit `bit`, applies the operation `trueOp` with `trueInput` as its input when `bit` is `true`, and applies `falseOp(falseInput)` when `bit` is `false`.</span></span>

## <a name="input"></a><span data-ttu-id="13973-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="13973-108">Input</span></span>

### <a name="bit--bool"></a><span data-ttu-id="13973-109">bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="13973-109">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="13973-110">Логическое значение, используемое для определения того, применяется ли оператор `trueOp` или `falseOp` .</span><span class="sxs-lookup"><span data-stu-id="13973-110">The boolean value used to determine whether `trueOp` or `falseOp` is applied.</span></span>


### <a name="trueop--t--unit-adj--ctl"></a><span data-ttu-id="13973-111">Труеоп: 'T => [модульные](xref:microsoft.quantum.lang-ref.unit) года + CTL</span><span class="sxs-lookup"><span data-stu-id="13973-111">trueOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="13973-112">Единая операция, применяемая, если `bit` имеет значение `true` .</span><span class="sxs-lookup"><span data-stu-id="13973-112">The unitary operation to be applied when `bit` is `true`.</span></span>


### <a name="trueinput--t"></a><span data-ttu-id="13973-113">Труеинпут: 'T</span><span class="sxs-lookup"><span data-stu-id="13973-113">trueInput : 'T</span></span>

<span data-ttu-id="13973-114">Входные данные, которые должны быть предоставлены, `trueOp` Если `bit` имеет значение `true` .</span><span class="sxs-lookup"><span data-stu-id="13973-114">The input to be provided to `trueOp` when `bit` is `true`.</span></span>


### <a name="falseop--u--unit-adj--ctl"></a><span data-ttu-id="13973-115">Фалсеоп: "U => [единицы](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="13973-115">falseOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="13973-116">Единая операция, применяемая, если `bit` имеет значение `false` .</span><span class="sxs-lookup"><span data-stu-id="13973-116">The unitary operation to be applied when `bit` is `false`.</span></span>


### <a name="falseinput--u"></a><span data-ttu-id="13973-117">Фалсеинпут: ' U</span><span class="sxs-lookup"><span data-stu-id="13973-117">falseInput : 'U</span></span>

<span data-ttu-id="13973-118">Входные данные, которые должны быть предоставлены, `falseOp` Если `bit` имеет значение `false` .</span><span class="sxs-lookup"><span data-stu-id="13973-118">The input to be provided to `falseOp` when `bit` is `false`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="13973-119">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="13973-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="13973-120">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="13973-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="13973-121">Е</span><span class="sxs-lookup"><span data-stu-id="13973-121">'T</span></span>

<span data-ttu-id="13973-122">Тип входных данных операции `trueOp` , которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="13973-122">The input type of the operation `trueOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="13973-123">' U</span><span class="sxs-lookup"><span data-stu-id="13973-123">'U</span></span>

<span data-ttu-id="13973-124">Тип входных данных операции `falseOp` , которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="13973-124">The input type of the operation `falseOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="13973-125">См. также:</span><span class="sxs-lookup"><span data-stu-id="13973-125">See Also</span></span>

- [<span data-ttu-id="13973-126">Microsoft. тактов. Canon. Апплифзеро</span><span class="sxs-lookup"><span data-stu-id="13973-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="13973-127">Microsoft. тактов. Canon. Апплифоне</span><span class="sxs-lookup"><span data-stu-id="13973-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="13973-128">Microsoft. тактов. Canon. Апплифелсерк</span><span class="sxs-lookup"><span data-stu-id="13973-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="13973-129">Microsoft. тактов. Canon. Апплифелсера</span><span class="sxs-lookup"><span data-stu-id="13973-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="13973-130">Microsoft. тактов. Canon. Апплифелсерка</span><span class="sxs-lookup"><span data-stu-id="13973-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)