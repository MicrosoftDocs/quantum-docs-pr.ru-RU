---
uid: Microsoft.Quantum.Math.ContinuedFractionConvergentI
title: Функция Континуедфрактионконверженти
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ContinuedFractionConvergentI
qsharp.summary: Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`
ms.openlocfilehash: 2322e005a5afb73d9719eb65d9ebf50740f1c9fc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732752"
---
# <a name="continuedfractionconvergenti-function"></a><span data-ttu-id="a8472-102">Функция Континуедфрактионконверженти</span><span class="sxs-lookup"><span data-stu-id="a8472-102">ContinuedFractionConvergentI function</span></span>

<span data-ttu-id="a8472-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="a8472-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="a8472-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a8472-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a8472-105">Находит непрерывные дроби, наиболее близкие к `fraction` знаменателю меньше или равно `denominatorBound`</span><span class="sxs-lookup"><span data-stu-id="a8472-105">Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`</span></span>

```qsharp
function ContinuedFractionConvergentI (fraction : Microsoft.Quantum.Math.Fraction, denominatorBound : Int) : Microsoft.Quantum.Math.Fraction
```


## <a name="input"></a><span data-ttu-id="a8472-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a8472-106">Input</span></span>

### <a name="fraction--fraction"></a><span data-ttu-id="a8472-107">Дробь: [дробь](xref:Microsoft.Quantum.Math.Fraction)</span><span class="sxs-lookup"><span data-stu-id="a8472-107">fraction : [Fraction](xref:Microsoft.Quantum.Math.Fraction)</span></span>




### <a name="denominatorbound--int"></a><span data-ttu-id="a8472-108">Деноминаторбаунд: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a8472-108">denominatorBound : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--fraction"></a><span data-ttu-id="a8472-109">Выходные данные: [дробь](xref:Microsoft.Quantum.Math.Fraction)</span><span class="sxs-lookup"><span data-stu-id="a8472-109">Output : [Fraction](xref:Microsoft.Quantum.Math.Fraction)</span></span>

<span data-ttu-id="a8472-110">Продолжение ближайшей дробной части `fraction` с знаменателем меньше или равным `denominatorBound`</span><span class="sxs-lookup"><span data-stu-id="a8472-110">Continued fraction closest to `fraction` with the denominator less or equal to `denominatorBound`</span></span>