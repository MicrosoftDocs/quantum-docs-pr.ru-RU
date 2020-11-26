---
uid: Microsoft.Quantum.Logical.Not
title: Not, функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Not
qsharp.summary: Returns the Boolean negation of a value.
ms.openlocfilehash: f2db43f4a2ce83d8cad1d60aa8c481a33b0c7d44
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197455"
---
# <a name="not-function"></a><span data-ttu-id="4fb56-102">Not, функция</span><span class="sxs-lookup"><span data-stu-id="4fb56-102">Not function</span></span>

<span data-ttu-id="4fb56-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="4fb56-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="4fb56-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4fb56-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4fb56-105">Возвращает логическое отрицание значения.</span><span class="sxs-lookup"><span data-stu-id="4fb56-105">Returns the Boolean negation of a value.</span></span>

```qsharp
function Not (value : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="4fb56-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4fb56-106">Input</span></span>

### <a name="value--bool"></a><span data-ttu-id="4fb56-107">значение: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="4fb56-107">value : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="4fb56-108">Значение, которое необходимо инвертировать.</span><span class="sxs-lookup"><span data-stu-id="4fb56-108">The value to be negated.</span></span>



## <a name="output--bool"></a><span data-ttu-id="4fb56-109">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="4fb56-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="4fb56-110">`true` Если и только если `value` имеет значение `false` .</span><span class="sxs-lookup"><span data-stu-id="4fb56-110">`true` if and only if `value` is `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fb56-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4fb56-111">Remarks</span></span>

<span data-ttu-id="4fb56-112">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="4fb56-112">The following are equivalent:</span></span>

```Q#
let x = not value;
let x = Not(value);
```