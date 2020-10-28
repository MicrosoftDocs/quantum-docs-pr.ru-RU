---
uid: Microsoft.Quantum.Logical.EqualD
title: Функция equaled
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualD
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 024ddee785a6a907b4a39d0eccc5990b4c5d5d83
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711394"
---
# <a name="equald-function"></a><span data-ttu-id="b76f7-102">Функция equaled</span><span class="sxs-lookup"><span data-stu-id="b76f7-102">EqualD function</span></span>

<span data-ttu-id="b76f7-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="b76f7-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="b76f7-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b76f7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b76f7-105">Возвращает значение true только в том случае, если два входных значения равны.</span><span class="sxs-lookup"><span data-stu-id="b76f7-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="b76f7-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b76f7-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="b76f7-107">ответ. [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b76f7-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b76f7-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="b76f7-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="b76f7-109">б: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b76f7-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b76f7-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="b76f7-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="b76f7-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="b76f7-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="b76f7-112">`true` Если и, только если `a` равно `b` .</span><span class="sxs-lookup"><span data-stu-id="b76f7-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="b76f7-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="b76f7-113">Remarks</span></span>

<span data-ttu-id="b76f7-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="b76f7-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualD(a, b);
```