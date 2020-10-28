---
uid: Microsoft.Quantum.Logical.Conditioned
title: Условная функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Conditioned
qsharp.summary: Returns one of two values, depending on the value of a Boolean condition.
ms.openlocfilehash: 8aabe8b018129ddee3b934c207d0a62e59fb6f4a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731296"
---
# <a name="conditioned-function"></a><span data-ttu-id="0d7d4-102">Условная функция</span><span class="sxs-lookup"><span data-stu-id="0d7d4-102">Conditioned function</span></span>

<span data-ttu-id="0d7d4-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="0d7d4-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="0d7d4-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0d7d4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0d7d4-105">Возвращает одно из двух значений в зависимости от значения логического условия.</span><span class="sxs-lookup"><span data-stu-id="0d7d4-105">Returns one of two values, depending on the value of a Boolean condition.</span></span>

```qsharp
function Conditioned<'T> (condition : Bool, ifTrue : 'T, ifFalse : 'T) : 'T
```


## <a name="input"></a><span data-ttu-id="0d7d4-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0d7d4-106">Input</span></span>

### <a name="condition--bool"></a><span data-ttu-id="0d7d4-107">условие: [логическое](xref:microsoft.quantum.lang-ref.bool) значение</span><span class="sxs-lookup"><span data-stu-id="0d7d4-107">condition : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="0d7d4-108">Условие, используемое для управления возвращаемыми входными данными.</span><span class="sxs-lookup"><span data-stu-id="0d7d4-108">A condition used to control which input is returned.</span></span>


### <a name="iftrue--t"></a><span data-ttu-id="0d7d4-109">ifTrue: 'T</span><span class="sxs-lookup"><span data-stu-id="0d7d4-109">ifTrue : 'T</span></span>

<span data-ttu-id="0d7d4-110">Значение, возвращаемое, если `condition` равно `true` .</span><span class="sxs-lookup"><span data-stu-id="0d7d4-110">The value to be returned when `condition` is `true`.</span></span>


### <a name="iffalse--t"></a><span data-ttu-id="0d7d4-111">ifFalse: 'T</span><span class="sxs-lookup"><span data-stu-id="0d7d4-111">ifFalse : 'T</span></span>

<span data-ttu-id="0d7d4-112">Значение, возвращаемое, если `condition` равно `false` .</span><span class="sxs-lookup"><span data-stu-id="0d7d4-112">The value to be returned when `condition` is `false`.</span></span>



## <a name="output--t"></a><span data-ttu-id="0d7d4-113">Выходные данные: 'T</span><span class="sxs-lookup"><span data-stu-id="0d7d4-113">Output : 'T</span></span>

<span data-ttu-id="0d7d4-114">`ifTrue` Если `condition` имеет значение `true` , и `ifFalse` в противном случае —.</span><span class="sxs-lookup"><span data-stu-id="0d7d4-114">`ifTrue` if `condition` is `true`, and `ifFalse` otherwise.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="0d7d4-115">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="0d7d4-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0d7d4-116">Е</span><span class="sxs-lookup"><span data-stu-id="0d7d4-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="0d7d4-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="0d7d4-117">Remarks</span></span>

<span data-ttu-id="0d7d4-118">В отличие от `?|` оператора, эта функция не является сокращенной, так что оба входа полностью оцениваются.</span><span class="sxs-lookup"><span data-stu-id="0d7d4-118">Unlike the `?|` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="0d7d4-119">Ниже приведены эквивалентные действия для сокращенного поведения.</span><span class="sxs-lookup"><span data-stu-id="0d7d4-119">Up to short-circuiting behavior, the following are equivalent:</span></span>

```Q#
let x = condition ? ifTrue | ifFalse;
let x = Conditioned(condition, ifTrue, ifFalse);
```