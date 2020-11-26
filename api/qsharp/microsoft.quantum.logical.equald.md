---
uid: Microsoft.Quantum.Logical.EqualD
title: Функция equaled
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualD
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: d6731b293ba402f5cd43591d3c2bcd258e8ebe32
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198152"
---
# <a name="equald-function"></a><span data-ttu-id="8399d-102">Функция equaled</span><span class="sxs-lookup"><span data-stu-id="8399d-102">EqualD function</span></span>

<span data-ttu-id="8399d-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="8399d-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="8399d-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8399d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8399d-105">Возвращает значение true только в том случае, если два входных значения равны.</span><span class="sxs-lookup"><span data-stu-id="8399d-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="8399d-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8399d-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="8399d-107">ответ. [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8399d-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8399d-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="8399d-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="8399d-109">б: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8399d-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8399d-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="8399d-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="8399d-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="8399d-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="8399d-112">`true` Если и, только если `a` равно `b` .</span><span class="sxs-lookup"><span data-stu-id="8399d-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="8399d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8399d-113">Remarks</span></span>

<span data-ttu-id="8399d-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="8399d-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualD(a, b);
```