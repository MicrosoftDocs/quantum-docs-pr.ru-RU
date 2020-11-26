---
uid: Microsoft.Quantum.Logical.EqualB
title: Функция Екуалб
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualB
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: b566f5ba8548eadeecf63a1e91956d936e7e9a20
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198475"
---
# <a name="equalb-function"></a><span data-ttu-id="64ba9-102">Функция Екуалб</span><span class="sxs-lookup"><span data-stu-id="64ba9-102">EqualB function</span></span>

<span data-ttu-id="64ba9-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="64ba9-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="64ba9-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="64ba9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="64ba9-105">Возвращает значение true только в том случае, если два входных значения равны.</span><span class="sxs-lookup"><span data-stu-id="64ba9-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="64ba9-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="64ba9-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="64ba9-107">ответ. [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="64ba9-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="64ba9-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="64ba9-108">The first value to be compared.</span></span>


### <a name="b--bool"></a><span data-ttu-id="64ba9-109">б: [логическое](xref:microsoft.quantum.lang-ref.bool) значение</span><span class="sxs-lookup"><span data-stu-id="64ba9-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="64ba9-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="64ba9-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="64ba9-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="64ba9-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="64ba9-112">`true` Если и, только если `a` равно `b` .</span><span class="sxs-lookup"><span data-stu-id="64ba9-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="64ba9-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="64ba9-113">Remarks</span></span>

<span data-ttu-id="64ba9-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="64ba9-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualB(a, b);
```