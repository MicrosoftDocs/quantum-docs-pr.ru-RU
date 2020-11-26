---
uid: Microsoft.Quantum.Math.SquaredNorm
title: Функция Скуареднорм
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: SquaredNorm
qsharp.summary: Returns the squared 2-norm of a vector.
ms.openlocfilehash: ecbc66a8851f23187e0c0ea53ce121442323733b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227307"
---
# <a name="squarednorm-function"></a><span data-ttu-id="4f4e3-102">Функция Скуареднорм</span><span class="sxs-lookup"><span data-stu-id="4f4e3-102">SquaredNorm function</span></span>

<span data-ttu-id="4f4e3-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="4f4e3-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="4f4e3-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4f4e3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4f4e3-105">Возвращает квадрат с 2 по норме для вектора.</span><span class="sxs-lookup"><span data-stu-id="4f4e3-105">Returns the squared 2-norm of a vector.</span></span>

```qsharp
function SquaredNorm (array : Double[]) : Double
```


## <a name="description"></a><span data-ttu-id="4f4e3-106">Описание</span><span class="sxs-lookup"><span data-stu-id="4f4e3-106">Description</span></span>

<span data-ttu-id="4f4e3-107">Возвращает квадратное значение 2-нормы вектора; то есть при наличии входного $ \век{КС} $ возвращается значение $ \ sum_i x_i ^ 2 $.</span><span class="sxs-lookup"><span data-stu-id="4f4e3-107">Returns the squared 2-norm of a vector; that is, given an input $\vec{x}$, returns $\sum_i x_i^2$.</span></span>

## <a name="input"></a><span data-ttu-id="4f4e3-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4f4e3-108">Input</span></span>

### <a name="array--double"></a><span data-ttu-id="4f4e3-109">массив: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="4f4e3-109">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="4f4e3-110">Объект Vector, в котором возвращается значение по норме 2.</span><span class="sxs-lookup"><span data-stu-id="4f4e3-110">The vector whose squared 2-norm is to be returned.</span></span>



## <a name="output--double"></a><span data-ttu-id="4f4e3-111">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="4f4e3-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="4f4e3-112">В квадрате 2 — норма `array` .</span><span class="sxs-lookup"><span data-stu-id="4f4e3-112">The squared 2-norm of `array`.</span></span>