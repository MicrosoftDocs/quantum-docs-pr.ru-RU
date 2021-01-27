---
uid: Microsoft.Quantum.Simulation.IntsToPaulis
title: Функция Интстопаулис
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntsToPaulis
qsharp.summary: Converts an array of integers to an array of single-qubit Pauli operators.
ms.openlocfilehash: 6904054bb1aff3a57c80882694b4c217812b2b81
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842227"
---
# <a name="intstopaulis-function"></a><span data-ttu-id="2a19e-102">Функция Интстопаулис</span><span class="sxs-lookup"><span data-stu-id="2a19e-102">IntsToPaulis function</span></span>

<span data-ttu-id="2a19e-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="2a19e-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="2a19e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2a19e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2a19e-105">Преобразует массив целых чисел в массив однокубитных операторов Паули.</span><span class="sxs-lookup"><span data-stu-id="2a19e-105">Converts an array of integers to an array of single-qubit Pauli operators.</span></span>

```qsharp
function IntsToPaulis (ints : Int[]) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="2a19e-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2a19e-106">Input</span></span>

### <a name="ints--int"></a><span data-ttu-id="2a19e-107">ints: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="2a19e-107">ints : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="2a19e-108">Массив целых чисел в диапазоне, `0..3`  который должен быть преобразован в операторы Паули.</span><span class="sxs-lookup"><span data-stu-id="2a19e-108">Array of integers in the range `0..3`  to be converted to Pauli operators.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="2a19e-109">Выходные данные: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="2a19e-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="2a19e-110">Массив `paulis` операторов Паули `Pauli[]` имеет одинаковую длину `ints` , `paulis[idxPauli]` равную элементу, `[PauliI, PauliX, PauliY, PauliZ]` заданному параметром `ints[idxPauli]` .</span><span class="sxs-lookup"><span data-stu-id="2a19e-110">An array `paulis` of Pauli operators `Pauli[]` the same length as `ints` such that `paulis[idxPauli]` is equal to the element of `[PauliI, PauliX, PauliY, PauliZ]` given by `ints[idxPauli]`.</span></span>