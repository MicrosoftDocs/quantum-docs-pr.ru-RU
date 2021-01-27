---
uid: Microsoft.Quantum.Logical.EqualB
title: Функция Екуалб
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualB
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 2a15a749f52fe814db4fa57118f69c80fa22158a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98817257"
---
# <a name="equalb-function"></a><span data-ttu-id="02fe8-102">Функция Екуалб</span><span class="sxs-lookup"><span data-stu-id="02fe8-102">EqualB function</span></span>

<span data-ttu-id="02fe8-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="02fe8-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="02fe8-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="02fe8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="02fe8-105">Возвращает значение true только в том случае, если два входных значения равны.</span><span class="sxs-lookup"><span data-stu-id="02fe8-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="02fe8-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="02fe8-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="02fe8-107">ответ. [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="02fe8-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="02fe8-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="02fe8-108">The first value to be compared.</span></span>


### <a name="b--bool"></a><span data-ttu-id="02fe8-109">б: [логическое](xref:microsoft.quantum.lang-ref.bool) значение</span><span class="sxs-lookup"><span data-stu-id="02fe8-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="02fe8-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="02fe8-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="02fe8-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="02fe8-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="02fe8-112">`true` Если и, только если `a` равно `b` .</span><span class="sxs-lookup"><span data-stu-id="02fe8-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="02fe8-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="02fe8-113">Remarks</span></span>

<span data-ttu-id="02fe8-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="02fe8-114">The following are equivalent:</span></span>

```qsharp
let cond = a == b;
let cond = EqualB(a, b);
```