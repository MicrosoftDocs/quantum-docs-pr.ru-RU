---
uid: Microsoft.Quantum.MachineLearning.InputEncoder
title: Функция Инпутенкодер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state.
ms.openlocfilehash: 019161c0ef6cdec6875518ab58c8159b0f142149
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211752"
---
# <a name="inputencoder-function"></a><span data-ttu-id="dd41a-102">Функция Инпутенкодер</span><span class="sxs-lookup"><span data-stu-id="dd41a-102">InputEncoder function</span></span>

<span data-ttu-id="dd41a-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="dd41a-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="dd41a-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="dd41a-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="dd41a-105">Учитывая набор коэффициентов и допустимости, возвращает операцию подготовки состояния, которая подготавливает каждый коэффициент в качестве соответствующей амплитуды вычислительного состояния.</span><span class="sxs-lookup"><span data-stu-id="dd41a-105">Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state.</span></span>

```qsharp
function InputEncoder (coefficients : Double[]) : Microsoft.Quantum.MachineLearning.StateGenerator
```


## <a name="input"></a><span data-ttu-id="dd41a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="dd41a-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="dd41a-107">коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="dd41a-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="dd41a-108">Коэффициенты для кодирования во входное состояние.</span><span class="sxs-lookup"><span data-stu-id="dd41a-108">The coefficients to be encoded into an input state.</span></span>



## <a name="output--stategenerator"></a><span data-ttu-id="dd41a-109">Выходные данные: [статеженератор](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span><span class="sxs-lookup"><span data-stu-id="dd41a-109">Output : [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span></span>

<span data-ttu-id="dd41a-110">Операция подготовки состояния, которая подготавливает заданные коэффициенты в качестве входного состояния для заданного регистра.</span><span class="sxs-lookup"><span data-stu-id="dd41a-110">A state preparation operation that prepares the given coefficients as an input state on a given register.</span></span>