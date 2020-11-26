---
uid: Microsoft.Quantum.Measurement.MResetZ
title: Операция Мресетз
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetZ
qsharp.summary: Measures a single qubit in the Z basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 494f11c8129175ddd84c6539f5e9df1a758e8a82
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194140"
---
# <a name="mresetz-operation"></a><span data-ttu-id="a7f8b-102">Операция Мресетз</span><span class="sxs-lookup"><span data-stu-id="a7f8b-102">MResetZ operation</span></span>

<span data-ttu-id="a7f8b-103">Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="a7f8b-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="a7f8b-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="a7f8b-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="a7f8b-105">Измеряет один кубит в Z-координате и сбрасывает его в фиксированное начальное состояние после измерения.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-105">Measures a single qubit in the Z basis, and resets it to a fixed initial state following the measurement.</span></span>

```qsharp
operation MResetZ (target : Qubit) : Result
```


## <a name="description"></a><span data-ttu-id="a7f8b-106">Описание</span><span class="sxs-lookup"><span data-stu-id="a7f8b-106">Description</span></span>

<span data-ttu-id="a7f8b-107">Выполняет кубит измерение в $Z $-of и гарантирует, что кубит возвращается в $ \кет {0} $ после измерения.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-107">Performs a single-qubit measurement in the $Z$-basis, and ensures that the qubit is returned to $\ket{0}$ following the measurement.</span></span>

## <a name="input"></a><span data-ttu-id="a7f8b-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a7f8b-108">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="a7f8b-109">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a7f8b-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a7f8b-110">Один кубит, который необходимо измерять.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-110">A single qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="a7f8b-111">Выходные данные __: <Result> Недопустимый__</span><span class="sxs-lookup"><span data-stu-id="a7f8b-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="a7f8b-112">Результат измерения `target` в паули $Z $.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-112">The result of measuring `target` in the Pauli $Z$ basis.</span></span>