---
uid: Microsoft.Quantum.Logical.NotEqualB
title: Функция Нотекуалб
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualB
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 7943411b662683df058213a9e4b8eb7c9329ff07
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197387"
---
# <a name="notequalb-function"></a><span data-ttu-id="3f165-102">Функция Нотекуалб</span><span class="sxs-lookup"><span data-stu-id="3f165-102">NotEqualB function</span></span>

<span data-ttu-id="3f165-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="3f165-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="3f165-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3f165-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3f165-105">Возвращает значение true только в том случае, если два входных значения не равны.</span><span class="sxs-lookup"><span data-stu-id="3f165-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="3f165-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3f165-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="3f165-107">ответ. [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="3f165-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="3f165-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="3f165-108">The first value to be compared.</span></span>


### <a name="b--bool"></a><span data-ttu-id="3f165-109">б: [логическое](xref:microsoft.quantum.lang-ref.bool) значение</span><span class="sxs-lookup"><span data-stu-id="3f165-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="3f165-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="3f165-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="3f165-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="3f165-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="3f165-112">`true` Если и, только если `a` не равно `b` .</span><span class="sxs-lookup"><span data-stu-id="3f165-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f165-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3f165-113">Remarks</span></span>

<span data-ttu-id="3f165-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="3f165-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualB(a, b);
```