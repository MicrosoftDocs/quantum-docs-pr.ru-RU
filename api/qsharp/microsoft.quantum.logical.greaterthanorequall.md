---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualL
title: Функция Греатерсанорекуалл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualL
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: 5536c009d6e78eac9ab2320b42aec7d2d82946eb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197761"
---
# <a name="greaterthanorequall-function"></a><span data-ttu-id="a5a82-102">Функция Греатерсанорекуалл</span><span class="sxs-lookup"><span data-stu-id="a5a82-102">GreaterThanOrEqualL function</span></span>

<span data-ttu-id="a5a82-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="a5a82-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="a5a82-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a5a82-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a5a82-105">Возвращает значение true только в том случае, если число больше или равно другому числу.</span><span class="sxs-lookup"><span data-stu-id="a5a82-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="a5a82-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a5a82-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="a5a82-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="a5a82-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="a5a82-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="a5a82-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="a5a82-109">б: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="a5a82-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="a5a82-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="a5a82-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="a5a82-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a5a82-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a5a82-112">`true` значение и, только если `a` значение больше или равно `b` .</span><span class="sxs-lookup"><span data-stu-id="a5a82-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5a82-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5a82-113">Remarks</span></span>

<span data-ttu-id="a5a82-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="a5a82-114">The following are equivalent:</span></span>

```Q#
let cond = a >= b;
let cond = GreaterThanOrEqualL(a, b);
```