---
uid: Microsoft.Quantum.Math.SquaredNorm
title: Функция Скуареднорм
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: SquaredNorm
qsharp.summary: Returns the squared 2-norm of a vector.
ms.openlocfilehash: 72ae8266492bef64eaec34cd70c5fe725ee1e8c9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848217"
---
# <a name="squarednorm-function"></a><span data-ttu-id="d53fb-102">Функция Скуареднорм</span><span class="sxs-lookup"><span data-stu-id="d53fb-102">SquaredNorm function</span></span>

<span data-ttu-id="d53fb-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="d53fb-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="d53fb-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d53fb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d53fb-105">Возвращает квадрат с 2 по норме для вектора.</span><span class="sxs-lookup"><span data-stu-id="d53fb-105">Returns the squared 2-norm of a vector.</span></span>

```qsharp
function SquaredNorm (array : Double[]) : Double
```


## <a name="description"></a><span data-ttu-id="d53fb-106">Описание</span><span class="sxs-lookup"><span data-stu-id="d53fb-106">Description</span></span>

<span data-ttu-id="d53fb-107">Возвращает квадратное значение 2-нормы вектора; то есть при наличии входного $ \век{КС} $ возвращается значение $ \ sum_i x_i ^ 2 $.</span><span class="sxs-lookup"><span data-stu-id="d53fb-107">Returns the squared 2-norm of a vector; that is, given an input $\vec{x}$, returns $\sum_i x_i^2$.</span></span>

## <a name="input"></a><span data-ttu-id="d53fb-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d53fb-108">Input</span></span>

### <a name="array--double"></a><span data-ttu-id="d53fb-109">массив: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="d53fb-109">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="d53fb-110">Объект Vector, в котором возвращается значение по норме 2.</span><span class="sxs-lookup"><span data-stu-id="d53fb-110">The vector whose squared 2-norm is to be returned.</span></span>



## <a name="output--double"></a><span data-ttu-id="d53fb-111">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d53fb-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d53fb-112">В квадрате 2 — норма `array` .</span><span class="sxs-lookup"><span data-stu-id="d53fb-112">The squared 2-norm of `array`.</span></span>