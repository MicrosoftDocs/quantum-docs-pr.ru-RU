---
uid: Microsoft.Quantum.Logical.GreaterThanD
title: Функция Греатерсанд
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanD
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: 26a963645758b6de83654304c38830af5c561b3a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849222"
---
# <a name="greaterthand-function"></a><span data-ttu-id="45026-102">Функция Греатерсанд</span><span class="sxs-lookup"><span data-stu-id="45026-102">GreaterThanD function</span></span>

<span data-ttu-id="45026-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="45026-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="45026-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="45026-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="45026-105">Возвращает значение true только в том случае, если число больше, чем другое число.</span><span class="sxs-lookup"><span data-stu-id="45026-105">Returns true if and only if a number is greater than another number.</span></span>

```qsharp
function GreaterThanD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="45026-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="45026-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="45026-107">ответ. [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="45026-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="45026-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="45026-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="45026-109">б: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="45026-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="45026-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="45026-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="45026-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="45026-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="45026-112">`true` только в случае, если `a` строго больше `b` .</span><span class="sxs-lookup"><span data-stu-id="45026-112">`true` if and only if `a` is strictly greater than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="45026-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="45026-113">Remarks</span></span>

<span data-ttu-id="45026-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="45026-114">The following are equivalent:</span></span>

```qsharp
let cond = a > b;
let cond = GreaterThanD(a, b);
```