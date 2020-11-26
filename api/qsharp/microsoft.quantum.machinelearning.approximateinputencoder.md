---
uid: Microsoft.Quantum.MachineLearning.ApproximateInputEncoder
title: Функция Аппроксиматеинпутенкодер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ApproximateInputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state, up to the given tolerance.
ms.openlocfilehash: 2e39318cfaf3321c33b08f742bb25a9276b7e660
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196605"
---
# <a name="approximateinputencoder-function"></a><span data-ttu-id="883e1-102">Функция Аппроксиматеинпутенкодер</span><span class="sxs-lookup"><span data-stu-id="883e1-102">ApproximateInputEncoder function</span></span>

<span data-ttu-id="883e1-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="883e1-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="883e1-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="883e1-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="883e1-105">Учитывая набор коэффициентов и допустимости, возвращает операцию подготовки состояния, которая подготавливает каждый коэффициент в качестве соответствующей амплитуды вычислительного состояния, вплоть до заданного допуска.</span><span class="sxs-lookup"><span data-stu-id="883e1-105">Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state, up to the given tolerance.</span></span>

```qsharp
function ApproximateInputEncoder (tolerance : Double, coefficients : Double[]) : Microsoft.Quantum.MachineLearning.StateGenerator
```


## <a name="input"></a><span data-ttu-id="883e1-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="883e1-106">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="883e1-107">Допуск: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="883e1-107">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="883e1-108">Отклонение аппроксимации, используемое для кодирования заданных коэффициентов в входное состояние.</span><span class="sxs-lookup"><span data-stu-id="883e1-108">The approximation tolerance to be used in encoding the given coefficients into an input state.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="883e1-109">коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="883e1-109">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="883e1-110">Коэффициенты для кодирования во входное состояние.</span><span class="sxs-lookup"><span data-stu-id="883e1-110">The coefficients to be encoded into an input state.</span></span>



## <a name="output--stategenerator"></a><span data-ttu-id="883e1-111">Выходные данные: [статеженератор](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span><span class="sxs-lookup"><span data-stu-id="883e1-111">Output : [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span></span>

<span data-ttu-id="883e1-112">Операция подготовки состояния, которая подготавливает заданные коэффициенты в качестве входного состояния для заданного регистра.</span><span class="sxs-lookup"><span data-stu-id="883e1-112">A state preparation operation that prepares the given coefficients as an input state on a given register.</span></span>