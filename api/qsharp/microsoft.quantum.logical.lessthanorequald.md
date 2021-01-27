---
uid: Microsoft.Quantum.Logical.LessThanOrEqualD
title: Функция Лесссанорекуалд
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualD
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: 703b782efe9daccd4f6a339481d49ae9232123f3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849140"
---
# <a name="lessthanorequald-function"></a><span data-ttu-id="fbb79-102">Функция Лесссанорекуалд</span><span class="sxs-lookup"><span data-stu-id="fbb79-102">LessThanOrEqualD function</span></span>

<span data-ttu-id="fbb79-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="fbb79-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="fbb79-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fbb79-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fbb79-105">Возвращает значение true только в том случае, если число меньше или равно другому числу.</span><span class="sxs-lookup"><span data-stu-id="fbb79-105">Returns true if and only if a number is less than or equal to another number.</span></span>

```qsharp
function LessThanOrEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="fbb79-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fbb79-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="fbb79-107">ответ. [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fbb79-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fbb79-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="fbb79-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="fbb79-109">б: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fbb79-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fbb79-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="fbb79-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="fbb79-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="fbb79-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="fbb79-112">`true` только в случае, если `a` меньше или равно `b` .</span><span class="sxs-lookup"><span data-stu-id="fbb79-112">`true` if and only if `a` is less than or equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbb79-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="fbb79-113">Remarks</span></span>

<span data-ttu-id="fbb79-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="fbb79-114">The following are equivalent:</span></span>

```qsharp
let cond = a <= b;
let cond = LessThanOrEqualD(a, b);
```