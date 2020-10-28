---
uid: Microsoft.Quantum.Math.Fraction
title: Определяемый пользователем тип дроби
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: Fraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: 350d470c374fc8e0a3f4c4a9a68ad8566ab88727
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733024"
---
# <a name="fraction-user-defined-type"></a><span data-ttu-id="2568a-102">Определяемый пользователем тип дроби</span><span class="sxs-lookup"><span data-stu-id="2568a-102">Fraction user defined type</span></span>

<span data-ttu-id="2568a-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="2568a-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="2568a-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2568a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2568a-105">Представляет рациональное число в форме `p/q` .</span><span class="sxs-lookup"><span data-stu-id="2568a-105">Represents a rational number of the form `p/q`.</span></span> <span data-ttu-id="2568a-106">Integer `p` — это первый элемент кортежа, который `q` является вторым элементом кортежа.</span><span class="sxs-lookup"><span data-stu-id="2568a-106">Integer `p` is the first element of the tuple and `q` is the second element of the tuple.</span></span>

```qsharp

newtype Fraction = (Numerator : Int, Denominator : Int);
```



## <a name="named-items"></a><span data-ttu-id="2568a-107">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="2568a-107">Named Items</span></span>

### <a name="numerator--int"></a><span data-ttu-id="2568a-108">Числитель: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2568a-108">Numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2568a-109">Числитель дробной части.</span><span class="sxs-lookup"><span data-stu-id="2568a-109">Numerator of the fraction.</span></span>
### <a name="denominator--int"></a><span data-ttu-id="2568a-110">Знаменатель: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2568a-110">Denominator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2568a-111">Знаменатель дроби/</span><span class="sxs-lookup"><span data-stu-id="2568a-111">Denominator of the fraction/</span></span>