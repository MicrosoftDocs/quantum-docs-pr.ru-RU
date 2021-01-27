---
uid: Microsoft.Quantum.Simulation.PauliStringFromGenIdx
title: Функция Паулистрингфромженидкс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliStringFromGenIdx
qsharp.summary: Extracts the Pauli string and its qubit indices of a Pauli term described by a `GeneratorIndex`.
ms.openlocfilehash: 048f91411099d24f3c0c5fd8ae3703779e7ab8a2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847910"
---
# <a name="paulistringfromgenidx-function"></a><span data-ttu-id="48fcf-102">Функция Паулистрингфромженидкс</span><span class="sxs-lookup"><span data-stu-id="48fcf-102">PauliStringFromGenIdx function</span></span>

<span data-ttu-id="48fcf-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="48fcf-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="48fcf-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="48fcf-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="48fcf-105">Извлекает строку Паули и ее индексы кубит для термина Паули, описанного в `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="48fcf-105">Extracts the Pauli string and its qubit indices of a Pauli term described by a `GeneratorIndex`.</span></span>

```qsharp
function PauliStringFromGenIdx (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : (Pauli[], Int[])
```


## <a name="input"></a><span data-ttu-id="48fcf-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="48fcf-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="48fcf-107">Женераториндекс: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="48fcf-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="48fcf-108">`GeneratorIndex` тип, который кодирует термин Паули.</span><span class="sxs-lookup"><span data-stu-id="48fcf-108">`GeneratorIndex` type that encodes a Pauli term.</span></span>



## <a name="output--pauliint"></a><span data-ttu-id="48fcf-109">Выходные данные: ([Паули](xref:microsoft.quantum.lang-ref.pauli)[],[int](xref:microsoft.quantum.lang-ref.int)[])</span><span class="sxs-lookup"><span data-stu-id="48fcf-109">Output : ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Int](xref:microsoft.quantum.lang-ref.int)[])</span></span>

<span data-ttu-id="48fcf-110">Строка Паули термина, описываемая `GeneratorIndex` , и индексы для Кубитс, с которой он работает.</span><span class="sxs-lookup"><span data-stu-id="48fcf-110">The Pauli string of the term described by a `GeneratorIndex`, and indices to the qubits it acts on.</span></span>