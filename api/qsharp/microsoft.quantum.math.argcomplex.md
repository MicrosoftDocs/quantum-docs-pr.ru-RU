---
uid: Microsoft.Quantum.Math.ArgComplex
title: Функция Аргкомплекс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ArgComplex
qsharp.summary: Returns the phase of a complex number of type `Complex`.
ms.openlocfilehash: e8ce73a43940ab0ed66338f962cc6f76fc2b694b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842755"
---
# <a name="argcomplex-function"></a><span data-ttu-id="00900-102">Функция Аргкомплекс</span><span class="sxs-lookup"><span data-stu-id="00900-102">ArgComplex function</span></span>

<span data-ttu-id="00900-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="00900-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="00900-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="00900-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="00900-105">Возвращает фазу комплексного числа типа `Complex` .</span><span class="sxs-lookup"><span data-stu-id="00900-105">Returns the phase of a complex number of type `Complex`.</span></span>

```qsharp
function ArgComplex (input : Microsoft.Quantum.Math.Complex) : Double
```


## <a name="input"></a><span data-ttu-id="00900-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="00900-106">Input</span></span>

### <a name="input--complex"></a><span data-ttu-id="00900-107">входные данные: [сложные](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="00900-107">input : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="00900-108">Комплексное число $c = x + i y $.</span><span class="sxs-lookup"><span data-stu-id="00900-108">Complex number $c = x + i y$.</span></span>



## <a name="output--double"></a><span data-ttu-id="00900-109">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="00900-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="00900-110">Этап $ \Текст{АРГ} [c] = \Текст{арктан} (y, x) \ин (-\пи, \пи] $).</span><span class="sxs-lookup"><span data-stu-id="00900-110">Phase $\text{Arg}[c] = \text{ArcTan}(y,x) \in (-\pi,\pi]$.</span></span>