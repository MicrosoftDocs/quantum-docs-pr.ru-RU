---
uid: Microsoft.Quantum.Measurement.MResetY
title: Операция Мресети
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetY
qsharp.summary: Measures a single qubit in the Y basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 2e41e76a46b68178a8a22b39131d6ca2a8c50b64
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854634"
---
# <a name="mresety-operation"></a><span data-ttu-id="6b21f-102">Операция Мресети</span><span class="sxs-lookup"><span data-stu-id="6b21f-102">MResetY operation</span></span>

<span data-ttu-id="6b21f-103">Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="6b21f-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="6b21f-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="6b21f-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="6b21f-105">Измеряет один кубит в базе Y и сбрасывает его в фиксированное начальное состояние после измерения.</span><span class="sxs-lookup"><span data-stu-id="6b21f-105">Measures a single qubit in the Y basis, and resets it to a fixed initial state following the measurement.</span></span>

```qsharp
operation MResetY (target : Qubit) : Result
```


## <a name="description"></a><span data-ttu-id="6b21f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="6b21f-106">Description</span></span>

<span data-ttu-id="6b21f-107">Выполняет кубит измерение в $Y $-of и гарантирует, что кубит возвращается в $ \кет {0} $ после измерения.</span><span class="sxs-lookup"><span data-stu-id="6b21f-107">Performs a single-qubit measurement in the $Y$-basis, and ensures that the qubit is returned to $\ket{0}$ following the measurement.</span></span>

## <a name="input"></a><span data-ttu-id="6b21f-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6b21f-108">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="6b21f-109">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="6b21f-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="6b21f-110">Один кубит, который необходимо измерять.</span><span class="sxs-lookup"><span data-stu-id="6b21f-110">A single qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="6b21f-111">Выходные данные __: <Result> Недопустимый__</span><span class="sxs-lookup"><span data-stu-id="6b21f-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="6b21f-112">Результат измерения `target` в паули $Y $.</span><span class="sxs-lookup"><span data-stu-id="6b21f-112">The result of measuring `target` in the Pauli $Y$ basis.</span></span>