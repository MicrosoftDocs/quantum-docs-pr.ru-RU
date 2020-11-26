---
uid: Microsoft.Quantum.Measurement.MultiM
title: Операция Мултим
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MultiM
qsharp.summary: Measures each qubit in a given array in the standard basis.
ms.openlocfilehash: c39601f3e8b272b9341f1789b4c8e7230cb4182c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227001"
---
# <a name="multim-operation"></a><span data-ttu-id="a75af-102">Операция Мултим</span><span class="sxs-lookup"><span data-stu-id="a75af-102">MultiM operation</span></span>

<span data-ttu-id="a75af-103">Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="a75af-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="a75af-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a75af-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a75af-105">Измеряет каждый кубит в заданном массиве в стандартном уровне.</span><span class="sxs-lookup"><span data-stu-id="a75af-105">Measures each qubit in a given array in the standard basis.</span></span>

```qsharp
operation MultiM (targets : Qubit[]) : Result[]
```


## <a name="input"></a><span data-ttu-id="a75af-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a75af-106">Input</span></span>

### <a name="targets--qubit"></a><span data-ttu-id="a75af-107">целевые объекты: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a75af-107">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a75af-108">Массив Кубитс для измерения.</span><span class="sxs-lookup"><span data-stu-id="a75af-108">An array of qubits to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="a75af-109">Выходные данные __: <Result> Недопустимый__[]</span><span class="sxs-lookup"><span data-stu-id="a75af-109">Output : __invalid<Result>__[]</span></span>

<span data-ttu-id="a75af-110">Массив результатов измерения.</span><span class="sxs-lookup"><span data-stu-id="a75af-110">An array of measurement results.</span></span>