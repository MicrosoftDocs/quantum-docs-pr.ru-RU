---
uid: Microsoft.Quantum.Simulation.PauliStringFromGenIdx
title: Функция Паулистрингфромженидкс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliStringFromGenIdx
qsharp.summary: Extracts the Pauli string and its qubit indices of a Pauli term described by a `GeneratorIndex`.
ms.openlocfilehash: 33da4bc3d7e58b87aef75b453b6af09a51214923
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710540"
---
# <a name="paulistringfromgenidx-function"></a><span data-ttu-id="3e9fe-102">Функция Паулистрингфромженидкс</span><span class="sxs-lookup"><span data-stu-id="3e9fe-102">PauliStringFromGenIdx function</span></span>

<span data-ttu-id="3e9fe-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="3e9fe-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="3e9fe-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3e9fe-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3e9fe-105">Извлекает строку Паули и ее индексы кубит для термина Паули, описанного в `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="3e9fe-105">Extracts the Pauli string and its qubit indices of a Pauli term described by a `GeneratorIndex`.</span></span>

```qsharp
function PauliStringFromGenIdx (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : (Pauli[], Int[])
```


## <a name="input"></a><span data-ttu-id="3e9fe-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3e9fe-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="3e9fe-107">Женераториндекс: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="3e9fe-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="3e9fe-108">`GeneratorIndex` тип, который кодирует термин Паули.</span><span class="sxs-lookup"><span data-stu-id="3e9fe-108">`GeneratorIndex` type that encodes a Pauli term.</span></span>



## <a name="output--pauliint"></a><span data-ttu-id="3e9fe-109">Выходные данные: ([Паули](xref:microsoft.quantum.lang-ref.pauli)[],[int](xref:microsoft.quantum.lang-ref.int)[])</span><span class="sxs-lookup"><span data-stu-id="3e9fe-109">Output : ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Int](xref:microsoft.quantum.lang-ref.int)[])</span></span>

<span data-ttu-id="3e9fe-110">Строка Паули термина, описываемая `GeneratorIndex` , и индексы для Кубитс, с которой он работает.</span><span class="sxs-lookup"><span data-stu-id="3e9fe-110">The Pauli string of the term described by a `GeneratorIndex`, and indices to the qubits it acts on.</span></span>