---
uid: Microsoft.Quantum.Math.ExtendedGreatestCommonDivisorI
title: Функция Екстендедгреатесткоммондивисори
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExtendedGreatestCommonDivisorI
qsharp.summary: Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: 8cb21ae5052ae6c5a8aed8be71d6bd3d32034272
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733057"
---
# <a name="extendedgreatestcommondivisori-function"></a><span data-ttu-id="29100-102">Функция Екстендедгреатесткоммондивисори</span><span class="sxs-lookup"><span data-stu-id="29100-102">ExtendedGreatestCommonDivisorI function</span></span>

<span data-ttu-id="29100-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="29100-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="29100-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="29100-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="29100-105">Выполняет вычисление кортежа $ (u, v) $ таким, что $u \кдот a + v \кдот b = \Операторнаме{ГКД} (a, b) $, где $ \Операторнаме{ГКД} $ — $a $ наибольший общий делитель $a $ и $b $.</span><span class="sxs-lookup"><span data-stu-id="29100-105">Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$.</span></span> <span data-ttu-id="29100-106">GCD всегда имеет положительное значение.</span><span class="sxs-lookup"><span data-stu-id="29100-106">The GCD is always positive.</span></span>

```qsharp
function ExtendedGreatestCommonDivisorI (a : Int, b : Int) : (Int, Int)
```


## <a name="input"></a><span data-ttu-id="29100-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="29100-107">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="29100-108">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="29100-108">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="29100-109">Первое число, для которого вычисляются расширенные наибольшие общие делительы</span><span class="sxs-lookup"><span data-stu-id="29100-109">the first number of which extended greatest common divisor is being computed</span></span>


### <a name="b--int"></a><span data-ttu-id="29100-110">б: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="29100-110">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="29100-111">второе число, для которого вычисляются расширенные наибольшие общие делительы</span><span class="sxs-lookup"><span data-stu-id="29100-111">the second number of which extended greatest common divisor is being computed</span></span>



## <a name="output--intint"></a><span data-ttu-id="29100-112">Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="29100-112">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>

<span data-ttu-id="29100-113">Кортеж $ (u, v) $ со свойством $u \кдот + v \кдот b = \Операторнаме{ГКД} (a, b) $.</span><span class="sxs-lookup"><span data-stu-id="29100-113">Tuple $(u,v)$ with the property $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$.</span></span>

## <a name="references"></a><span data-ttu-id="29100-114">Ссылки</span><span class="sxs-lookup"><span data-stu-id="29100-114">References</span></span>

- <span data-ttu-id="29100-115">Эта реализация в соответствии с https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span><span class="sxs-lookup"><span data-stu-id="29100-115">This implementation is according to https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span></span>