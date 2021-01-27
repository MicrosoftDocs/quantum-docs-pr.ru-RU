---
uid: Microsoft.Quantum.Canon.ApplyIfElseBCA
title: Операция Апплифелсебка
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseBCA
qsharp.summary: Applies one of two unitary operations, depending on the value of a classical bit.
ms.openlocfilehash: 3ed9d7cbf277f4c3acd0e6c3b5f920c3e140855d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844970"
---
# <a name="applyifelsebca-operation"></a><span data-ttu-id="0d895-102">Операция Апплифелсебка</span><span class="sxs-lookup"><span data-stu-id="0d895-102">ApplyIfElseBCA operation</span></span>

<span data-ttu-id="0d895-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0d895-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0d895-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0d895-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0d895-105">Применяет одну из двух операций в зависимости от значения классического бита.</span><span class="sxs-lookup"><span data-stu-id="0d895-105">Applies one of two unitary operations, depending on the value of a classical bit.</span></span>

```qsharp
operation ApplyIfElseBCA<'T, 'U> (bit : Bool, (trueOp : ('T => Unit is Adj + Ctl), trueInput : 'T), (falseOp : ('U => Unit is Adj + Ctl), falseInput : 'U)) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="0d895-106">Описание</span><span class="sxs-lookup"><span data-stu-id="0d895-106">Description</span></span>

<span data-ttu-id="0d895-107">Учитывая бит `bit` , применяет операцию `trueOp` с в `trueInput` качестве входных данных `bit` , если имеет значение `true` , и применяется, `falseOp(falseInput)` Если `bit` имеет значение `false` .</span><span class="sxs-lookup"><span data-stu-id="0d895-107">Given a bit `bit`, applies the operation `trueOp` with `trueInput` as its input when `bit` is `true`, and applies `falseOp(falseInput)` when `bit` is `false`.</span></span>

## <a name="input"></a><span data-ttu-id="0d895-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0d895-108">Input</span></span>

### <a name="bit--bool"></a><span data-ttu-id="0d895-109">bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="0d895-109">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="0d895-110">Логическое значение, используемое для определения того, применяется ли оператор `trueOp` или `falseOp` .</span><span class="sxs-lookup"><span data-stu-id="0d895-110">The boolean value used to determine whether `trueOp` or `falseOp` is applied.</span></span>


### <a name="trueop--t--unit--is-adj--ctl"></a><span data-ttu-id="0d895-111">Труеоп: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="0d895-111">trueOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="0d895-112">Единая операция, применяемая, если `bit` имеет значение `true` .</span><span class="sxs-lookup"><span data-stu-id="0d895-112">The unitary operation to be applied when `bit` is `true`.</span></span>


### <a name="trueinput--t"></a><span data-ttu-id="0d895-113">Труеинпут: 'T</span><span class="sxs-lookup"><span data-stu-id="0d895-113">trueInput : 'T</span></span>

<span data-ttu-id="0d895-114">Входные данные, которые должны быть предоставлены, `trueOp` Если `bit` имеет значение `true` .</span><span class="sxs-lookup"><span data-stu-id="0d895-114">The input to be provided to `trueOp` when `bit` is `true`.</span></span>


### <a name="falseop--u--unit--is-adj--ctl"></a><span data-ttu-id="0d895-115">Фалсеоп: "U => [единицей](xref:microsoft.quantum.lang-ref.unit)  является список" года + CTL "</span><span class="sxs-lookup"><span data-stu-id="0d895-115">falseOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="0d895-116">Единая операция, применяемая, если `bit` имеет значение `false` .</span><span class="sxs-lookup"><span data-stu-id="0d895-116">The unitary operation to be applied when `bit` is `false`.</span></span>


### <a name="falseinput--u"></a><span data-ttu-id="0d895-117">Фалсеинпут: ' U</span><span class="sxs-lookup"><span data-stu-id="0d895-117">falseInput : 'U</span></span>

<span data-ttu-id="0d895-118">Входные данные, которые должны быть предоставлены, `falseOp` Если `bit` имеет значение `false` .</span><span class="sxs-lookup"><span data-stu-id="0d895-118">The input to be provided to `falseOp` when `bit` is `false`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0d895-119">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0d895-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="0d895-120">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="0d895-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0d895-121">Е</span><span class="sxs-lookup"><span data-stu-id="0d895-121">'T</span></span>

<span data-ttu-id="0d895-122">Тип входных данных операции `trueOp` , которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="0d895-122">The input type of the operation `trueOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="0d895-123">' U</span><span class="sxs-lookup"><span data-stu-id="0d895-123">'U</span></span>

<span data-ttu-id="0d895-124">Тип входных данных операции `falseOp` , которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="0d895-124">The input type of the operation `falseOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d895-125">См. также:</span><span class="sxs-lookup"><span data-stu-id="0d895-125">See Also</span></span>

- [<span data-ttu-id="0d895-126">Microsoft. тактов. Canon. Апплифзеро</span><span class="sxs-lookup"><span data-stu-id="0d895-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="0d895-127">Microsoft. тактов. Canon. Апплифоне</span><span class="sxs-lookup"><span data-stu-id="0d895-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="0d895-128">Microsoft. тактов. Canon. Апплифелсерк</span><span class="sxs-lookup"><span data-stu-id="0d895-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="0d895-129">Microsoft. тактов. Canon. Апплифелсера</span><span class="sxs-lookup"><span data-stu-id="0d895-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="0d895-130">Microsoft. тактов. Canon. Апплифелсерка</span><span class="sxs-lookup"><span data-stu-id="0d895-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)