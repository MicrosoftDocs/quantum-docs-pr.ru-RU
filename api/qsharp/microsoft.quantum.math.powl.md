---
uid: Microsoft.Quantum.Math.PowL
title: Функция Повл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PowL
qsharp.summary: Returns a number raised to a given power.
ms.openlocfilehash: b3207d1854f6b69cdb5b68d354000a0b6746c0c2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228327"
---
# <a name="powl-function"></a><span data-ttu-id="5ed9e-102">Функция Повл</span><span class="sxs-lookup"><span data-stu-id="5ed9e-102">PowL function</span></span>

<span data-ttu-id="5ed9e-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="5ed9e-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="5ed9e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5ed9e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5ed9e-105">Возвращает число, возведенное в заданную степень.</span><span class="sxs-lookup"><span data-stu-id="5ed9e-105">Returns a number raised to a given power.</span></span>

```qsharp
function PowL (a : BigInt, power : Int) : BigInt
```


## <a name="input"></a><span data-ttu-id="5ed9e-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5ed9e-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="5ed9e-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="5ed9e-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="5ed9e-108">Число $a $, которое должно быть выдано.</span><span class="sxs-lookup"><span data-stu-id="5ed9e-108">The number $a$ that is to be raised.</span></span>


### <a name="power--int"></a><span data-ttu-id="5ed9e-109">степень: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5ed9e-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5ed9e-110">$B $, до которой должно быть создано $a $.</span><span class="sxs-lookup"><span data-stu-id="5ed9e-110">The power $b$ to which $a$ should be raised.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="5ed9e-111">Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="5ed9e-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="5ed9e-112">$a питания ^ b $</span><span class="sxs-lookup"><span data-stu-id="5ed9e-112">The power $a^b$</span></span>