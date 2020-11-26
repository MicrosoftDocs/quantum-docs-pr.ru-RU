---
uid: Microsoft.Quantum.Logical.EqualL
title: Функция EQUAL
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualL
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 395b8fedd3b3334939c2a4b5602ee19e0c6e34b0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198118"
---
# <a name="equall-function"></a><span data-ttu-id="9379c-102">Функция EQUAL</span><span class="sxs-lookup"><span data-stu-id="9379c-102">EqualL function</span></span>

<span data-ttu-id="9379c-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="9379c-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="9379c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9379c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9379c-105">Возвращает значение true только в том случае, если два входных значения равны.</span><span class="sxs-lookup"><span data-stu-id="9379c-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="9379c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9379c-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="9379c-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="9379c-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="9379c-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="9379c-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="9379c-109">б: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="9379c-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="9379c-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="9379c-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="9379c-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="9379c-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="9379c-112">`true` Если и, только если `a` равно `b` .</span><span class="sxs-lookup"><span data-stu-id="9379c-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="9379c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9379c-113">Remarks</span></span>

<span data-ttu-id="9379c-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="9379c-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualL(a, b);
```