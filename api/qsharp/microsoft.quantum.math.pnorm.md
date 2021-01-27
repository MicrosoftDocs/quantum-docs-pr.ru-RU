---
uid: Microsoft.Quantum.Math.PNorm
title: Функция Пнорм
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNorm
qsharp.summary: >-
  Returns the `L(p)` norm of a vector of `Double`s.

  That is, given an array $x$ of type `Double[]`, this returns the $p$-norm $\|x\|\_p= (\sum_{j}|x_j|^{p})^{1/p}$.
ms.openlocfilehash: 6207cca6cda5f9030facd31c327e58bdb9ecbf14
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847650"
---
# <a name="pnorm-function"></a><span data-ttu-id="d3dc4-102">Функция Пнорм</span><span class="sxs-lookup"><span data-stu-id="d3dc4-102">PNorm function</span></span>

<span data-ttu-id="d3dc4-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="d3dc4-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="d3dc4-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d3dc4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d3dc4-105">Возвращает `L(p)` норму вектора типа `Double` .</span><span class="sxs-lookup"><span data-stu-id="d3dc4-105">Returns the `L(p)` norm of a vector of `Double`s.</span></span>

<span data-ttu-id="d3dc4-106">То есть при наличии массива, $x $ типа `Double[]` , возвращается $p $-норма $ \| x \| \_ p = (\ sum_ {j} | x_j | ^ {p}) ^ {1/p} $.</span><span class="sxs-lookup"><span data-stu-id="d3dc4-106">That is, given an array $x$ of type `Double[]`, this returns the $p$-norm $\|x\|\_p= (\sum_{j}|x_j|^{p})^{1/p}$.</span></span>

```qsharp
function PNorm (p : Double, array : Double[]) : Double
```


## <a name="input"></a><span data-ttu-id="d3dc4-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d3dc4-107">Input</span></span>

### <a name="p--double"></a><span data-ttu-id="d3dc4-108">p: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d3dc4-108">p : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d3dc4-109">Экспонента $p $ в $p $-норме.</span><span class="sxs-lookup"><span data-stu-id="d3dc4-109">The exponent $p$ in the $p$-norm.</span></span>


### <a name="array--double"></a><span data-ttu-id="d3dc4-110">массив: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="d3dc4-110">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>





## <a name="output--double"></a><span data-ttu-id="d3dc4-111">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d3dc4-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d3dc4-112">$P $-норма $ \| x \| _p $.</span><span class="sxs-lookup"><span data-stu-id="d3dc4-112">The $p$-norm $\|x\|_p$.</span></span>