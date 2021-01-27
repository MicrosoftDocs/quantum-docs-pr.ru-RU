---
uid: Microsoft.Quantum.Logical.NotEqualI
title: Функция Нотекуали
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualI
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: f88ae08f45c284f65151419c214705c74c3fadac
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814502"
---
# <a name="notequali-function"></a><span data-ttu-id="3a35e-102">Функция Нотекуали</span><span class="sxs-lookup"><span data-stu-id="3a35e-102">NotEqualI function</span></span>

<span data-ttu-id="3a35e-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="3a35e-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="3a35e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3a35e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3a35e-105">Возвращает значение true только в том случае, если два входных значения не равны.</span><span class="sxs-lookup"><span data-stu-id="3a35e-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="3a35e-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3a35e-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="3a35e-107">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3a35e-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3a35e-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="3a35e-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="3a35e-109">б: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3a35e-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3a35e-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="3a35e-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="3a35e-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="3a35e-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="3a35e-112">`true` Если и, только если `a` не равно `b` .</span><span class="sxs-lookup"><span data-stu-id="3a35e-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a35e-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="3a35e-113">Remarks</span></span>

<span data-ttu-id="3a35e-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="3a35e-114">The following are equivalent:</span></span>

```qsharp
let cond = a != b;
let cond = NotEqualI(a, b);
```