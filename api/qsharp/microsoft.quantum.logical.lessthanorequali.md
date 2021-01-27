---
uid: Microsoft.Quantum.Logical.LessThanOrEqualI
title: Функция Лесссанорекуали
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualI
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: 9438fc05b4ccb041b087f9cfeb30ac0c8cfcabd6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98815604"
---
# <a name="lessthanorequali-function"></a><span data-ttu-id="82527-102">Функция Лесссанорекуали</span><span class="sxs-lookup"><span data-stu-id="82527-102">LessThanOrEqualI function</span></span>

<span data-ttu-id="82527-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="82527-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="82527-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="82527-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="82527-105">Возвращает значение true только в том случае, если число меньше или равно другому числу.</span><span class="sxs-lookup"><span data-stu-id="82527-105">Returns true if and only if a number is less than or equal to another number.</span></span>

```qsharp
function LessThanOrEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="82527-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="82527-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="82527-107">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="82527-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="82527-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="82527-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="82527-109">б: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="82527-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="82527-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="82527-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="82527-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="82527-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="82527-112">`true` только в случае, если `a` меньше или равно `b` .</span><span class="sxs-lookup"><span data-stu-id="82527-112">`true` if and only if `a` is less than or equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="82527-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="82527-113">Remarks</span></span>

<span data-ttu-id="82527-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="82527-114">The following are equivalent:</span></span>

```qsharp
let cond = a <= b;
let cond = LessThanOrEqualI(a, b);
```