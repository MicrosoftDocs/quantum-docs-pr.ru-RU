---
uid: Microsoft.Quantum.Math.PNorm
title: Функция Пнорм
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNorm
qsharp.summary: >-
  Returns the `L(p)` norm of a vector of `Double`s.

  That is, given an array $x$ of type `Double[]`, this returns the $p$-norm $\|x\|\_p= (\sum_{j}|x_j|^{p})^{1/p}$.
ms.openlocfilehash: 3fe029bd893fc4d11aaf351f7ea566256cac5a9e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194735"
---
# <a name="pnorm-function"></a><span data-ttu-id="23b79-102">Функция Пнорм</span><span class="sxs-lookup"><span data-stu-id="23b79-102">PNorm function</span></span>

<span data-ttu-id="23b79-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="23b79-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="23b79-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="23b79-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="23b79-105">Возвращает `L(p)` норму вектора типа `Double` .</span><span class="sxs-lookup"><span data-stu-id="23b79-105">Returns the `L(p)` norm of a vector of `Double`s.</span></span>

<span data-ttu-id="23b79-106">То есть при наличии массива, $x $ типа `Double[]` , возвращается $p $-норма $ \| x \| \_ p = (\ sum_ {j} | x_j | ^ {p}) ^ {1/p} $.</span><span class="sxs-lookup"><span data-stu-id="23b79-106">That is, given an array $x$ of type `Double[]`, this returns the $p$-norm $\|x\|\_p= (\sum_{j}|x_j|^{p})^{1/p}$.</span></span>

```qsharp
function PNorm (p : Double, array : Double[]) : Double
```


## <a name="input"></a><span data-ttu-id="23b79-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="23b79-107">Input</span></span>

### <a name="p--double"></a><span data-ttu-id="23b79-108">p: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="23b79-108">p : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="23b79-109">Экспонента $p $ в $p $-норме.</span><span class="sxs-lookup"><span data-stu-id="23b79-109">The exponent $p$ in the $p$-norm.</span></span>


### <a name="array--double"></a><span data-ttu-id="23b79-110">массив: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="23b79-110">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>





## <a name="output--double"></a><span data-ttu-id="23b79-111">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="23b79-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="23b79-112">$P $-норма $ \| x \| _p $.</span><span class="sxs-lookup"><span data-stu-id="23b79-112">The $p$-norm $\|x\|_p$.</span></span>