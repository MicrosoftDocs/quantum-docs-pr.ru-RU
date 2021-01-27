---
uid: Microsoft.Quantum.Math.ContinuedFractionConvergentI
title: Функция Континуедфрактионконверженти
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ContinuedFractionConvergentI
qsharp.summary: Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`
ms.openlocfilehash: c5316c13ce499da88c0d5c45b9d8c5e3a8c6162d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853861"
---
# <a name="continuedfractionconvergenti-function"></a><span data-ttu-id="a4f13-102">Функция Континуедфрактионконверженти</span><span class="sxs-lookup"><span data-stu-id="a4f13-102">ContinuedFractionConvergentI function</span></span>

<span data-ttu-id="a4f13-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="a4f13-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="a4f13-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a4f13-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a4f13-105">Находит непрерывные дроби, наиболее близкие к `fraction` знаменателю меньше или равно `denominatorBound`</span><span class="sxs-lookup"><span data-stu-id="a4f13-105">Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`</span></span>

```qsharp
function ContinuedFractionConvergentI (fraction : Microsoft.Quantum.Math.Fraction, denominatorBound : Int) : Microsoft.Quantum.Math.Fraction
```


## <a name="input"></a><span data-ttu-id="a4f13-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a4f13-106">Input</span></span>

### <a name="fraction--fraction"></a><span data-ttu-id="a4f13-107">Дробь: [дробь](xref:Microsoft.Quantum.Math.Fraction)</span><span class="sxs-lookup"><span data-stu-id="a4f13-107">fraction : [Fraction](xref:Microsoft.Quantum.Math.Fraction)</span></span>




### <a name="denominatorbound--int"></a><span data-ttu-id="a4f13-108">Деноминаторбаунд: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a4f13-108">denominatorBound : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--fraction"></a><span data-ttu-id="a4f13-109">Выходные данные: [дробь](xref:Microsoft.Quantum.Math.Fraction)</span><span class="sxs-lookup"><span data-stu-id="a4f13-109">Output : [Fraction](xref:Microsoft.Quantum.Math.Fraction)</span></span>

<span data-ttu-id="a4f13-110">Продолжение ближайшей дробной части `fraction` с знаменателем меньше или равным `denominatorBound`</span><span class="sxs-lookup"><span data-stu-id="a4f13-110">Continued fraction closest to `fraction` with the denominator less or equal to `denominatorBound`</span></span>