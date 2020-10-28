---
uid: Microsoft.Quantum.Core.RangeReverse
title: Функция Ранжереверсе
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeReverse
qsharp.summary: Returns a new range which is the reverse of the input range.
ms.openlocfilehash: d4e612d2f175015b7193634aeec12f9df12df7d3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713228"
---
# <a name="rangereverse-function"></a><span data-ttu-id="2ec0a-102">Функция Ранжереверсе</span><span class="sxs-lookup"><span data-stu-id="2ec0a-102">RangeReverse function</span></span>

<span data-ttu-id="2ec0a-103">Пространство имен: [Microsoft. тактов. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="2ec0a-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="2ec0a-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2ec0a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2ec0a-105">Возвращает новый диапазон, являющийся обратным по отношению к входному диапазону.</span><span class="sxs-lookup"><span data-stu-id="2ec0a-105">Returns a new range which is the reverse of the input range.</span></span>

```qsharp
function RangeReverse (r : Range) : Range
```


## <a name="input"></a><span data-ttu-id="2ec0a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2ec0a-106">Input</span></span>

### <a name="r--range"></a><span data-ttu-id="2ec0a-107">r: [диапазон](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="2ec0a-107">r : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="2ec0a-108">Входной диапазон.</span><span class="sxs-lookup"><span data-stu-id="2ec0a-108">Input range.</span></span>



## <a name="output--range"></a><span data-ttu-id="2ec0a-109">Выходные данные: [диапазон](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="2ec0a-109">Output : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="2ec0a-110">Новый диапазон, являющийся обратным по отношению к заданному диапазону.</span><span class="sxs-lookup"><span data-stu-id="2ec0a-110">A new range that is the reverse of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ec0a-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="2ec0a-111">Remarks</span></span>

<span data-ttu-id="2ec0a-112">Обратите внимание, что обратная часть диапазона не просто `end` .. `-step` .. `start` , поскольку фактический последний элемент диапазона может не совпадать с `end` .</span><span class="sxs-lookup"><span data-stu-id="2ec0a-112">Note that the reverse of a range is not simply `end`..`-step`..`start`, because the actual last element of a range may not be the same as `end`.</span></span>