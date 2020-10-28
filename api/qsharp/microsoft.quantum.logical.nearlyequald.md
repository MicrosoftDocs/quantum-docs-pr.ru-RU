---
uid: Microsoft.Quantum.Logical.NearlyEqualD
title: Функция Неарлекуалд
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NearlyEqualD
qsharp.summary: Returns true if and only if two inputs are nearly equal (that is, within a tolerance of 1e-12).
ms.openlocfilehash: 332f9ea1753b539eba7b931d5b948b2a238d1abf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709868"
---
# <a name="nearlyequald-function"></a><span data-ttu-id="80744-102">Функция Неарлекуалд</span><span class="sxs-lookup"><span data-stu-id="80744-102">NearlyEqualD function</span></span>

<span data-ttu-id="80744-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="80744-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="80744-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="80744-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="80744-105">Возвращает значение true только в том случае, если два входных значения почти равны (то есть в пределах допустимого диапазона 1E-12).</span><span class="sxs-lookup"><span data-stu-id="80744-105">Returns true if and only if two inputs are nearly equal (that is, within a tolerance of 1e-12).</span></span>

```qsharp
function NearlyEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="80744-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="80744-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="80744-107">ответ. [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="80744-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="80744-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="80744-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="80744-109">б: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="80744-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="80744-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="80744-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="80744-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="80744-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="80744-112">`true` Если и, только если `a` почти равно `b` .</span><span class="sxs-lookup"><span data-stu-id="80744-112">`true` if and only if `a` is nearly equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="80744-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="80744-113">Remarks</span></span>

<span data-ttu-id="80744-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="80744-114">The following are equivalent:</span></span>

```Q#
let cond = Microsoft.Quantum.Math.AbsD(a - b) < 1e-12;
let cond = NearlyEqualD(a, b);
```