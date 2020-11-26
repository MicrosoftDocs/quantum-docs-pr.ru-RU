---
uid: Microsoft.Quantum.Logical.NotNearlyEqualD
title: Функция Нотнеарлекуалд
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotNearlyEqualD
qsharp.summary: Returns true if and only if two inputs are not nearly equal (that is, are not within a tolerance of 1e-12).
ms.openlocfilehash: 23229b1630982eba4485330cc2290aed733c4d86
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197149"
---
# <a name="notnearlyequald-function"></a><span data-ttu-id="1412f-102">Функция Нотнеарлекуалд</span><span class="sxs-lookup"><span data-stu-id="1412f-102">NotNearlyEqualD function</span></span>

<span data-ttu-id="1412f-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="1412f-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="1412f-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1412f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1412f-105">Возвращает значение true только в том случае, если два входных значения не почти равны (то есть не находятся в пределах допустимого диапазона 1E-12).</span><span class="sxs-lookup"><span data-stu-id="1412f-105">Returns true if and only if two inputs are not nearly equal (that is, are not within a tolerance of 1e-12).</span></span>

```qsharp
function NotNearlyEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="1412f-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="1412f-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="1412f-107">ответ. [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="1412f-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="1412f-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="1412f-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="1412f-109">б: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="1412f-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="1412f-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="1412f-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="1412f-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="1412f-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="1412f-112">`true` Если и, только если `a` не равно `b` .</span><span class="sxs-lookup"><span data-stu-id="1412f-112">`true` if and only if `a` is not nearly equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="1412f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1412f-113">Remarks</span></span>

<span data-ttu-id="1412f-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="1412f-114">The following are equivalent:</span></span>

```Q#
let cond = Microsoft.Quantum.Math.AbsD(a - b) >= 1e-12;
let cond = NotNearlyEqualD(a, b);
```