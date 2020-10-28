---
uid: Microsoft.Quantum.Math.SquaredNorm
title: Функция Скуареднорм
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: SquaredNorm
qsharp.summary: Returns the squared 2-norm of a vector.
ms.openlocfilehash: 4165a761753f336cb7b94ad36b11ac324ad4e5c6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733801"
---
# <a name="squarednorm-function"></a><span data-ttu-id="04c7b-102">Функция Скуареднорм</span><span class="sxs-lookup"><span data-stu-id="04c7b-102">SquaredNorm function</span></span>

<span data-ttu-id="04c7b-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="04c7b-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="04c7b-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="04c7b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="04c7b-105">Возвращает квадрат с 2 по норме для вектора.</span><span class="sxs-lookup"><span data-stu-id="04c7b-105">Returns the squared 2-norm of a vector.</span></span>

```qsharp
function SquaredNorm (array : Double[]) : Double
```


## <a name="description"></a><span data-ttu-id="04c7b-106">Описание</span><span class="sxs-lookup"><span data-stu-id="04c7b-106">Description</span></span>

<span data-ttu-id="04c7b-107">Возвращает квадратное значение 2-нормы вектора; то есть при наличии входного $ \век{КС} $ возвращается значение $ \ sum_i x_i ^ 2 $.</span><span class="sxs-lookup"><span data-stu-id="04c7b-107">Returns the squared 2-norm of a vector; that is, given an input $\vec{x}$, returns $\sum_i x_i^2$.</span></span>

## <a name="input"></a><span data-ttu-id="04c7b-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="04c7b-108">Input</span></span>

### <a name="array--double"></a><span data-ttu-id="04c7b-109">массив: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="04c7b-109">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="04c7b-110">Объект Vector, в котором возвращается значение по норме 2.</span><span class="sxs-lookup"><span data-stu-id="04c7b-110">The vector whose squared 2-norm is to be returned.</span></span>



## <a name="output--double"></a><span data-ttu-id="04c7b-111">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="04c7b-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="04c7b-112">В квадрате 2 — норма `array` .</span><span class="sxs-lookup"><span data-stu-id="04c7b-112">The squared 2-norm of `array`.</span></span>