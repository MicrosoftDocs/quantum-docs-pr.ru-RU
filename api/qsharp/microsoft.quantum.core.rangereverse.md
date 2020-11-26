---
uid: Microsoft.Quantum.Core.RangeReverse
title: Функция Ранжереверсе
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeReverse
qsharp.summary: Returns a new range which is the reverse of the input range.
ms.openlocfilehash: 7bd7c55abe0b56b9d30b4c6e91f7175101dd2948
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96213843"
---
# <a name="rangereverse-function"></a><span data-ttu-id="dd332-102">Функция Ранжереверсе</span><span class="sxs-lookup"><span data-stu-id="dd332-102">RangeReverse function</span></span>

<span data-ttu-id="dd332-103">Пространство имен: [Microsoft. тактов. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="dd332-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="dd332-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="dd332-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="dd332-105">Возвращает новый диапазон, являющийся обратным по отношению к входному диапазону.</span><span class="sxs-lookup"><span data-stu-id="dd332-105">Returns a new range which is the reverse of the input range.</span></span>

```qsharp
function RangeReverse (r : Range) : Range
```


## <a name="input"></a><span data-ttu-id="dd332-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="dd332-106">Input</span></span>

### <a name="r--range"></a><span data-ttu-id="dd332-107">r: [диапазон](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="dd332-107">r : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="dd332-108">Входной диапазон.</span><span class="sxs-lookup"><span data-stu-id="dd332-108">Input range.</span></span>



## <a name="output--range"></a><span data-ttu-id="dd332-109">Выходные данные: [диапазон](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="dd332-109">Output : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="dd332-110">Новый диапазон, являющийся обратным по отношению к заданному диапазону.</span><span class="sxs-lookup"><span data-stu-id="dd332-110">A new range that is the reverse of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd332-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd332-111">Remarks</span></span>

<span data-ttu-id="dd332-112">Обратите внимание, что обратная часть диапазона не просто `end` .. `-step` .. `start` , поскольку фактический последний элемент диапазона может не совпадать с `end` .</span><span class="sxs-lookup"><span data-stu-id="dd332-112">Note that the reverse of a range is not simply `end`..`-step`..`start`, because the actual last element of a range may not be the same as `end`.</span></span>