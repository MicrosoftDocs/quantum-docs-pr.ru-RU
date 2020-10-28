---
uid: Microsoft.Quantum.Math.ExpModL
title: Функция Експмодл
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModL
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: 73d434bd364847b4e5e06d1a9f460424e0c50850
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733064"
---
# <a name="expmodl-function"></a><span data-ttu-id="1b798-102">Функция Експмодл</span><span class="sxs-lookup"><span data-stu-id="1b798-102">ExpModL function</span></span>

<span data-ttu-id="1b798-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="1b798-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="1b798-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1b798-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1b798-105">Возвращает целое число, возведенное в заданную степень, по отношению к заданному модулю.</span><span class="sxs-lookup"><span data-stu-id="1b798-105">Returns an integer raised to a given power, with respect to a given modulus.</span></span>

```qsharp
function ExpModL (expBase : BigInt, power : BigInt, modulus : BigInt) : BigInt
```


## <a name="description"></a><span data-ttu-id="1b798-106">Описание</span><span class="sxs-lookup"><span data-stu-id="1b798-106">Description</span></span>

<span data-ttu-id="1b798-107">Давайте $x Експбасе $, Power by $p $ и модулем по $N $.</span><span class="sxs-lookup"><span data-stu-id="1b798-107">Let us denote expBase by $x$, power by $p$ and modulus by $N$.</span></span>
<span data-ttu-id="1b798-108">Функция возвращает $x ^ p \операторнаме{мод} N $.</span><span class="sxs-lookup"><span data-stu-id="1b798-108">The function returns $x^p \operatorname{mod} N$.</span></span>

<span data-ttu-id="1b798-109">Предполагается, что $N $, $x $ являются положительными, а энергопотребление не отрицательно.</span><span class="sxs-lookup"><span data-stu-id="1b798-109">We assume that $N$, $x$ are positive and power is non-negative.</span></span>

## <a name="input"></a><span data-ttu-id="1b798-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="1b798-110">Input</span></span>

### <a name="expbase--bigint"></a><span data-ttu-id="1b798-111">Експбасе: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="1b798-111">expBase : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>




### <a name="power--bigint"></a><span data-ttu-id="1b798-112">степень: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="1b798-112">power : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>




### <a name="modulus--bigint"></a><span data-ttu-id="1b798-113">модуль: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="1b798-113">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>





## <a name="output--bigint"></a><span data-ttu-id="1b798-114">Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="1b798-114">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>



## <a name="remarks"></a><span data-ttu-id="1b798-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="1b798-115">Remarks</span></span>

<span data-ttu-id="1b798-116">Принимает время пропорционально числу битов в `power` , а не в `power` самой.</span><span class="sxs-lookup"><span data-stu-id="1b798-116">Takes time proportional to the number of bits in `power`, not the `power` itself.</span></span>