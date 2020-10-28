---
uid: Microsoft.Quantum.Math.GreatestCommonDivisorL
title: Функция Греатесткоммондивисорл
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: GreatestCommonDivisorL
qsharp.summary: Computes the greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: 77bdb040908e9a8af81dee09451a3582f7b7d159
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733016"
---
# <a name="greatestcommondivisorl-function"></a><span data-ttu-id="025c8-102">Функция Греатесткоммондивисорл</span><span class="sxs-lookup"><span data-stu-id="025c8-102">GreatestCommonDivisorL function</span></span>

<span data-ttu-id="025c8-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="025c8-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="025c8-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="025c8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="025c8-105">Вычисление наибольшего общего делителя $a $ и $b $.</span><span class="sxs-lookup"><span data-stu-id="025c8-105">Computes the greatest common divisor of $a$ and $b$.</span></span> <span data-ttu-id="025c8-106">GCD всегда имеет положительное значение.</span><span class="sxs-lookup"><span data-stu-id="025c8-106">The GCD is always positive.</span></span>

```qsharp
function GreatestCommonDivisorL (a : BigInt, b : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="025c8-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="025c8-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="025c8-108">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="025c8-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="025c8-109">Первое число, для которого вычисляются расширенные наибольшие общие делительы</span><span class="sxs-lookup"><span data-stu-id="025c8-109">the first number of which extended greatest common divisor is being computed</span></span>


### <a name="b--bigint"></a><span data-ttu-id="025c8-110">б: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="025c8-110">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="025c8-111">второе число, для которого вычисляются расширенные наибольшие общие делительы</span><span class="sxs-lookup"><span data-stu-id="025c8-111">the second number of which extended greatest common divisor is being computed</span></span>



## <a name="output--bigint"></a><span data-ttu-id="025c8-112">Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="025c8-112">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="025c8-113">Наибольший общий делитель $a $ и $b $</span><span class="sxs-lookup"><span data-stu-id="025c8-113">Greatest common divisor of $a$ and $b$</span></span>