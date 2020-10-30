---
uid: Microsoft.Quantum.Math.BigFraction
title: Определяемый пользователем тип Бигфрактион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BigFraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: a8daa54947097b95040a2dfa7a4d1b90bfaff856
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732768"
---
# <a name="bigfraction-user-defined-type"></a><span data-ttu-id="613f2-102">Определяемый пользователем тип Бигфрактион</span><span class="sxs-lookup"><span data-stu-id="613f2-102">BigFraction user defined type</span></span>

<span data-ttu-id="613f2-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="613f2-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="613f2-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="613f2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="613f2-105">Представляет рациональное число в форме `p/q` .</span><span class="sxs-lookup"><span data-stu-id="613f2-105">Represents a rational number of the form `p/q`.</span></span> <span data-ttu-id="613f2-106">Integer `p` — это первый элемент кортежа, который `q` является вторым элементом кортежа.</span><span class="sxs-lookup"><span data-stu-id="613f2-106">Integer `p` is the first element of the tuple and `q` is the second element of the tuple.</span></span>

```qsharp

newtype BigFraction = (Numerator : BigInt, Denominator : BigInt);
```



## <a name="named-items"></a><span data-ttu-id="613f2-107">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="613f2-107">Named Items</span></span>

### <a name="numerator--bigint"></a><span data-ttu-id="613f2-108">Числитель: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="613f2-108">Numerator : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="613f2-109">Числитель дробной части.</span><span class="sxs-lookup"><span data-stu-id="613f2-109">Numerator of the fraction.</span></span>
### <a name="denominator--bigint"></a><span data-ttu-id="613f2-110">Знаменатель: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="613f2-110">Denominator : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="613f2-111">Знаменатель дроби/</span><span class="sxs-lookup"><span data-stu-id="613f2-111">Denominator of the fraction/</span></span>