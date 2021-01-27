---
uid: Microsoft.Quantum.Math.PowL
title: Функция Повл
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PowL
qsharp.summary: Returns a number raised to a given power.
ms.openlocfilehash: f7282a3639ca87dae731e39594576aa73c4602ac
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857470"
---
# <a name="powl-function"></a><span data-ttu-id="d68fa-102">Функция Повл</span><span class="sxs-lookup"><span data-stu-id="d68fa-102">PowL function</span></span>

<span data-ttu-id="d68fa-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="d68fa-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="d68fa-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d68fa-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d68fa-105">Возвращает число, возведенное в заданную степень.</span><span class="sxs-lookup"><span data-stu-id="d68fa-105">Returns a number raised to a given power.</span></span>

```qsharp
function PowL (a : BigInt, power : Int) : BigInt
```


## <a name="input"></a><span data-ttu-id="d68fa-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d68fa-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="d68fa-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="d68fa-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="d68fa-108">Число $a $, которое должно быть выдано.</span><span class="sxs-lookup"><span data-stu-id="d68fa-108">The number $a$ that is to be raised.</span></span>


### <a name="power--int"></a><span data-ttu-id="d68fa-109">степень: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d68fa-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d68fa-110">$B $, до которой должно быть создано $a $.</span><span class="sxs-lookup"><span data-stu-id="d68fa-110">The power $b$ to which $a$ should be raised.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="d68fa-111">Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="d68fa-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="d68fa-112">$a питания ^ b $</span><span class="sxs-lookup"><span data-stu-id="d68fa-112">The power $a^b$</span></span>