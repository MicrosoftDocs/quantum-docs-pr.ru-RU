---
uid: Microsoft.Quantum.Synthesis.DecomposedOn
title: Функция Декомпоседон
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecomposedOn
qsharp.summary: Decomposes a permutation on a variable
ms.openlocfilehash: b033723a50fb85e77c9d4baec1f94231327e9b25
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733913"
---
# <a name="decomposedon-function"></a><span data-ttu-id="60a2c-102">Функция Декомпоседон</span><span class="sxs-lookup"><span data-stu-id="60a2c-102">DecomposedOn function</span></span>

<span data-ttu-id="60a2c-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="60a2c-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="60a2c-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="60a2c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="60a2c-105">Разделяет перестановку на переменную</span><span class="sxs-lookup"><span data-stu-id="60a2c-105">Decomposes a permutation on a variable</span></span>

```qsharp
function DecomposedOn (perm : Int[], index : Int) : ((Int[], Int[]), Int[])
```


## <a name="description"></a><span data-ttu-id="60a2c-106">Описание</span><span class="sxs-lookup"><span data-stu-id="60a2c-106">Description</span></span>

<span data-ttu-id="60a2c-107">Учитывая перестановку $ \пи $ ( `perm` ) и индекс $i $ ( `index` ), этот метод возвращает три перестановки $ ((\ pi_l, \ pi_r), \пи ") $ таким, что изображения $ \ pi_l $ и $ \ pi_r $ не изменяют биты в своих элементах в индексах, отличных от $i $ и изображений $ \пи" $ не меняйте бит $i $ в своих элементах.</span><span class="sxs-lookup"><span data-stu-id="60a2c-107">Given a permutation $\pi$ (`perm`) and an index $i$ (`index`), this method returns three permutations $((\pi_l, \pi_r), \pi')$ such that the images of $\pi_l$ and $\pi_r$ do not change bits in their elements at indexes other than $i$ and images of $\pi'$ do not change bit $i$ in their elements.</span></span>

## <a name="input"></a><span data-ttu-id="60a2c-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="60a2c-108">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="60a2c-109">разрешение: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="60a2c-109">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="index--int"></a><span data-ttu-id="60a2c-110">Индекс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="60a2c-110">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--intintint"></a><span data-ttu-id="60a2c-111">Выходные данные: (([int](xref:microsoft.quantum.lang-ref.int)[],[int](xref:microsoft.quantum.lang-ref.int)[]),[int](xref:microsoft.quantum.lang-ref.int)[])</span><span class="sxs-lookup"><span data-stu-id="60a2c-111">Output : (([Int](xref:microsoft.quantum.lang-ref.int)[],[Int](xref:microsoft.quantum.lang-ref.int)[]),[Int](xref:microsoft.quantum.lang-ref.int)[])</span></span>

