---
uid: Microsoft.Quantum.Simulation.IntToPauli
title: Функция Инттопаули
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntToPauli
qsharp.summary: Converts a integer to a single-qubit Pauli operator.
ms.openlocfilehash: f0f1186f14a0dc30bb34bd29f148cdc830fd1337
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733704"
---
# <a name="inttopauli-function"></a><span data-ttu-id="7ad72-102">Функция Инттопаули</span><span class="sxs-lookup"><span data-stu-id="7ad72-102">IntToPauli function</span></span>

<span data-ttu-id="7ad72-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="7ad72-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="7ad72-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7ad72-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7ad72-105">Преобразует целое число в один кубит Паули оператор.</span><span class="sxs-lookup"><span data-stu-id="7ad72-105">Converts a integer to a single-qubit Pauli operator.</span></span>

```qsharp
function IntToPauli (idx : Int) : Pauli
```


## <a name="input"></a><span data-ttu-id="7ad72-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7ad72-106">Input</span></span>

### <a name="idx--int"></a><span data-ttu-id="7ad72-107">IDX: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7ad72-107">idx : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7ad72-108">Целое число в диапазоне `0..3` для преобразования в операторы Паули.</span><span class="sxs-lookup"><span data-stu-id="7ad72-108">Integer in the range `0..3` to be converted to Pauli operators.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="7ad72-109">Выходные данные: [Паули](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="7ad72-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="7ad72-110">`Pauli`Оператор, заданный параметром `[PauliI, PauliX, PauliY, PauliZ][idx]` .</span><span class="sxs-lookup"><span data-stu-id="7ad72-110">A `Pauli` operator given by `[PauliI, PauliX, PauliY, PauliZ][idx]`.</span></span>