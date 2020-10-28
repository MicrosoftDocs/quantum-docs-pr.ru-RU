---
uid: Microsoft.Quantum.Logical.NotEqualD
title: Функция Нотекуалд
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualD
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: dd21fcc1d0d73bd210303bfbf4f336386b912107
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732920"
---
# <a name="notequald-function"></a><span data-ttu-id="977d1-102">Функция Нотекуалд</span><span class="sxs-lookup"><span data-stu-id="977d1-102">NotEqualD function</span></span>

<span data-ttu-id="977d1-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="977d1-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="977d1-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="977d1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="977d1-105">Возвращает значение true только в том случае, если два входных значения не равны.</span><span class="sxs-lookup"><span data-stu-id="977d1-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="977d1-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="977d1-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="977d1-107">ответ. [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="977d1-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="977d1-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="977d1-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="977d1-109">б: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="977d1-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="977d1-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="977d1-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="977d1-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="977d1-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="977d1-112">`true` Если и, только если `a` не равно `b` .</span><span class="sxs-lookup"><span data-stu-id="977d1-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="977d1-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="977d1-113">Remarks</span></span>

<span data-ttu-id="977d1-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="977d1-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualD(a, b);
```