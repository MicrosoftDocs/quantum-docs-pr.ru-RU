---
uid: Microsoft.Quantum.Math.RealMod
title: Функция Реалмод
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: RealMod
qsharp.summary: Computes the modulus between two real numbers.
ms.openlocfilehash: 6ec799885bd2f0d35314ed727356499efbe9fcf8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731040"
---
# <a name="realmod-function"></a><span data-ttu-id="e88c9-102">Функция Реалмод</span><span class="sxs-lookup"><span data-stu-id="e88c9-102">RealMod function</span></span>

<span data-ttu-id="e88c9-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="e88c9-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="e88c9-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e88c9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e88c9-105">Выполняет вычисление модуля между двумя вещественными числами.</span><span class="sxs-lookup"><span data-stu-id="e88c9-105">Computes the modulus between two real numbers.</span></span>

```qsharp
function RealMod (value : Double, modulo : Double, minValue : Double) : Double
```


## <a name="input"></a><span data-ttu-id="e88c9-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e88c9-106">Input</span></span>

### <a name="value--double"></a><span data-ttu-id="e88c9-107">значение: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e88c9-107">value : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e88c9-108">Вещественное число $x $ для получения модуля.</span><span class="sxs-lookup"><span data-stu-id="e88c9-108">A real number $x$ to take the modulus of.</span></span>


### <a name="modulo--double"></a><span data-ttu-id="e88c9-109">остаток от деления: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e88c9-109">modulo : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e88c9-110">Вещественное число, взятое из модуля $x $ по отношению к.</span><span class="sxs-lookup"><span data-stu-id="e88c9-110">A real number to take the modulus of $x$ with respect to.</span></span>


### <a name="minvalue--double"></a><span data-ttu-id="e88c9-111">minValue: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e88c9-111">minValue : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e88c9-112">Наименьшее значение, возвращаемое этой функцией.</span><span class="sxs-lookup"><span data-stu-id="e88c9-112">The smallest value to be returned by this function.</span></span>



## <a name="output--double"></a><span data-ttu-id="e88c9-113">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e88c9-113">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="e88c9-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="e88c9-114">Remarks</span></span>

<span data-ttu-id="e88c9-115">Эта функция вычислит реальный модуль, заключив реальную строку вокруг единицы круга, а затем находим угол на единицу круга, соответствующую входным данным.</span><span class="sxs-lookup"><span data-stu-id="e88c9-115">This function computes the real modulus by wrapping the real line about the unit circle, then finding the angle on the unit circle corresponding to the input.</span></span>
<span data-ttu-id="e88c9-116">`minValue`Затем входные данные фактически указывают, куда вырезать единицу круга.</span><span class="sxs-lookup"><span data-stu-id="e88c9-116">The `minValue` input then effectively specifies where to cut the unit circle.</span></span>