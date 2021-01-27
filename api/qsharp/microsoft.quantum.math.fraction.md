---
uid: Microsoft.Quantum.Math.Fraction
title: Определяемый пользователем тип дроби
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: Fraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: a56d28e34938729a8e4ffda5f870e0b6a25be017
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857516"
---
# <a name="fraction-user-defined-type"></a><span data-ttu-id="0fe89-102">Определяемый пользователем тип дроби</span><span class="sxs-lookup"><span data-stu-id="0fe89-102">Fraction user defined type</span></span>

<span data-ttu-id="0fe89-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="0fe89-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="0fe89-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0fe89-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0fe89-105">Представляет рациональное число в форме `p/q` .</span><span class="sxs-lookup"><span data-stu-id="0fe89-105">Represents a rational number of the form `p/q`.</span></span> <span data-ttu-id="0fe89-106">Integer `p` — это первый элемент кортежа, который `q` является вторым элементом кортежа.</span><span class="sxs-lookup"><span data-stu-id="0fe89-106">Integer `p` is the first element of the tuple and `q` is the second element of the tuple.</span></span>

```qsharp

newtype Fraction = (Numerator : Int, Denominator : Int);
```



## <a name="named-items"></a><span data-ttu-id="0fe89-107">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="0fe89-107">Named Items</span></span>

### <a name="numerator--int"></a><span data-ttu-id="0fe89-108">Числитель: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0fe89-108">Numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0fe89-109">Числитель дробной части.</span><span class="sxs-lookup"><span data-stu-id="0fe89-109">Numerator of the fraction.</span></span>
### <a name="denominator--int"></a><span data-ttu-id="0fe89-110">Знаменатель: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0fe89-110">Denominator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0fe89-111">Знаменатель дроби/</span><span class="sxs-lookup"><span data-stu-id="0fe89-111">Denominator of the fraction/</span></span>