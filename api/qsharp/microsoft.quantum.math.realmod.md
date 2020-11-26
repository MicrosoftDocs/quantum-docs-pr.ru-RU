---
uid: Microsoft.Quantum.Math.RealMod
title: Функция Реалмод
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: RealMod
qsharp.summary: Computes the modulus between two real numbers.
ms.openlocfilehash: 20916d8462288395384aa875bfae4f042ba6b6ad
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228259"
---
# <a name="realmod-function"></a><span data-ttu-id="100b0-102">Функция Реалмод</span><span class="sxs-lookup"><span data-stu-id="100b0-102">RealMod function</span></span>

<span data-ttu-id="100b0-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="100b0-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="100b0-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="100b0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="100b0-105">Выполняет вычисление модуля между двумя вещественными числами.</span><span class="sxs-lookup"><span data-stu-id="100b0-105">Computes the modulus between two real numbers.</span></span>

```qsharp
function RealMod (value : Double, modulo : Double, minValue : Double) : Double
```


## <a name="input"></a><span data-ttu-id="100b0-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="100b0-106">Input</span></span>

### <a name="value--double"></a><span data-ttu-id="100b0-107">значение: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="100b0-107">value : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="100b0-108">Вещественное число $x $ для получения модуля.</span><span class="sxs-lookup"><span data-stu-id="100b0-108">A real number $x$ to take the modulus of.</span></span>


### <a name="modulo--double"></a><span data-ttu-id="100b0-109">остаток от деления: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="100b0-109">modulo : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="100b0-110">Вещественное число, взятое из модуля $x $ по отношению к.</span><span class="sxs-lookup"><span data-stu-id="100b0-110">A real number to take the modulus of $x$ with respect to.</span></span>


### <a name="minvalue--double"></a><span data-ttu-id="100b0-111">minValue: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="100b0-111">minValue : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="100b0-112">Наименьшее значение, возвращаемое этой функцией.</span><span class="sxs-lookup"><span data-stu-id="100b0-112">The smallest value to be returned by this function.</span></span>



## <a name="output--double"></a><span data-ttu-id="100b0-113">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="100b0-113">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="100b0-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="100b0-114">Remarks</span></span>

<span data-ttu-id="100b0-115">Эта функция вычислит реальный модуль, заключив реальную строку вокруг единицы круга, а затем находим угол на единицу круга, соответствующую входным данным.</span><span class="sxs-lookup"><span data-stu-id="100b0-115">This function computes the real modulus by wrapping the real line about the unit circle, then finding the angle on the unit circle corresponding to the input.</span></span>
<span data-ttu-id="100b0-116">`minValue`Затем входные данные фактически указывают, куда вырезать единицу круга.</span><span class="sxs-lookup"><span data-stu-id="100b0-116">The `minValue` input then effectively specifies where to cut the unit circle.</span></span>