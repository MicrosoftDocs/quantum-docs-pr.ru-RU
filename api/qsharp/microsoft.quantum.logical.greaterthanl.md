---
uid: Microsoft.Quantum.Logical.GreaterThanL
title: Функция Греатерсанл
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanL
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: 2247c1c1ae8b37b59e87c0c68b06fd1094c9003b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849203"
---
# <a name="greaterthanl-function"></a><span data-ttu-id="df30c-102">Функция Греатерсанл</span><span class="sxs-lookup"><span data-stu-id="df30c-102">GreaterThanL function</span></span>

<span data-ttu-id="df30c-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="df30c-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="df30c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="df30c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="df30c-105">Возвращает значение true только в том случае, если число больше, чем другое число.</span><span class="sxs-lookup"><span data-stu-id="df30c-105">Returns true if and only if a number is greater than another number.</span></span>

```qsharp
function GreaterThanL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="df30c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="df30c-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="df30c-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="df30c-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="df30c-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="df30c-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="df30c-109">б: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="df30c-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="df30c-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="df30c-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="df30c-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="df30c-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="df30c-112">`true` только в случае, если `a` строго больше `b` .</span><span class="sxs-lookup"><span data-stu-id="df30c-112">`true` if and only if `a` is strictly greater than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="df30c-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="df30c-113">Remarks</span></span>

<span data-ttu-id="df30c-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="df30c-114">The following are equivalent:</span></span>

```qsharp
let cond = a > b;
let cond = GreaterThanL(a, b);
```