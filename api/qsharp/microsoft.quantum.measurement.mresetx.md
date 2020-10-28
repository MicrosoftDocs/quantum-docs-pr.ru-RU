---
uid: Microsoft.Quantum.Measurement.MResetX
title: Операция Мресеткс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetX
qsharp.summary: Measures a single qubit in the X basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: a16d7405388b560edcdb6c36b6668791f7ba1398
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733792"
---
# <a name="mresetx-operation"></a><span data-ttu-id="b0654-102">Операция Мресеткс</span><span class="sxs-lookup"><span data-stu-id="b0654-102">MResetX operation</span></span>

<span data-ttu-id="b0654-103">Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="b0654-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="b0654-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b0654-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b0654-105">Измеряет один кубит в базе X и сбрасывает его в фиксированное начальное состояние после измерения.</span><span class="sxs-lookup"><span data-stu-id="b0654-105">Measures a single qubit in the X basis, and resets it to a fixed initial state following the measurement.</span></span>

```qsharp
operation MResetX (target : Qubit) : Result
```


## <a name="description"></a><span data-ttu-id="b0654-106">Описание</span><span class="sxs-lookup"><span data-stu-id="b0654-106">Description</span></span>

<span data-ttu-id="b0654-107">Выполняет кубит измерение в $X $-of и гарантирует, что кубит возвращается в $ \кет {0} $ после измерения.</span><span class="sxs-lookup"><span data-stu-id="b0654-107">Performs a single-qubit measurement in the $X$-basis, and ensures that the qubit is returned to $\ket{0}$ following the measurement.</span></span>

## <a name="input"></a><span data-ttu-id="b0654-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b0654-108">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="b0654-109">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="b0654-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="b0654-110">Один кубит, который необходимо измерять.</span><span class="sxs-lookup"><span data-stu-id="b0654-110">A single qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="b0654-111">Выходные данные __: <Result> Недопустимый__</span><span class="sxs-lookup"><span data-stu-id="b0654-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="b0654-112">Результат измерения `target` в паули $X $.</span><span class="sxs-lookup"><span data-stu-id="b0654-112">The result of measuring `target` in the Pauli $X$ basis.</span></span>