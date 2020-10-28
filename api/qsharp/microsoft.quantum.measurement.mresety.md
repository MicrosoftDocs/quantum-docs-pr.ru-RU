---
uid: Microsoft.Quantum.Measurement.MResetY
title: Операция Мресети
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetY
qsharp.summary: Measures a single qubit in the Y basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 48aba7317d0e48d089ec6c4814efdee51bb8e2ed
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733793"
---
# <a name="mresety-operation"></a><span data-ttu-id="a6a51-102">Операция Мресети</span><span class="sxs-lookup"><span data-stu-id="a6a51-102">MResetY operation</span></span>

<span data-ttu-id="a6a51-103">Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="a6a51-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="a6a51-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a6a51-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a6a51-105">Измеряет один кубит в базе Y и сбрасывает его в фиксированное начальное состояние после измерения.</span><span class="sxs-lookup"><span data-stu-id="a6a51-105">Measures a single qubit in the Y basis, and resets it to a fixed initial state following the measurement.</span></span>

```qsharp
operation MResetY (target : Qubit) : Result
```


## <a name="description"></a><span data-ttu-id="a6a51-106">Описание</span><span class="sxs-lookup"><span data-stu-id="a6a51-106">Description</span></span>

<span data-ttu-id="a6a51-107">Выполняет кубит измерение в $Y $-of и гарантирует, что кубит возвращается в $ \кет {0} $ после измерения.</span><span class="sxs-lookup"><span data-stu-id="a6a51-107">Performs a single-qubit measurement in the $Y$-basis, and ensures that the qubit is returned to $\ket{0}$ following the measurement.</span></span>

## <a name="input"></a><span data-ttu-id="a6a51-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a6a51-108">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="a6a51-109">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a6a51-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a6a51-110">Один кубит, который необходимо измерять.</span><span class="sxs-lookup"><span data-stu-id="a6a51-110">A single qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="a6a51-111">Выходные данные __: <Result> Недопустимый__</span><span class="sxs-lookup"><span data-stu-id="a6a51-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="a6a51-112">Результат измерения `target` в паули $Y $.</span><span class="sxs-lookup"><span data-stu-id="a6a51-112">The result of measuring `target` in the Pauli $Y$ basis.</span></span>