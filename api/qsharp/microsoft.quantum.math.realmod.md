---
uid: Microsoft.Quantum.Math.RealMod
title: Функция Реалмод
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: RealMod
qsharp.summary: Computes the modulus between two real numbers.
ms.openlocfilehash: 56da313fabb20655ec358120b8d9b435e4971159
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848352"
---
# <a name="realmod-function"></a><span data-ttu-id="092f5-102">Функция Реалмод</span><span class="sxs-lookup"><span data-stu-id="092f5-102">RealMod function</span></span>

<span data-ttu-id="092f5-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="092f5-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="092f5-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="092f5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="092f5-105">Выполняет вычисление модуля между двумя вещественными числами.</span><span class="sxs-lookup"><span data-stu-id="092f5-105">Computes the modulus between two real numbers.</span></span>

```qsharp
function RealMod (value : Double, modulo : Double, minValue : Double) : Double
```


## <a name="input"></a><span data-ttu-id="092f5-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="092f5-106">Input</span></span>

### <a name="value--double"></a><span data-ttu-id="092f5-107">значение: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="092f5-107">value : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="092f5-108">Вещественное число $x $ для получения модуля.</span><span class="sxs-lookup"><span data-stu-id="092f5-108">A real number $x$ to take the modulus of.</span></span>


### <a name="modulo--double"></a><span data-ttu-id="092f5-109">остаток от деления: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="092f5-109">modulo : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="092f5-110">Вещественное число, взятое из модуля $x $ по отношению к.</span><span class="sxs-lookup"><span data-stu-id="092f5-110">A real number to take the modulus of $x$ with respect to.</span></span>


### <a name="minvalue--double"></a><span data-ttu-id="092f5-111">minValue: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="092f5-111">minValue : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="092f5-112">Наименьшее значение, возвращаемое этой функцией.</span><span class="sxs-lookup"><span data-stu-id="092f5-112">The smallest value to be returned by this function.</span></span>



## <a name="output--double"></a><span data-ttu-id="092f5-113">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="092f5-113">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="example"></a><span data-ttu-id="092f5-114">Пример</span><span class="sxs-lookup"><span data-stu-id="092f5-114">Example</span></span>

```qsharp
    // Returns 3 π / 2.
    let y = RealMod(5.5 * PI(), 2.0 * PI(), 0.0);
    // Returns -1.2, since +3.6 and -1.2 are 4.8 apart on the real line,
    // which is a multiple of 2.4.
    let z = RealMod(3.6, 2.4, -1.2);
```

## <a name="remarks"></a><span data-ttu-id="092f5-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="092f5-115">Remarks</span></span>

<span data-ttu-id="092f5-116">Эта функция вычислит реальный модуль, заключив реальную строку вокруг единицы круга, а затем находим угол на единицу круга, соответствующую входным данным.</span><span class="sxs-lookup"><span data-stu-id="092f5-116">This function computes the real modulus by wrapping the real line about the unit circle, then finding the angle on the unit circle corresponding to the input.</span></span>
<span data-ttu-id="092f5-117">`minValue`Затем входные данные фактически указывают, куда вырезать единицу круга.</span><span class="sxs-lookup"><span data-stu-id="092f5-117">The `minValue` input then effectively specifies where to cut the unit circle.</span></span>