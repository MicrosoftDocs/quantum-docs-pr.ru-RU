---
uid: Microsoft.Quantum.Measurement.MResetZ
title: Операция Мресетз
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetZ
qsharp.summary: Measures a single qubit in the Z basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: fc9ba6576b56d7df1a57334e1da46b9c48376ecb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853740"
---
# <a name="mresetz-operation"></a><span data-ttu-id="ed9ba-102">Операция Мресетз</span><span class="sxs-lookup"><span data-stu-id="ed9ba-102">MResetZ operation</span></span>

<span data-ttu-id="ed9ba-103">Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="ed9ba-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="ed9ba-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="ed9ba-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="ed9ba-105">Измеряет один кубит в Z-координате и сбрасывает его в фиксированное начальное состояние после измерения.</span><span class="sxs-lookup"><span data-stu-id="ed9ba-105">Measures a single qubit in the Z basis, and resets it to a fixed initial state following the measurement.</span></span>

```qsharp
operation MResetZ (target : Qubit) : Result
```


## <a name="description"></a><span data-ttu-id="ed9ba-106">Описание</span><span class="sxs-lookup"><span data-stu-id="ed9ba-106">Description</span></span>

<span data-ttu-id="ed9ba-107">Выполняет кубит измерение в $Z $-of и гарантирует, что кубит возвращается в $ \кет {0} $ после измерения.</span><span class="sxs-lookup"><span data-stu-id="ed9ba-107">Performs a single-qubit measurement in the $Z$-basis, and ensures that the qubit is returned to $\ket{0}$ following the measurement.</span></span>

## <a name="input"></a><span data-ttu-id="ed9ba-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ed9ba-108">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="ed9ba-109">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="ed9ba-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="ed9ba-110">Один кубит, который необходимо измерять.</span><span class="sxs-lookup"><span data-stu-id="ed9ba-110">A single qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="ed9ba-111">Выходные данные __: <Result> Недопустимый__</span><span class="sxs-lookup"><span data-stu-id="ed9ba-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="ed9ba-112">Результат измерения `target` в паули $Z $.</span><span class="sxs-lookup"><span data-stu-id="ed9ba-112">The result of measuring `target` in the Pauli $Z$ basis.</span></span>