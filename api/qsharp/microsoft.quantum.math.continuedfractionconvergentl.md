---
uid: Microsoft.Quantum.Math.ContinuedFractionConvergentL
title: Функция Континуедфрактионконвержентл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ContinuedFractionConvergentL
qsharp.summary: Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`
ms.openlocfilehash: c10fcbbe63d3d4c7d6c56196768c1062be1ca350
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210936"
---
# <a name="continuedfractionconvergentl-function"></a><span data-ttu-id="402eb-102">Функция Континуедфрактионконвержентл</span><span class="sxs-lookup"><span data-stu-id="402eb-102">ContinuedFractionConvergentL function</span></span>

<span data-ttu-id="402eb-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="402eb-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="402eb-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="402eb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="402eb-105">Находит непрерывные дроби, наиболее близкие к `fraction` знаменателю меньше или равно `denominatorBound`</span><span class="sxs-lookup"><span data-stu-id="402eb-105">Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`</span></span>

```qsharp
function ContinuedFractionConvergentL (fraction : Microsoft.Quantum.Math.BigFraction, denominatorBound : BigInt) : Microsoft.Quantum.Math.BigFraction
```


## <a name="input"></a><span data-ttu-id="402eb-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="402eb-106">Input</span></span>

### <a name="fraction--bigfraction"></a><span data-ttu-id="402eb-107">Дробь: [бигфрактион](xref:Microsoft.Quantum.Math.BigFraction)</span><span class="sxs-lookup"><span data-stu-id="402eb-107">fraction : [BigFraction](xref:Microsoft.Quantum.Math.BigFraction)</span></span>




### <a name="denominatorbound--bigint"></a><span data-ttu-id="402eb-108">Деноминаторбаунд: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="402eb-108">denominatorBound : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>





## <a name="output--bigfraction"></a><span data-ttu-id="402eb-109">Выходные данные: [бигфрактион](xref:Microsoft.Quantum.Math.BigFraction)</span><span class="sxs-lookup"><span data-stu-id="402eb-109">Output : [BigFraction](xref:Microsoft.Quantum.Math.BigFraction)</span></span>

<span data-ttu-id="402eb-110">Продолжение ближайшей дробной части `fraction` с знаменателем меньше или равным `denominatorBound`</span><span class="sxs-lookup"><span data-stu-id="402eb-110">Continued fraction closest to `fraction` with the denominator less or equal to `denominatorBound`</span></span>