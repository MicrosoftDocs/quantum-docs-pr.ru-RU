---
uid: Microsoft.Quantum.Measurement.MResetX
title: Операция Мресеткс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetX
qsharp.summary: Measures a single qubit in the X basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 44459e681daf1d28ce7d45f91ad59059babe5716
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853753"
---
# <a name="mresetx-operation"></a><span data-ttu-id="bd885-102">Операция Мресеткс</span><span class="sxs-lookup"><span data-stu-id="bd885-102">MResetX operation</span></span>

<span data-ttu-id="bd885-103">Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="bd885-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="bd885-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="bd885-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="bd885-105">Измеряет один кубит в базе X и сбрасывает его в фиксированное начальное состояние после измерения.</span><span class="sxs-lookup"><span data-stu-id="bd885-105">Measures a single qubit in the X basis, and resets it to a fixed initial state following the measurement.</span></span>

```qsharp
operation MResetX (target : Qubit) : Result
```


## <a name="description"></a><span data-ttu-id="bd885-106">Описание</span><span class="sxs-lookup"><span data-stu-id="bd885-106">Description</span></span>

<span data-ttu-id="bd885-107">Выполняет кубит измерение в $X $-of и гарантирует, что кубит возвращается в $ \кет {0} $ после измерения.</span><span class="sxs-lookup"><span data-stu-id="bd885-107">Performs a single-qubit measurement in the $X$-basis, and ensures that the qubit is returned to $\ket{0}$ following the measurement.</span></span>

## <a name="input"></a><span data-ttu-id="bd885-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bd885-108">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="bd885-109">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="bd885-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="bd885-110">Один кубит, который необходимо измерять.</span><span class="sxs-lookup"><span data-stu-id="bd885-110">A single qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="bd885-111">Выходные данные __: <Result> Недопустимый__</span><span class="sxs-lookup"><span data-stu-id="bd885-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="bd885-112">Результат измерения `target` в паули $X $.</span><span class="sxs-lookup"><span data-stu-id="bd885-112">The result of measuring `target` in the Pauli $X$ basis.</span></span>