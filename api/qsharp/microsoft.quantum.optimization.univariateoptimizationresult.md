---
uid: Microsoft.Quantum.Optimization.UnivariateOptimizationResult
title: Определяемый пользователем тип Унивариатеоптимизатионресулт
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: UnivariateOptimizationResult
qsharp.summary: Represents the result of optimizing a univariate function.
ms.openlocfilehash: 0bcdbda5586181f965297cb2a398d766f9c6fabb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194038"
---
# <a name="univariateoptimizationresult-user-defined-type"></a><span data-ttu-id="8e803-102">Определяемый пользователем тип Унивариатеоптимизатионресулт</span><span class="sxs-lookup"><span data-stu-id="8e803-102">UnivariateOptimizationResult user defined type</span></span>

<span data-ttu-id="8e803-103">Пространство имен: [Microsoft. тактов. Optimization](xref:Microsoft.Quantum.Optimization)</span><span class="sxs-lookup"><span data-stu-id="8e803-103">Namespace: [Microsoft.Quantum.Optimization](xref:Microsoft.Quantum.Optimization)</span></span>

<span data-ttu-id="8e803-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8e803-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8e803-105">Представляет результат оптимизации функции унивариате.</span><span class="sxs-lookup"><span data-stu-id="8e803-105">Represents the result of optimizing a univariate function.</span></span>

```qsharp

newtype UnivariateOptimizationResult = (Coordinate : Double, Value : Double);
```



## <a name="named-items"></a><span data-ttu-id="8e803-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="8e803-106">Named Items</span></span>

### <a name="coordinate--double"></a><span data-ttu-id="8e803-107">Координата: [Двойное](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8e803-107">Coordinate : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8e803-108">Входные данные, для которых была обнаружена оптимальная.</span><span class="sxs-lookup"><span data-stu-id="8e803-108">Input at which an optimum was found.</span></span>
### <a name="value--double"></a><span data-ttu-id="8e803-109">Значение: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8e803-109">Value : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8e803-110">Значение, возвращаемое функцией в своей оптимальной области.</span><span class="sxs-lookup"><span data-stu-id="8e803-110">Value returned by the function at its optimum.</span></span>