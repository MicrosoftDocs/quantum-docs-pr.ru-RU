---
uid: Microsoft.Quantum.Math.PowL
title: Функция Повл
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PowL
qsharp.summary: Returns a number raised to a given power.
ms.openlocfilehash: 22c05cf85acf691490049ce9ac27a7c6b2a4899e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733648"
---
# <a name="powl-function"></a><span data-ttu-id="7de05-102">Функция Повл</span><span class="sxs-lookup"><span data-stu-id="7de05-102">PowL function</span></span>

<span data-ttu-id="7de05-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="7de05-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="7de05-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7de05-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7de05-105">Возвращает число, возведенное в заданную степень.</span><span class="sxs-lookup"><span data-stu-id="7de05-105">Returns a number raised to a given power.</span></span>

```qsharp
function PowL (a : BigInt, power : Int) : BigInt
```


## <a name="input"></a><span data-ttu-id="7de05-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7de05-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="7de05-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="7de05-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="7de05-108">Число $a $, которое должно быть выдано.</span><span class="sxs-lookup"><span data-stu-id="7de05-108">The number $a$ that is to be raised.</span></span>


### <a name="power--int"></a><span data-ttu-id="7de05-109">степень: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7de05-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7de05-110">$B $, до которой должно быть создано $a $.</span><span class="sxs-lookup"><span data-stu-id="7de05-110">The power $b$ to which $a$ should be raised.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="7de05-111">Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="7de05-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="7de05-112">$a питания ^ b $</span><span class="sxs-lookup"><span data-stu-id="7de05-112">The power $a^b$</span></span>