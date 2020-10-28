---
uid: Microsoft.Quantum.Logical.EqualB
title: Функция Екуалб
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualB
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 91ab51180018a9b95a2f9010477c0a24f3a54617
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731289"
---
# <a name="equalb-function"></a><span data-ttu-id="a9fe7-102">Функция Екуалб</span><span class="sxs-lookup"><span data-stu-id="a9fe7-102">EqualB function</span></span>

<span data-ttu-id="a9fe7-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="a9fe7-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="a9fe7-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a9fe7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a9fe7-105">Возвращает значение true только в том случае, если два входных значения равны.</span><span class="sxs-lookup"><span data-stu-id="a9fe7-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="a9fe7-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a9fe7-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="a9fe7-107">ответ. [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a9fe7-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a9fe7-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="a9fe7-108">The first value to be compared.</span></span>


### <a name="b--bool"></a><span data-ttu-id="a9fe7-109">б: [логическое](xref:microsoft.quantum.lang-ref.bool) значение</span><span class="sxs-lookup"><span data-stu-id="a9fe7-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a9fe7-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="a9fe7-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="a9fe7-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a9fe7-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a9fe7-112">`true` Если и, только если `a` равно `b` .</span><span class="sxs-lookup"><span data-stu-id="a9fe7-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9fe7-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="a9fe7-113">Remarks</span></span>

<span data-ttu-id="a9fe7-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="a9fe7-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualB(a, b);
```