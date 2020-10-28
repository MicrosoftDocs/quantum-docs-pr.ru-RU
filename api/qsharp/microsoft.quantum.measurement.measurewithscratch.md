---
uid: Microsoft.Quantum.Measurement.MeasureWithScratch
title: Операция Меасуревисскратч
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureWithScratch
qsharp.summary: Measures the given Pauli operator using an explicit scratch qubit to perform the measurement.
ms.openlocfilehash: 1ee25dbccd5bddde406cf8ed84dff77d96d7804e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730985"
---
# <a name="measurewithscratch-operation"></a><span data-ttu-id="d21f7-102">Операция Меасуревисскратч</span><span class="sxs-lookup"><span data-stu-id="d21f7-102">MeasureWithScratch operation</span></span>

<span data-ttu-id="d21f7-103">Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="d21f7-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="d21f7-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d21f7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d21f7-105">Измеряет заданный оператор Паули, используя явное значение "кубит" для выполнения измерения.</span><span class="sxs-lookup"><span data-stu-id="d21f7-105">Measures the given Pauli operator using an explicit scratch qubit to perform the measurement.</span></span>

```qsharp
operation MeasureWithScratch (pauli : Pauli[], target : Qubit[]) : Result
```


## <a name="input"></a><span data-ttu-id="d21f7-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d21f7-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="d21f7-107">Паули: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="d21f7-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="d21f7-108">Оператор Multi-кубит Паули, указанный в качестве массива операторов с одним кубит Паули.</span><span class="sxs-lookup"><span data-stu-id="d21f7-108">A multi-qubit Pauli operator specified as an array of single-qubit Pauli operators.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="d21f7-109">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d21f7-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d21f7-110">Регистр кубит для измерения.</span><span class="sxs-lookup"><span data-stu-id="d21f7-110">Qubit register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="d21f7-111">Выходные данные __: <Result> Недопустимый__</span><span class="sxs-lookup"><span data-stu-id="d21f7-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="d21f7-112">Результат измерения данного оператора Паули в `target` регистре.</span><span class="sxs-lookup"><span data-stu-id="d21f7-112">The result of measuring the given Pauli operator on the `target` register.</span></span>