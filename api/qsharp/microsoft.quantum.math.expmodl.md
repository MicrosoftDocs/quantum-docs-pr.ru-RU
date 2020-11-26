---
uid: Microsoft.Quantum.Math.ExpModL
title: Функция Експмодл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModL
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: 07da113caeb9f6f3f3f3f92f13478f33021bfa14
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210757"
---
# <a name="expmodl-function"></a><span data-ttu-id="a6586-102">Функция Експмодл</span><span class="sxs-lookup"><span data-stu-id="a6586-102">ExpModL function</span></span>

<span data-ttu-id="a6586-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="a6586-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="a6586-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a6586-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a6586-105">Возвращает целое число, возведенное в заданную степень, по отношению к заданному модулю.</span><span class="sxs-lookup"><span data-stu-id="a6586-105">Returns an integer raised to a given power, with respect to a given modulus.</span></span>

```qsharp
function ExpModL (expBase : BigInt, power : BigInt, modulus : BigInt) : BigInt
```


## <a name="description"></a><span data-ttu-id="a6586-106">Описание</span><span class="sxs-lookup"><span data-stu-id="a6586-106">Description</span></span>

<span data-ttu-id="a6586-107">Давайте $x Експбасе $, Power by $p $ и модулем по $N $.</span><span class="sxs-lookup"><span data-stu-id="a6586-107">Let us denote expBase by $x$, power by $p$ and modulus by $N$.</span></span>
<span data-ttu-id="a6586-108">Функция возвращает $x ^ p \операторнаме{мод} N $.</span><span class="sxs-lookup"><span data-stu-id="a6586-108">The function returns $x^p \operatorname{mod} N$.</span></span>

<span data-ttu-id="a6586-109">Предполагается, что $N $, $x $ являются положительными, а энергопотребление не отрицательно.</span><span class="sxs-lookup"><span data-stu-id="a6586-109">We assume that $N$, $x$ are positive and power is non-negative.</span></span>

## <a name="input"></a><span data-ttu-id="a6586-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a6586-110">Input</span></span>

### <a name="expbase--bigint"></a><span data-ttu-id="a6586-111">Експбасе: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="a6586-111">expBase : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>




### <a name="power--bigint"></a><span data-ttu-id="a6586-112">степень: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="a6586-112">power : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>




### <a name="modulus--bigint"></a><span data-ttu-id="a6586-113">модуль: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="a6586-113">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>





## <a name="output--bigint"></a><span data-ttu-id="a6586-114">Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="a6586-114">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>



## <a name="remarks"></a><span data-ttu-id="a6586-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a6586-115">Remarks</span></span>

<span data-ttu-id="a6586-116">Принимает время пропорционально числу битов в `power` , а не в `power` самой.</span><span class="sxs-lookup"><span data-stu-id="a6586-116">Takes time proportional to the number of bits in `power`, not the `power` itself.</span></span>