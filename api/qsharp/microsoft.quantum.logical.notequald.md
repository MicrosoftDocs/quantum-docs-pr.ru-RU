---
uid: Microsoft.Quantum.Logical.NotEqualD
title: Функция Нотекуалд
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualD
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 38f30309a4c27a5ef7e112a09a0efe3b5512d4e3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849052"
---
# <a name="notequald-function"></a><span data-ttu-id="fa6d7-102">Функция Нотекуалд</span><span class="sxs-lookup"><span data-stu-id="fa6d7-102">NotEqualD function</span></span>

<span data-ttu-id="fa6d7-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="fa6d7-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="fa6d7-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fa6d7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fa6d7-105">Возвращает значение true только в том случае, если два входных значения не равны.</span><span class="sxs-lookup"><span data-stu-id="fa6d7-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="fa6d7-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fa6d7-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="fa6d7-107">ответ. [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fa6d7-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fa6d7-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="fa6d7-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="fa6d7-109">б: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fa6d7-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fa6d7-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="fa6d7-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="fa6d7-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="fa6d7-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="fa6d7-112">`true` Если и, только если `a` не равно `b` .</span><span class="sxs-lookup"><span data-stu-id="fa6d7-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa6d7-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="fa6d7-113">Remarks</span></span>

<span data-ttu-id="fa6d7-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="fa6d7-114">The following are equivalent:</span></span>

```qsharp
let cond = a != b;
let cond = NotEqualD(a, b);
```