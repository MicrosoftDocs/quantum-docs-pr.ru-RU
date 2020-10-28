---
uid: Microsoft.Quantum.Logical.Not
title: Not, функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Not
qsharp.summary: Returns the Boolean negation of a value.
ms.openlocfilehash: 3a688aac0178a2f4127496c1009fe7d5ee7ae198
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709867"
---
# <a name="not-function"></a><span data-ttu-id="8a53e-102">Not, функция</span><span class="sxs-lookup"><span data-stu-id="8a53e-102">Not function</span></span>

<span data-ttu-id="8a53e-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="8a53e-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="8a53e-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8a53e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8a53e-105">Возвращает логическое отрицание значения.</span><span class="sxs-lookup"><span data-stu-id="8a53e-105">Returns the Boolean negation of a value.</span></span>

```qsharp
function Not (value : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="8a53e-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8a53e-106">Input</span></span>

### <a name="value--bool"></a><span data-ttu-id="8a53e-107">значение: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="8a53e-107">value : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="8a53e-108">Значение, которое необходимо инвертировать.</span><span class="sxs-lookup"><span data-stu-id="8a53e-108">The value to be negated.</span></span>



## <a name="output--bool"></a><span data-ttu-id="8a53e-109">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="8a53e-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="8a53e-110">`true` Если и только если `value` имеет значение `false` .</span><span class="sxs-lookup"><span data-stu-id="8a53e-110">`true` if and only if `value` is `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a53e-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="8a53e-111">Remarks</span></span>

<span data-ttu-id="8a53e-112">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="8a53e-112">The following are equivalent:</span></span>

```Q#
let x = not value;
let x = Not(value);
```