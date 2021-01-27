---
uid: Microsoft.Quantum.Math.ContinuedFractionConvergentL
title: Функция Континуедфрактионконвержентл
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ContinuedFractionConvergentL
qsharp.summary: Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`
ms.openlocfilehash: 14f0eee5565b3e80f4090a2d3763ef96c928368d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856393"
---
# <a name="continuedfractionconvergentl-function"></a><span data-ttu-id="2a2b3-102">Функция Континуедфрактионконвержентл</span><span class="sxs-lookup"><span data-stu-id="2a2b3-102">ContinuedFractionConvergentL function</span></span>

<span data-ttu-id="2a2b3-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="2a2b3-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="2a2b3-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2a2b3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2a2b3-105">Находит непрерывные дроби, наиболее близкие к `fraction` знаменателю меньше или равно `denominatorBound`</span><span class="sxs-lookup"><span data-stu-id="2a2b3-105">Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`</span></span>

```qsharp
function ContinuedFractionConvergentL (fraction : Microsoft.Quantum.Math.BigFraction, denominatorBound : BigInt) : Microsoft.Quantum.Math.BigFraction
```


## <a name="input"></a><span data-ttu-id="2a2b3-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2a2b3-106">Input</span></span>

### <a name="fraction--bigfraction"></a><span data-ttu-id="2a2b3-107">Дробь: [бигфрактион](xref:Microsoft.Quantum.Math.BigFraction)</span><span class="sxs-lookup"><span data-stu-id="2a2b3-107">fraction : [BigFraction](xref:Microsoft.Quantum.Math.BigFraction)</span></span>




### <a name="denominatorbound--bigint"></a><span data-ttu-id="2a2b3-108">Деноминаторбаунд: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="2a2b3-108">denominatorBound : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>





## <a name="output--bigfraction"></a><span data-ttu-id="2a2b3-109">Выходные данные: [бигфрактион](xref:Microsoft.Quantum.Math.BigFraction)</span><span class="sxs-lookup"><span data-stu-id="2a2b3-109">Output : [BigFraction](xref:Microsoft.Quantum.Math.BigFraction)</span></span>

<span data-ttu-id="2a2b3-110">Продолжение ближайшей дробной части `fraction` с знаменателем меньше или равным `denominatorBound`</span><span class="sxs-lookup"><span data-stu-id="2a2b3-110">Continued fraction closest to `fraction` with the denominator less or equal to `denominatorBound`</span></span>