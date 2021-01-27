---
uid: Microsoft.Quantum.Logical.EqualI
title: Функция Екуали
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualI
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 87cf00ea8bb738cda30092b3d80940291beb1fb9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98816754"
---
# <a name="equali-function"></a><span data-ttu-id="df3d1-102">Функция Екуали</span><span class="sxs-lookup"><span data-stu-id="df3d1-102">EqualI function</span></span>

<span data-ttu-id="df3d1-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="df3d1-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="df3d1-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="df3d1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="df3d1-105">Возвращает значение true только в том случае, если два входных значения равны.</span><span class="sxs-lookup"><span data-stu-id="df3d1-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="df3d1-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="df3d1-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="df3d1-107">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="df3d1-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="df3d1-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="df3d1-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="df3d1-109">б: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="df3d1-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="df3d1-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="df3d1-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="df3d1-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="df3d1-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="df3d1-112">`true` Если и, только если `a` равно `b` .</span><span class="sxs-lookup"><span data-stu-id="df3d1-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="df3d1-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="df3d1-113">Remarks</span></span>

<span data-ttu-id="df3d1-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="df3d1-114">The following are equivalent:</span></span>

```qsharp
let cond = a == b;
let cond = EqualI(a, b);
```