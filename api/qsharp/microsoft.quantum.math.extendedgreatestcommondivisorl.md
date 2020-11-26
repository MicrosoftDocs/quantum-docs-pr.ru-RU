---
uid: Microsoft.Quantum.Math.ExtendedGreatestCommonDivisorL
title: Функция Екстендедгреатесткоммондивисорл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExtendedGreatestCommonDivisorL
qsharp.summary: Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: abbbd367859952180f181a245ca0754646529b18
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210715"
---
# <a name="extendedgreatestcommondivisorl-function"></a><span data-ttu-id="65840-102">Функция Екстендедгреатесткоммондивисорл</span><span class="sxs-lookup"><span data-stu-id="65840-102">ExtendedGreatestCommonDivisorL function</span></span>

<span data-ttu-id="65840-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="65840-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="65840-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="65840-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="65840-105">Выполняет вычисление кортежа $ (u, v) $ таким, что $u \кдот a + v \кдот b = \Операторнаме{ГКД} (a, b) $, где $ \Операторнаме{ГКД} $ — $a $ наибольший общий делитель $a $ и $b $.</span><span class="sxs-lookup"><span data-stu-id="65840-105">Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$.</span></span> <span data-ttu-id="65840-106">GCD всегда имеет положительное значение.</span><span class="sxs-lookup"><span data-stu-id="65840-106">The GCD is always positive.</span></span>

```qsharp
function ExtendedGreatestCommonDivisorL (a : BigInt, b : BigInt) : (BigInt, BigInt)
```


## <a name="input"></a><span data-ttu-id="65840-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="65840-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="65840-108">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="65840-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="65840-109">Первое число, для которого вычисляются расширенные наибольшие общие делительы</span><span class="sxs-lookup"><span data-stu-id="65840-109">the first number of which extended greatest common divisor is being computed</span></span>


### <a name="b--bigint"></a><span data-ttu-id="65840-110">б: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="65840-110">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="65840-111">второе число, для которого вычисляются расширенные наибольшие общие делительы</span><span class="sxs-lookup"><span data-stu-id="65840-111">the second number of which extended greatest common divisor is being computed</span></span>



## <a name="output--bigintbigint"></a><span data-ttu-id="65840-112">Выходные данные: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[bigint](xref:microsoft.quantum.lang-ref.bigint))</span><span class="sxs-lookup"><span data-stu-id="65840-112">Output : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[BigInt](xref:microsoft.quantum.lang-ref.bigint))</span></span>

<span data-ttu-id="65840-113">Кортеж $ (u, v) $ со свойством $u \кдот + v \кдот b = \Операторнаме{ГКД} (a, b) $.</span><span class="sxs-lookup"><span data-stu-id="65840-113">Tuple $(u,v)$ with the property $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$.</span></span>

## <a name="references"></a><span data-ttu-id="65840-114">Ссылки</span><span class="sxs-lookup"><span data-stu-id="65840-114">References</span></span>

- <span data-ttu-id="65840-115">Эта реализация в соответствии с https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span><span class="sxs-lookup"><span data-stu-id="65840-115">This implementation is according to https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span></span>