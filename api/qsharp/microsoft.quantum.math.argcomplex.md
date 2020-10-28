---
uid: Microsoft.Quantum.Math.ArgComplex
title: Функция Аргкомплекс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ArgComplex
qsharp.summary: Returns the phase of a complex number of type `Complex`.
ms.openlocfilehash: 629aa32ad80e5aa3d6f5ff75ac65df9b1a96fc15
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732800"
---
# <a name="argcomplex-function"></a><span data-ttu-id="600cd-102">Функция Аргкомплекс</span><span class="sxs-lookup"><span data-stu-id="600cd-102">ArgComplex function</span></span>

<span data-ttu-id="600cd-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="600cd-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="600cd-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="600cd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="600cd-105">Возвращает фазу комплексного числа типа `Complex` .</span><span class="sxs-lookup"><span data-stu-id="600cd-105">Returns the phase of a complex number of type `Complex`.</span></span>

```qsharp
function ArgComplex (input : Microsoft.Quantum.Math.Complex) : Double
```


## <a name="input"></a><span data-ttu-id="600cd-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="600cd-106">Input</span></span>

### <a name="input--complex"></a><span data-ttu-id="600cd-107">входные данные: [сложные](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="600cd-107">input : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="600cd-108">Комплексное число $c = x + i y $.</span><span class="sxs-lookup"><span data-stu-id="600cd-108">Complex number $c = x + i y$.</span></span>



## <a name="output--double"></a><span data-ttu-id="600cd-109">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="600cd-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="600cd-110">Этап $ \Текст{АРГ} [c] = \Текст{арктан} (y, x) \ин (-\пи, \пи] $).</span><span class="sxs-lookup"><span data-stu-id="600cd-110">Phase $\text{Arg}[c] = \text{ArcTan}(y,x) \in (-\pi,\pi]$.</span></span>