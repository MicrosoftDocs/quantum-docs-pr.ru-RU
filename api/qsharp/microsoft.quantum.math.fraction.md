---
uid: Microsoft.Quantum.Math.Fraction
title: Определяемый пользователем тип дроби
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: Fraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: 1838bb2b605b109742948ec0633b08ca01baea98
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210681"
---
# <a name="fraction-user-defined-type"></a><span data-ttu-id="dd69d-102">Определяемый пользователем тип дроби</span><span class="sxs-lookup"><span data-stu-id="dd69d-102">Fraction user defined type</span></span>

<span data-ttu-id="dd69d-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="dd69d-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="dd69d-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="dd69d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="dd69d-105">Представляет рациональное число в форме `p/q` .</span><span class="sxs-lookup"><span data-stu-id="dd69d-105">Represents a rational number of the form `p/q`.</span></span> <span data-ttu-id="dd69d-106">Integer `p` — это первый элемент кортежа, который `q` является вторым элементом кортежа.</span><span class="sxs-lookup"><span data-stu-id="dd69d-106">Integer `p` is the first element of the tuple and `q` is the second element of the tuple.</span></span>

```qsharp

newtype Fraction = (Numerator : Int, Denominator : Int);
```



## <a name="named-items"></a><span data-ttu-id="dd69d-107">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="dd69d-107">Named Items</span></span>

### <a name="numerator--int"></a><span data-ttu-id="dd69d-108">Числитель: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="dd69d-108">Numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="dd69d-109">Числитель дробной части.</span><span class="sxs-lookup"><span data-stu-id="dd69d-109">Numerator of the fraction.</span></span>
### <a name="denominator--int"></a><span data-ttu-id="dd69d-110">Знаменатель: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="dd69d-110">Denominator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="dd69d-111">Знаменатель дроби/</span><span class="sxs-lookup"><span data-stu-id="dd69d-111">Denominator of the fraction/</span></span>