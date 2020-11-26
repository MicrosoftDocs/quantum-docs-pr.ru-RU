---
uid: Microsoft.Quantum.Simulation.PauliCoefficientFromGenIdx
title: Функция ПауликоеффиЦиентфромженидкс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliCoefficientFromGenIdx
qsharp.summary: Extracts the coefficient of a Pauli term described by a `GeneratorIndex`.
ms.openlocfilehash: 59ddadabb5c77cdb0d2e3620a09433992e85f663
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225063"
---
# <a name="paulicoefficientfromgenidx-function"></a><span data-ttu-id="c7112-102">Функция ПауликоеффиЦиентфромженидкс</span><span class="sxs-lookup"><span data-stu-id="c7112-102">PauliCoefficientFromGenIdx function</span></span>

<span data-ttu-id="c7112-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="c7112-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="c7112-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c7112-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c7112-105">Извлекает коэффициент Паули термина, описываемого `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="c7112-105">Extracts the coefficient of a Pauli term described by a `GeneratorIndex`.</span></span>

```qsharp
function PauliCoefficientFromGenIdx (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Double
```


## <a name="input"></a><span data-ttu-id="c7112-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c7112-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="c7112-107">Женераториндекс: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="c7112-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="c7112-108">`GeneratorIndex` тип, который кодирует термин Паули.</span><span class="sxs-lookup"><span data-stu-id="c7112-108">`GeneratorIndex` type that encodes a Pauli term.</span></span>



## <a name="output--double"></a><span data-ttu-id="c7112-109">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c7112-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c7112-110">Коэффициент термина, описываемого `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="c7112-110">The coefficient of the term described by a `GeneratorIndex`.</span></span>