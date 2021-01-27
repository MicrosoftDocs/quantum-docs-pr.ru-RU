---
uid: Microsoft.Quantum.Optimization.LocalUnivariateMinimum
title: Функция Локалунивариатеминимум
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: LocalUnivariateMinimum
qsharp.summary: Returns the local minimum for a univariate function over a bounded interval, using a golden interval search.
ms.openlocfilehash: c2d094a6d0e0c7cecb249cd517995e11dff3d3b0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854614"
---
# <a name="localunivariateminimum-function"></a><span data-ttu-id="59674-102">Функция Локалунивариатеминимум</span><span class="sxs-lookup"><span data-stu-id="59674-102">LocalUnivariateMinimum function</span></span>

<span data-ttu-id="59674-103">Пространство имен: [Microsoft. тактов. Optimization](xref:Microsoft.Quantum.Optimization)</span><span class="sxs-lookup"><span data-stu-id="59674-103">Namespace: [Microsoft.Quantum.Optimization](xref:Microsoft.Quantum.Optimization)</span></span>

<span data-ttu-id="59674-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="59674-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="59674-105">Возвращает локальное минимальное значение для функции унивариате через ограниченный интервал при помощи золотого интервала поиска.</span><span class="sxs-lookup"><span data-stu-id="59674-105">Returns the local minimum for a univariate function over a bounded interval, using a golden interval search.</span></span>

```qsharp
function LocalUnivariateMinimum (fn : (Double -> Double), bounds : (Double, Double), tolerance : Double) : Microsoft.Quantum.Optimization.UnivariateOptimizationResult
```


## <a name="input"></a><span data-ttu-id="59674-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="59674-106">Input</span></span>

### <a name="fn--double---double"></a><span data-ttu-id="59674-107">FN: [Двойное](xref:microsoft.quantum.lang-ref.double) -> [Двойное](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="59674-107">fn : [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="59674-108">Функция унивариате для сворачивания.</span><span class="sxs-lookup"><span data-stu-id="59674-108">The univariate function to be minimized.</span></span>


### <a name="bounds--doubledouble"></a><span data-ttu-id="59674-109">границы: ([Двойное](xref:microsoft.quantum.lang-ref.double),[двойной](xref:microsoft.quantum.lang-ref.double))</span><span class="sxs-lookup"><span data-stu-id="59674-109">bounds : ([Double](xref:microsoft.quantum.lang-ref.double),[Double](xref:microsoft.quantum.lang-ref.double))</span></span>

<span data-ttu-id="59674-110">Интервал, в течение которого должно быть найдено локальное минимальное значение.</span><span class="sxs-lookup"><span data-stu-id="59674-110">The interval in which the local minimum is to be found.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="59674-111">Допуск: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="59674-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="59674-112">Точность входных данных функции, которая будет допускаться.</span><span class="sxs-lookup"><span data-stu-id="59674-112">The accuracy in the function input to be tolerated.</span></span>
<span data-ttu-id="59674-113">Поиск локальной Оптима будет продолжен до тех пор, пока интервал не уменьшится по ширине.</span><span class="sxs-lookup"><span data-stu-id="59674-113">The search for local optima will continue until the interval is smaller in width than this tolerance.</span></span>



## <a name="output--univariateoptimizationresult"></a><span data-ttu-id="59674-114">Выходные данные: [унивариатеоптимизатионресулт](xref:Microsoft.Quantum.Optimization.UnivariateOptimizationResult)</span><span class="sxs-lookup"><span data-stu-id="59674-114">Output : [UnivariateOptimizationResult](xref:Microsoft.Quantum.Optimization.UnivariateOptimizationResult)</span></span>

<span data-ttu-id="59674-115">Локальная Оптима заданной функции, расположенная в пределах заданных границ.</span><span class="sxs-lookup"><span data-stu-id="59674-115">A local optima of the given function, located within the given bounds.</span></span>