---
uid: Microsoft.Quantum.Measurement.MeasureWithScratch
title: Операция Меасуревисскратч
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureWithScratch
qsharp.summary: Measures the given Pauli operator using an explicit scratch qubit to perform the measurement.
ms.openlocfilehash: 4173aa9daac08a3febdfcbf12dc236f797685436
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854665"
---
# <a name="measurewithscratch-operation"></a><span data-ttu-id="e34b1-102">Операция Меасуревисскратч</span><span class="sxs-lookup"><span data-stu-id="e34b1-102">MeasureWithScratch operation</span></span>

<span data-ttu-id="e34b1-103">Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="e34b1-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="e34b1-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e34b1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e34b1-105">Измеряет заданный оператор Паули, используя явное значение "кубит" для выполнения измерения.</span><span class="sxs-lookup"><span data-stu-id="e34b1-105">Measures the given Pauli operator using an explicit scratch qubit to perform the measurement.</span></span>

```qsharp
operation MeasureWithScratch (pauli : Pauli[], target : Qubit[]) : Result
```


## <a name="input"></a><span data-ttu-id="e34b1-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e34b1-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="e34b1-107">Паули: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="e34b1-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="e34b1-108">Оператор Multi-кубит Паули, указанный в качестве массива операторов с одним кубит Паули.</span><span class="sxs-lookup"><span data-stu-id="e34b1-108">A multi-qubit Pauli operator specified as an array of single-qubit Pauli operators.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="e34b1-109">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="e34b1-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e34b1-110">Регистр кубит для измерения.</span><span class="sxs-lookup"><span data-stu-id="e34b1-110">Qubit register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="e34b1-111">Выходные данные __: <Result> Недопустимый__</span><span class="sxs-lookup"><span data-stu-id="e34b1-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="e34b1-112">Результат измерения данного оператора Паули в `target` регистре.</span><span class="sxs-lookup"><span data-stu-id="e34b1-112">The result of measuring the given Pauli operator on the `target` register.</span></span>