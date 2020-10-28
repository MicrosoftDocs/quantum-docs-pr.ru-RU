---
uid: Microsoft.Quantum.Logical.NotNearlyEqualD
title: Функция Нотнеарлекуалд
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotNearlyEqualD
qsharp.summary: Returns true if and only if two inputs are not nearly equal (that is, are not within a tolerance of 1e-12).
ms.openlocfilehash: d9e4cc5b0cfba3989ae64e494d0daa52069718a4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731256"
---
# <a name="notnearlyequald-function"></a><span data-ttu-id="f1c44-102">Функция Нотнеарлекуалд</span><span class="sxs-lookup"><span data-stu-id="f1c44-102">NotNearlyEqualD function</span></span>

<span data-ttu-id="f1c44-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="f1c44-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="f1c44-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f1c44-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f1c44-105">Возвращает значение true только в том случае, если два входных значения не почти равны (то есть не находятся в пределах допустимого диапазона 1E-12).</span><span class="sxs-lookup"><span data-stu-id="f1c44-105">Returns true if and only if two inputs are not nearly equal (that is, are not within a tolerance of 1e-12).</span></span>

```qsharp
function NotNearlyEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="f1c44-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f1c44-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="f1c44-107">ответ. [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f1c44-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f1c44-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="f1c44-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="f1c44-109">б: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f1c44-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f1c44-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="f1c44-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="f1c44-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f1c44-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f1c44-112">`true` Если и, только если `a` не равно `b` .</span><span class="sxs-lookup"><span data-stu-id="f1c44-112">`true` if and only if `a` is not nearly equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1c44-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="f1c44-113">Remarks</span></span>

<span data-ttu-id="f1c44-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="f1c44-114">The following are equivalent:</span></span>

```Q#
let cond = Microsoft.Quantum.Math.AbsD(a - b) >= 1e-12;
let cond = NotNearlyEqualD(a, b);
```