---
uid: Microsoft.Quantum.Math.BigFraction
title: Определяемый пользователем тип Бигфрактион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BigFraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: 1c9b9e350c4fa3664b2c66da05149005b1170ec3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211089"
---
# <a name="bigfraction-user-defined-type"></a><span data-ttu-id="d1f46-102">Определяемый пользователем тип Бигфрактион</span><span class="sxs-lookup"><span data-stu-id="d1f46-102">BigFraction user defined type</span></span>

<span data-ttu-id="d1f46-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="d1f46-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="d1f46-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d1f46-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d1f46-105">Представляет рациональное число в форме `p/q` .</span><span class="sxs-lookup"><span data-stu-id="d1f46-105">Represents a rational number of the form `p/q`.</span></span> <span data-ttu-id="d1f46-106">Integer `p` — это первый элемент кортежа, который `q` является вторым элементом кортежа.</span><span class="sxs-lookup"><span data-stu-id="d1f46-106">Integer `p` is the first element of the tuple and `q` is the second element of the tuple.</span></span>

```qsharp

newtype BigFraction = (Numerator : BigInt, Denominator : BigInt);
```



## <a name="named-items"></a><span data-ttu-id="d1f46-107">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="d1f46-107">Named Items</span></span>

### <a name="numerator--bigint"></a><span data-ttu-id="d1f46-108">Числитель: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="d1f46-108">Numerator : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="d1f46-109">Числитель дробной части.</span><span class="sxs-lookup"><span data-stu-id="d1f46-109">Numerator of the fraction.</span></span>
### <a name="denominator--bigint"></a><span data-ttu-id="d1f46-110">Знаменатель: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="d1f46-110">Denominator : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="d1f46-111">Знаменатель дроби/</span><span class="sxs-lookup"><span data-stu-id="d1f46-111">Denominator of the fraction/</span></span>