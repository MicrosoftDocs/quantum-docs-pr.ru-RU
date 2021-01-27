---
uid: Microsoft.Quantum.Logical.EqualD
title: Функция equaled
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualD
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: f8a24d7bfb9b4f7b8b0e1f68a94bfb341716b024
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98816865"
---
# <a name="equald-function"></a><span data-ttu-id="2cc2c-102">Функция equaled</span><span class="sxs-lookup"><span data-stu-id="2cc2c-102">EqualD function</span></span>

<span data-ttu-id="2cc2c-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="2cc2c-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="2cc2c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2cc2c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2cc2c-105">Возвращает значение true только в том случае, если два входных значения равны.</span><span class="sxs-lookup"><span data-stu-id="2cc2c-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="2cc2c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2cc2c-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="2cc2c-107">ответ. [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2cc2c-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2cc2c-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="2cc2c-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="2cc2c-109">б: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2cc2c-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2cc2c-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="2cc2c-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="2cc2c-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="2cc2c-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="2cc2c-112">`true` Если и, только если `a` равно `b` .</span><span class="sxs-lookup"><span data-stu-id="2cc2c-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cc2c-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="2cc2c-113">Remarks</span></span>

<span data-ttu-id="2cc2c-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="2cc2c-114">The following are equivalent:</span></span>

```qsharp
let cond = a == b;
let cond = EqualD(a, b);
```