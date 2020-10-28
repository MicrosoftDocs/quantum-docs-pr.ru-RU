---
uid: Microsoft.Quantum.Simulation.IntsToPaulis
title: Функция Интстопаулис
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntsToPaulis
qsharp.summary: Converts an array of integers to an array of single-qubit Pauli operators.
ms.openlocfilehash: 605257aa7ca39e457127e3c3459b5891145b1863
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709448"
---
# <a name="intstopaulis-function"></a><span data-ttu-id="d0694-102">Функция Интстопаулис</span><span class="sxs-lookup"><span data-stu-id="d0694-102">IntsToPaulis function</span></span>

<span data-ttu-id="d0694-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="d0694-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="d0694-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d0694-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d0694-105">Преобразует массив целых чисел в массив однокубитных операторов Паули.</span><span class="sxs-lookup"><span data-stu-id="d0694-105">Converts an array of integers to an array of single-qubit Pauli operators.</span></span>

```qsharp
function IntsToPaulis (ints : Int[]) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="d0694-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d0694-106">Input</span></span>

### <a name="ints--int"></a><span data-ttu-id="d0694-107">ints: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="d0694-107">ints : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="d0694-108">Массив целых чисел в диапазоне, `0..3`  который должен быть преобразован в операторы Паули.</span><span class="sxs-lookup"><span data-stu-id="d0694-108">Array of integers in the range `0..3`  to be converted to Pauli operators.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="d0694-109">Выходные данные: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="d0694-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="d0694-110">Массив `paulis` операторов Паули `Pauli[]` имеет одинаковую длину `ints` , `paulis[idxPauli]` равную элементу, `[PauliI, PauliX, PauliY, PauliZ]` заданному параметром `ints[idxPauli]` .</span><span class="sxs-lookup"><span data-stu-id="d0694-110">An array `paulis` of Pauli operators `Pauli[]` the same length as `ints` such that `paulis[idxPauli]` is equal to the element of `[PauliI, PauliX, PauliY, PauliZ]` given by `ints[idxPauli]`.</span></span>