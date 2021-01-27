---
uid: Microsoft.Quantum.Logical.Not
title: Not, функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Not
qsharp.summary: Returns the Boolean negation of a value.
ms.openlocfilehash: bf09cac8d126371df6218b7e92d68a881b732dc8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849078"
---
# <a name="not-function"></a><span data-ttu-id="29a76-102">Not, функция</span><span class="sxs-lookup"><span data-stu-id="29a76-102">Not function</span></span>

<span data-ttu-id="29a76-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="29a76-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="29a76-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="29a76-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="29a76-105">Возвращает логическое отрицание значения.</span><span class="sxs-lookup"><span data-stu-id="29a76-105">Returns the Boolean negation of a value.</span></span>

```qsharp
function Not (value : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="29a76-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="29a76-106">Input</span></span>

### <a name="value--bool"></a><span data-ttu-id="29a76-107">значение: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="29a76-107">value : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="29a76-108">Значение, которое необходимо инвертировать.</span><span class="sxs-lookup"><span data-stu-id="29a76-108">The value to be negated.</span></span>



## <a name="output--bool"></a><span data-ttu-id="29a76-109">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="29a76-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="29a76-110">`true` Если и только если `value` имеет значение `false` .</span><span class="sxs-lookup"><span data-stu-id="29a76-110">`true` if and only if `value` is `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="29a76-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="29a76-111">Remarks</span></span>

<span data-ttu-id="29a76-112">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="29a76-112">The following are equivalent:</span></span>

```qsharp
let x = not value;
let x = Not(value);
```