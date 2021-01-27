---
uid: Microsoft.Quantum.Math.BigFraction
title: Определяемый пользователем тип Бигфрактион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BigFraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: bfbf49e7a3d060417e506a1977c20adc08b81f0e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846906"
---
# <a name="bigfraction-user-defined-type"></a><span data-ttu-id="e549a-102">Определяемый пользователем тип Бигфрактион</span><span class="sxs-lookup"><span data-stu-id="e549a-102">BigFraction user defined type</span></span>

<span data-ttu-id="e549a-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="e549a-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="e549a-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e549a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e549a-105">Представляет рациональное число в форме `p/q` .</span><span class="sxs-lookup"><span data-stu-id="e549a-105">Represents a rational number of the form `p/q`.</span></span> <span data-ttu-id="e549a-106">Integer `p` — это первый элемент кортежа, который `q` является вторым элементом кортежа.</span><span class="sxs-lookup"><span data-stu-id="e549a-106">Integer `p` is the first element of the tuple and `q` is the second element of the tuple.</span></span>

```qsharp

newtype BigFraction = (Numerator : BigInt, Denominator : BigInt);
```



## <a name="named-items"></a><span data-ttu-id="e549a-107">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="e549a-107">Named Items</span></span>

### <a name="numerator--bigint"></a><span data-ttu-id="e549a-108">Числитель: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="e549a-108">Numerator : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="e549a-109">Числитель дробной части.</span><span class="sxs-lookup"><span data-stu-id="e549a-109">Numerator of the fraction.</span></span>
### <a name="denominator--bigint"></a><span data-ttu-id="e549a-110">Знаменатель: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="e549a-110">Denominator : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="e549a-111">Знаменатель дроби/</span><span class="sxs-lookup"><span data-stu-id="e549a-111">Denominator of the fraction/</span></span>