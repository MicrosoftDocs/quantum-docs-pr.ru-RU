---
uid: Microsoft.Quantum.Optimization.UnivariateOptimizationResult
title: Определяемый пользователем тип Унивариатеоптимизатионресулт
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: UnivariateOptimizationResult
qsharp.summary: Represents the result of optimizing a univariate function.
ms.openlocfilehash: c8aa91bbdc9e9e9bb4d110b470ff2041f9460a38
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733401"
---
# <a name="univariateoptimizationresult-user-defined-type"></a><span data-ttu-id="23607-102">Определяемый пользователем тип Унивариатеоптимизатионресулт</span><span class="sxs-lookup"><span data-stu-id="23607-102">UnivariateOptimizationResult user defined type</span></span>

<span data-ttu-id="23607-103">Пространство имен: [Microsoft. тактов. Optimization](xref:Microsoft.Quantum.Optimization)</span><span class="sxs-lookup"><span data-stu-id="23607-103">Namespace: [Microsoft.Quantum.Optimization](xref:Microsoft.Quantum.Optimization)</span></span>

<span data-ttu-id="23607-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="23607-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="23607-105">Представляет результат оптимизации функции унивариате.</span><span class="sxs-lookup"><span data-stu-id="23607-105">Represents the result of optimizing a univariate function.</span></span>

```qsharp

newtype UnivariateOptimizationResult = (Coordinate : Double, Value : Double);
```



## <a name="named-items"></a><span data-ttu-id="23607-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="23607-106">Named Items</span></span>

### <a name="coordinate--double"></a><span data-ttu-id="23607-107">Координата: [Двойное](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="23607-107">Coordinate : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="23607-108">Входные данные, для которых была обнаружена оптимальная.</span><span class="sxs-lookup"><span data-stu-id="23607-108">Input at which an optimum was found.</span></span>
### <a name="value--double"></a><span data-ttu-id="23607-109">Значение: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="23607-109">Value : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="23607-110">Значение, возвращаемое функцией в своей оптимальной области.</span><span class="sxs-lookup"><span data-stu-id="23607-110">Value returned by the function at its optimum.</span></span>