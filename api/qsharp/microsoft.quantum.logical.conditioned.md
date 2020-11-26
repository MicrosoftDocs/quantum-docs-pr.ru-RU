---
uid: Microsoft.Quantum.Logical.Conditioned
title: Условная функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Conditioned
qsharp.summary: Returns one of two values, depending on the value of a Boolean condition.
ms.openlocfilehash: c0f55d4db95ad1f0d2b7f291cbc6ba8ae704cb81
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198492"
---
# <a name="conditioned-function"></a><span data-ttu-id="6737b-102">Условная функция</span><span class="sxs-lookup"><span data-stu-id="6737b-102">Conditioned function</span></span>

<span data-ttu-id="6737b-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="6737b-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="6737b-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6737b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6737b-105">Возвращает одно из двух значений в зависимости от значения логического условия.</span><span class="sxs-lookup"><span data-stu-id="6737b-105">Returns one of two values, depending on the value of a Boolean condition.</span></span>

```qsharp
function Conditioned<'T> (condition : Bool, ifTrue : 'T, ifFalse : 'T) : 'T
```


## <a name="input"></a><span data-ttu-id="6737b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6737b-106">Input</span></span>

### <a name="condition--bool"></a><span data-ttu-id="6737b-107">условие: [логическое](xref:microsoft.quantum.lang-ref.bool) значение</span><span class="sxs-lookup"><span data-stu-id="6737b-107">condition : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="6737b-108">Условие, используемое для управления возвращаемыми входными данными.</span><span class="sxs-lookup"><span data-stu-id="6737b-108">A condition used to control which input is returned.</span></span>


### <a name="iftrue--t"></a><span data-ttu-id="6737b-109">ifTrue: 'T</span><span class="sxs-lookup"><span data-stu-id="6737b-109">ifTrue : 'T</span></span>

<span data-ttu-id="6737b-110">Значение, возвращаемое, если `condition` равно `true` .</span><span class="sxs-lookup"><span data-stu-id="6737b-110">The value to be returned when `condition` is `true`.</span></span>


### <a name="iffalse--t"></a><span data-ttu-id="6737b-111">ifFalse: 'T</span><span class="sxs-lookup"><span data-stu-id="6737b-111">ifFalse : 'T</span></span>

<span data-ttu-id="6737b-112">Значение, возвращаемое, если `condition` равно `false` .</span><span class="sxs-lookup"><span data-stu-id="6737b-112">The value to be returned when `condition` is `false`.</span></span>



## <a name="output--t"></a><span data-ttu-id="6737b-113">Выходные данные: 'T</span><span class="sxs-lookup"><span data-stu-id="6737b-113">Output : 'T</span></span>

<span data-ttu-id="6737b-114">`ifTrue` Если `condition` имеет значение `true` , и `ifFalse` в противном случае —.</span><span class="sxs-lookup"><span data-stu-id="6737b-114">`ifTrue` if `condition` is `true`, and `ifFalse` otherwise.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="6737b-115">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="6737b-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6737b-116">Е</span><span class="sxs-lookup"><span data-stu-id="6737b-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="6737b-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6737b-117">Remarks</span></span>

<span data-ttu-id="6737b-118">В отличие от `?|` оператора, эта функция не является сокращенной, так что оба входа полностью оцениваются.</span><span class="sxs-lookup"><span data-stu-id="6737b-118">Unlike the `?|` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="6737b-119">Ниже приведены эквивалентные действия для сокращенного поведения.</span><span class="sxs-lookup"><span data-stu-id="6737b-119">Up to short-circuiting behavior, the following are equivalent:</span></span>

```Q#
let x = condition ? ifTrue | ifFalse;
let x = Conditioned(condition, ifTrue, ifFalse);
```