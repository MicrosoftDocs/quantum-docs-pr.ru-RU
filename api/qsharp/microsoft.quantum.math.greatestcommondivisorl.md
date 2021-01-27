---
uid: Microsoft.Quantum.Math.GreatestCommonDivisorL
title: Функция Греатесткоммондивисорл
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: GreatestCommonDivisorL
qsharp.summary: Computes the greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: 0f545f7888f5a9a353cc6000a12988648ac82dd8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856378"
---
# <a name="greatestcommondivisorl-function"></a><span data-ttu-id="fe093-102">Функция Греатесткоммондивисорл</span><span class="sxs-lookup"><span data-stu-id="fe093-102">GreatestCommonDivisorL function</span></span>

<span data-ttu-id="fe093-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="fe093-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="fe093-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fe093-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fe093-105">Вычисление наибольшего общего делителя $a $ и $b $.</span><span class="sxs-lookup"><span data-stu-id="fe093-105">Computes the greatest common divisor of $a$ and $b$.</span></span> <span data-ttu-id="fe093-106">GCD всегда имеет положительное значение.</span><span class="sxs-lookup"><span data-stu-id="fe093-106">The GCD is always positive.</span></span>

```qsharp
function GreatestCommonDivisorL (a : BigInt, b : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="fe093-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fe093-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="fe093-108">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="fe093-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="fe093-109">Первое число, для которого вычисляются расширенные наибольшие общие делительы</span><span class="sxs-lookup"><span data-stu-id="fe093-109">the first number of which extended greatest common divisor is being computed</span></span>


### <a name="b--bigint"></a><span data-ttu-id="fe093-110">б: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="fe093-110">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="fe093-111">второе число, для которого вычисляются расширенные наибольшие общие делительы</span><span class="sxs-lookup"><span data-stu-id="fe093-111">the second number of which extended greatest common divisor is being computed</span></span>



## <a name="output--bigint"></a><span data-ttu-id="fe093-112">Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="fe093-112">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="fe093-113">Наибольший общий делитель $a $ и $b $</span><span class="sxs-lookup"><span data-stu-id="fe093-113">Greatest common divisor of $a$ and $b$</span></span>