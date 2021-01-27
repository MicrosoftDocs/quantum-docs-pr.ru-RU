---
uid: Microsoft.Quantum.Optimization.UnivariateOptimizationResult
title: Определяемый пользователем тип Унивариатеоптимизатионресулт
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: UnivariateOptimizationResult
qsharp.summary: Represents the result of optimizing a univariate function.
ms.openlocfilehash: cc54c0035796aac86482e8a3a6896ceb197c7cfe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854570"
---
# <a name="univariateoptimizationresult-user-defined-type"></a><span data-ttu-id="56488-102">Определяемый пользователем тип Унивариатеоптимизатионресулт</span><span class="sxs-lookup"><span data-stu-id="56488-102">UnivariateOptimizationResult user defined type</span></span>

<span data-ttu-id="56488-103">Пространство имен: [Microsoft. тактов. Optimization](xref:Microsoft.Quantum.Optimization)</span><span class="sxs-lookup"><span data-stu-id="56488-103">Namespace: [Microsoft.Quantum.Optimization](xref:Microsoft.Quantum.Optimization)</span></span>

<span data-ttu-id="56488-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="56488-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="56488-105">Представляет результат оптимизации функции унивариате.</span><span class="sxs-lookup"><span data-stu-id="56488-105">Represents the result of optimizing a univariate function.</span></span>

```qsharp

newtype UnivariateOptimizationResult = (Coordinate : Double, Value : Double);
```



## <a name="named-items"></a><span data-ttu-id="56488-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="56488-106">Named Items</span></span>

### <a name="coordinate--double"></a><span data-ttu-id="56488-107">Координата: [Двойное](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="56488-107">Coordinate : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="56488-108">Входные данные, для которых была обнаружена оптимальная.</span><span class="sxs-lookup"><span data-stu-id="56488-108">Input at which an optimum was found.</span></span>
### <a name="value--double"></a><span data-ttu-id="56488-109">Значение: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="56488-109">Value : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="56488-110">Значение, возвращаемое функцией в своей оптимальной области.</span><span class="sxs-lookup"><span data-stu-id="56488-110">Value returned by the function at its optimum.</span></span>