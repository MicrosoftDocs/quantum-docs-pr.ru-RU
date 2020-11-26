---
uid: Microsoft.Quantum.Math.ExpModI
title: Функция Експмоди
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModI
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: 197f7351ce76ebb7684ca8014cab9ab65d9c784c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228497"
---
# <a name="expmodi-function"></a><span data-ttu-id="cbe8f-102">Функция Експмоди</span><span class="sxs-lookup"><span data-stu-id="cbe8f-102">ExpModI function</span></span>

<span data-ttu-id="cbe8f-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="cbe8f-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="cbe8f-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cbe8f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cbe8f-105">Возвращает целое число, возведенное в заданную степень, по отношению к заданному модулю.</span><span class="sxs-lookup"><span data-stu-id="cbe8f-105">Returns an integer raised to a given power, with respect to a given modulus.</span></span>

```qsharp
function ExpModI (expBase : Int, power : Int, modulus : Int) : Int
```


## <a name="description"></a><span data-ttu-id="cbe8f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="cbe8f-106">Description</span></span>

<span data-ttu-id="cbe8f-107">Давайте $x Експбасе $, Power by $p $ и модулем по $N $.</span><span class="sxs-lookup"><span data-stu-id="cbe8f-107">Let us denote expBase by $x$, power by $p$ and modulus by $N$.</span></span>
<span data-ttu-id="cbe8f-108">Функция возвращает $x ^ p \операторнаме{мод} N $.</span><span class="sxs-lookup"><span data-stu-id="cbe8f-108">The function returns $x^p \operatorname{mod} N$.</span></span>

<span data-ttu-id="cbe8f-109">Предполагается, что $N $, $x $ являются положительными, а энергопотребление не отрицательно.</span><span class="sxs-lookup"><span data-stu-id="cbe8f-109">We assume that $N$, $x$ are positive and power is non-negative.</span></span>

## <a name="input"></a><span data-ttu-id="cbe8f-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="cbe8f-110">Input</span></span>

### <a name="expbase--int"></a><span data-ttu-id="cbe8f-111">Експбасе: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cbe8f-111">expBase : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="power--int"></a><span data-ttu-id="cbe8f-112">степень: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cbe8f-112">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="modulus--int"></a><span data-ttu-id="cbe8f-113">модуль: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cbe8f-113">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--int"></a><span data-ttu-id="cbe8f-114">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cbe8f-114">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>



## <a name="remarks"></a><span data-ttu-id="cbe8f-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cbe8f-115">Remarks</span></span>

<span data-ttu-id="cbe8f-116">Принимает время пропорционально числу битов в `power` , а не в `power` самой.</span><span class="sxs-lookup"><span data-stu-id="cbe8f-116">Takes time proportional to the number of bits in `power`, not the `power` itself.</span></span>