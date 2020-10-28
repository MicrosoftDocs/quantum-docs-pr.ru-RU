---
uid: Microsoft.Quantum.Logical.NotEqualL
title: Функция Нотекуалл
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualL
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: f1d36c284293519e75e6c30ac64679c7bdf4609c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709811"
---
# <a name="notequall-function"></a><span data-ttu-id="40486-102">Функция Нотекуалл</span><span class="sxs-lookup"><span data-stu-id="40486-102">NotEqualL function</span></span>

<span data-ttu-id="40486-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="40486-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="40486-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="40486-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="40486-105">Возвращает значение true только в том случае, если два входных значения не равны.</span><span class="sxs-lookup"><span data-stu-id="40486-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="40486-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="40486-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="40486-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="40486-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="40486-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="40486-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="40486-109">б: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="40486-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="40486-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="40486-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="40486-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="40486-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="40486-112">`true` Если и, только если `a` не равно `b` .</span><span class="sxs-lookup"><span data-stu-id="40486-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="40486-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="40486-113">Remarks</span></span>

<span data-ttu-id="40486-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="40486-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualL(a, b);
```