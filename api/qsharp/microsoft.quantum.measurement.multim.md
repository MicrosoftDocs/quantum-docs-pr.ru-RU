---
uid: Microsoft.Quantum.Measurement.MultiM
title: Операция Мултим
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MultiM
qsharp.summary: Measures each qubit in a given array in the standard basis.
ms.openlocfilehash: b7f4083bde84c204611ea33746ae351a3e27b946
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856999"
---
# <a name="multim-operation"></a><span data-ttu-id="025cd-102">Операция Мултим</span><span class="sxs-lookup"><span data-stu-id="025cd-102">MultiM operation</span></span>

<span data-ttu-id="025cd-103">Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="025cd-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="025cd-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="025cd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="025cd-105">Измеряет каждый кубит в заданном массиве в стандартном уровне.</span><span class="sxs-lookup"><span data-stu-id="025cd-105">Measures each qubit in a given array in the standard basis.</span></span>

```qsharp
operation MultiM (targets : Qubit[]) : Result[]
```


## <a name="input"></a><span data-ttu-id="025cd-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="025cd-106">Input</span></span>

### <a name="targets--qubit"></a><span data-ttu-id="025cd-107">целевые объекты: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="025cd-107">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="025cd-108">Массив Кубитс для измерения.</span><span class="sxs-lookup"><span data-stu-id="025cd-108">An array of qubits to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="025cd-109">Выходные данные __: <Result> Недопустимый__[]</span><span class="sxs-lookup"><span data-stu-id="025cd-109">Output : __invalid<Result>__[]</span></span>

<span data-ttu-id="025cd-110">Массив результатов измерения.</span><span class="sxs-lookup"><span data-stu-id="025cd-110">An array of measurement results.</span></span>