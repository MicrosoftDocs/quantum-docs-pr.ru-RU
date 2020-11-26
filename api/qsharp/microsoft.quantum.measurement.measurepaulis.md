---
uid: Microsoft.Quantum.Measurement.MeasurePaulis
title: Операция Меасурепаулис
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasurePaulis
qsharp.summary: Given an array of multi-qubit Pauli operators, measures each using a specified measurement gadget, then returns the array of results.
ms.openlocfilehash: 4faaf78f24fa28ae5e4f701b80d9297c910b975e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194225"
---
# <a name="measurepaulis-operation"></a><span data-ttu-id="ad5d9-102">Операция Меасурепаулис</span><span class="sxs-lookup"><span data-stu-id="ad5d9-102">MeasurePaulis operation</span></span>

<span data-ttu-id="ad5d9-103">Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="ad5d9-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="ad5d9-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ad5d9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ad5d9-105">Учитывая массив операторов кубит Паули, измеряет каждый с помощью указанного мини-приложения измерения, а затем возвращает массив результатов.</span><span class="sxs-lookup"><span data-stu-id="ad5d9-105">Given an array of multi-qubit Pauli operators, measures each using a specified measurement gadget, then returns the array of results.</span></span>

```qsharp
operation MeasurePaulis (paulis : Pauli[][], target : Qubit[], gadget : ((Pauli[], Qubit[]) => Result)) : Result[]
```


## <a name="input"></a><span data-ttu-id="ad5d9-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ad5d9-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="ad5d9-107">Пол: [Паули](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="ad5d9-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="ad5d9-108">Массив кубит Паули операторов для измерения.</span><span class="sxs-lookup"><span data-stu-id="ad5d9-108">Array of multi-qubit Pauli operators to measure.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="ad5d9-109">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ad5d9-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="ad5d9-110">Регистрация для измерения заданных операторов.</span><span class="sxs-lookup"><span data-stu-id="ad5d9-110">Register on which to measure the given operators.</span></span>


### <a name="gadget--pauliqubit--__invalidresult__"></a><span data-ttu-id="ad5d9-111">Мини-приложение: ([Паули](xref:microsoft.quantum.lang-ref.pauli)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) __= <Result> Недопустимый__></span><span class="sxs-lookup"><span data-stu-id="ad5d9-111">gadget : ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __invalid<Result>__</span></span> 

<span data-ttu-id="ad5d9-112">Операция, которая выполняет измерение заданного кубит оператора.</span><span class="sxs-lookup"><span data-stu-id="ad5d9-112">Operation which performs the measurement of a given multi-qubit operator.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="ad5d9-113">Выходные данные __: <Result> Недопустимый__[]</span><span class="sxs-lookup"><span data-stu-id="ad5d9-113">Output : __invalid<Result>__[]</span></span>

<span data-ttu-id="ad5d9-114">Массив результатов, полученных из измерения каждого элемента `paulis` в `target` .</span><span class="sxs-lookup"><span data-stu-id="ad5d9-114">The array of results obtained from measuring each element of `paulis` on `target`.</span></span>