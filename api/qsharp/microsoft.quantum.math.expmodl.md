---
uid: Microsoft.Quantum.Math.ExpModL
title: Функция Експмодл
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModL
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: 127f2e51e19c76f4f7973bf1ac2217d4fffd72f6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848369"
---
# <a name="expmodl-function"></a><span data-ttu-id="b15bd-102">Функция Експмодл</span><span class="sxs-lookup"><span data-stu-id="b15bd-102">ExpModL function</span></span>

<span data-ttu-id="b15bd-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="b15bd-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="b15bd-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b15bd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b15bd-105">Возвращает целое число, возведенное в заданную степень, по отношению к заданному модулю.</span><span class="sxs-lookup"><span data-stu-id="b15bd-105">Returns an integer raised to a given power, with respect to a given modulus.</span></span>

```qsharp
function ExpModL (expBase : BigInt, power : BigInt, modulus : BigInt) : BigInt
```


## <a name="description"></a><span data-ttu-id="b15bd-106">Описание</span><span class="sxs-lookup"><span data-stu-id="b15bd-106">Description</span></span>

<span data-ttu-id="b15bd-107">Давайте $x Експбасе $, Power by $p $ и модулем по $N $.</span><span class="sxs-lookup"><span data-stu-id="b15bd-107">Let us denote expBase by $x$, power by $p$ and modulus by $N$.</span></span>
<span data-ttu-id="b15bd-108">Функция возвращает $x ^ p \операторнаме{мод} N $.</span><span class="sxs-lookup"><span data-stu-id="b15bd-108">The function returns $x^p \operatorname{mod} N$.</span></span>

<span data-ttu-id="b15bd-109">Предполагается, что $N $, $x $ являются положительными, а энергопотребление не отрицательно.</span><span class="sxs-lookup"><span data-stu-id="b15bd-109">We assume that $N$, $x$ are positive and power is non-negative.</span></span>

## <a name="input"></a><span data-ttu-id="b15bd-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b15bd-110">Input</span></span>

### <a name="expbase--bigint"></a><span data-ttu-id="b15bd-111">Експбасе: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="b15bd-111">expBase : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>




### <a name="power--bigint"></a><span data-ttu-id="b15bd-112">степень: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="b15bd-112">power : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>




### <a name="modulus--bigint"></a><span data-ttu-id="b15bd-113">модуль: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="b15bd-113">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>





## <a name="output--bigint"></a><span data-ttu-id="b15bd-114">Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="b15bd-114">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>



## <a name="remarks"></a><span data-ttu-id="b15bd-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="b15bd-115">Remarks</span></span>

<span data-ttu-id="b15bd-116">Принимает время пропорционально числу битов в `power` , а не в `power` самой.</span><span class="sxs-lookup"><span data-stu-id="b15bd-116">Takes time proportional to the number of bits in `power`, not the `power` itself.</span></span>