---
uid: Microsoft.Quantum.Math.GreatestCommonDivisorL
title: Функция Греатесткоммондивисорл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: GreatestCommonDivisorL
qsharp.summary: Computes the greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: 1bd18758bb2dea8a4801cbfdf258d91f81c5d9a4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96195517"
---
# <a name="greatestcommondivisorl-function"></a><span data-ttu-id="5ae20-102">Функция Греатесткоммондивисорл</span><span class="sxs-lookup"><span data-stu-id="5ae20-102">GreatestCommonDivisorL function</span></span>

<span data-ttu-id="5ae20-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="5ae20-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="5ae20-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5ae20-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5ae20-105">Вычисление наибольшего общего делителя $a $ и $b $.</span><span class="sxs-lookup"><span data-stu-id="5ae20-105">Computes the greatest common divisor of $a$ and $b$.</span></span> <span data-ttu-id="5ae20-106">GCD всегда имеет положительное значение.</span><span class="sxs-lookup"><span data-stu-id="5ae20-106">The GCD is always positive.</span></span>

```qsharp
function GreatestCommonDivisorL (a : BigInt, b : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="5ae20-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5ae20-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="5ae20-108">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="5ae20-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="5ae20-109">Первое число, для которого вычисляются расширенные наибольшие общие делительы</span><span class="sxs-lookup"><span data-stu-id="5ae20-109">the first number of which extended greatest common divisor is being computed</span></span>


### <a name="b--bigint"></a><span data-ttu-id="5ae20-110">б: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="5ae20-110">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="5ae20-111">второе число, для которого вычисляются расширенные наибольшие общие делительы</span><span class="sxs-lookup"><span data-stu-id="5ae20-111">the second number of which extended greatest common divisor is being computed</span></span>



## <a name="output--bigint"></a><span data-ttu-id="5ae20-112">Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="5ae20-112">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="5ae20-113">Наибольший общий делитель $a $ и $b $</span><span class="sxs-lookup"><span data-stu-id="5ae20-113">Greatest common divisor of $a$ and $b$</span></span>