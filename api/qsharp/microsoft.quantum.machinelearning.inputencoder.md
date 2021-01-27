---
uid: Microsoft.Quantum.MachineLearning.InputEncoder
title: Функция Инпутенкодер
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state.
ms.openlocfilehash: ed70d9f24af06f8918083307c98a5f6c4671f1c3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852939"
---
# <a name="inputencoder-function"></a><span data-ttu-id="05b8f-102">Функция Инпутенкодер</span><span class="sxs-lookup"><span data-stu-id="05b8f-102">InputEncoder function</span></span>

<span data-ttu-id="05b8f-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="05b8f-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="05b8f-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="05b8f-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="05b8f-105">Учитывая набор коэффициентов и допустимости, возвращает операцию подготовки состояния, которая подготавливает каждый коэффициент в качестве соответствующей амплитуды вычислительного состояния.</span><span class="sxs-lookup"><span data-stu-id="05b8f-105">Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state.</span></span>

```qsharp
function InputEncoder (coefficients : Double[]) : Microsoft.Quantum.MachineLearning.StateGenerator
```


## <a name="input"></a><span data-ttu-id="05b8f-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="05b8f-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="05b8f-107">коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="05b8f-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="05b8f-108">Коэффициенты для кодирования во входное состояние.</span><span class="sxs-lookup"><span data-stu-id="05b8f-108">The coefficients to be encoded into an input state.</span></span>



## <a name="output--stategenerator"></a><span data-ttu-id="05b8f-109">Выходные данные: [статеженератор](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span><span class="sxs-lookup"><span data-stu-id="05b8f-109">Output : [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span></span>

<span data-ttu-id="05b8f-110">Операция подготовки состояния, которая подготавливает заданные коэффициенты в качестве входного состояния для заданного регистра.</span><span class="sxs-lookup"><span data-stu-id="05b8f-110">A state preparation operation that prepares the given coefficients as an input state on a given register.</span></span>