---
uid: Microsoft.Quantum.Simulation.PauliCoefficientFromGenIdx
title: Функция ПауликоеффиЦиентфромженидкс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliCoefficientFromGenIdx
qsharp.summary: Extracts the coefficient of a Pauli term described by a `GeneratorIndex`.
ms.openlocfilehash: 5bbc8d6113fb36bfd4050b98538bb61bbac02185
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730912"
---
# <a name="paulicoefficientfromgenidx-function"></a><span data-ttu-id="fa00f-102">Функция ПауликоеффиЦиентфромженидкс</span><span class="sxs-lookup"><span data-stu-id="fa00f-102">PauliCoefficientFromGenIdx function</span></span>

<span data-ttu-id="fa00f-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="fa00f-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="fa00f-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fa00f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fa00f-105">Извлекает коэффициент Паули термина, описываемого `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="fa00f-105">Extracts the coefficient of a Pauli term described by a `GeneratorIndex`.</span></span>

```qsharp
function PauliCoefficientFromGenIdx (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Double
```


## <a name="input"></a><span data-ttu-id="fa00f-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fa00f-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="fa00f-107">Женераториндекс: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="fa00f-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="fa00f-108">`GeneratorIndex` тип, который кодирует термин Паули.</span><span class="sxs-lookup"><span data-stu-id="fa00f-108">`GeneratorIndex` type that encodes a Pauli term.</span></span>



## <a name="output--double"></a><span data-ttu-id="fa00f-109">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fa00f-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fa00f-110">Коэффициент термина, описываемого `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="fa00f-110">The coefficient of the term described by a `GeneratorIndex`.</span></span>