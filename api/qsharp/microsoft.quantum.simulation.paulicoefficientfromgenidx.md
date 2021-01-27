---
uid: Microsoft.Quantum.Simulation.PauliCoefficientFromGenIdx
title: Функция ПауликоеффиЦиентфромженидкс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliCoefficientFromGenIdx
qsharp.summary: Extracts the coefficient of a Pauli term described by a `GeneratorIndex`.
ms.openlocfilehash: eb4f7a538e85ade4b095aa3ea5eab4448eda2491
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847994"
---
# <a name="paulicoefficientfromgenidx-function"></a><span data-ttu-id="fdbef-102">Функция ПауликоеффиЦиентфромженидкс</span><span class="sxs-lookup"><span data-stu-id="fdbef-102">PauliCoefficientFromGenIdx function</span></span>

<span data-ttu-id="fdbef-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="fdbef-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="fdbef-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fdbef-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fdbef-105">Извлекает коэффициент Паули термина, описываемого `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="fdbef-105">Extracts the coefficient of a Pauli term described by a `GeneratorIndex`.</span></span>

```qsharp
function PauliCoefficientFromGenIdx (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Double
```


## <a name="input"></a><span data-ttu-id="fdbef-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fdbef-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="fdbef-107">Женераториндекс: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="fdbef-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="fdbef-108">`GeneratorIndex` тип, который кодирует термин Паули.</span><span class="sxs-lookup"><span data-stu-id="fdbef-108">`GeneratorIndex` type that encodes a Pauli term.</span></span>



## <a name="output--double"></a><span data-ttu-id="fdbef-109">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fdbef-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fdbef-110">Коэффициент термина, описываемого `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="fdbef-110">The coefficient of the term described by a `GeneratorIndex`.</span></span>