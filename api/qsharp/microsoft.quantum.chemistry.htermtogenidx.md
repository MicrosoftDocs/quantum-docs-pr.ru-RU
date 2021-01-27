---
uid: Microsoft.Quantum.Chemistry.HTermToGenIdx
title: Функция Хтермтоженидкс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermToGenIdx
qsharp.summary: Converts a Hamiltonian term in `HTerm` data format to a GeneratorIndex.
ms.openlocfilehash: 46745632e2f6bafad0d7359141522b84f48c039d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839622"
---
# <a name="htermtogenidx-function"></a><span data-ttu-id="23ffa-102">Функция Хтермтоженидкс</span><span class="sxs-lookup"><span data-stu-id="23ffa-102">HTermToGenIdx function</span></span>

<span data-ttu-id="23ffa-103">Пространство имен: [Microsoft. тактов. Химия](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="23ffa-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="23ffa-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="23ffa-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="23ffa-105">Преобразует термин Хамилтониан в `HTerm` формате данных в женераториндекс.</span><span class="sxs-lookup"><span data-stu-id="23ffa-105">Converts a Hamiltonian term in `HTerm` data format to a GeneratorIndex.</span></span>

```qsharp
function HTermToGenIdx (term : Microsoft.Quantum.Chemistry.HTerm, termType : Int[]) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="23ffa-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="23ffa-106">Input</span></span>

### <a name="term--hterm"></a><span data-ttu-id="23ffa-107">термин: [хтерм](xref:Microsoft.Quantum.Chemistry.HTerm)</span><span class="sxs-lookup"><span data-stu-id="23ffa-107">term : [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)</span></span>

<span data-ttu-id="23ffa-108">Входные данные в `HTerm` формате.</span><span class="sxs-lookup"><span data-stu-id="23ffa-108">Input data in `HTerm` format.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="23ffa-109">Термтипе: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="23ffa-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="23ffa-110">Дополнительные сведения, добавленные в Женераториндекс.</span><span class="sxs-lookup"><span data-stu-id="23ffa-110">Additional information added to GeneratorIndex.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="23ffa-111">Выходные данные: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="23ffa-111">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="23ffa-112">Женераториндекс, представляющий Хамилтониан термин, представленный `term` вместе с дополнительными сведениями, добавленными `termType` .</span><span class="sxs-lookup"><span data-stu-id="23ffa-112">A GeneratorIndex representing a Hamiltonian term represented by `term`, together with additional information added by `termType`.</span></span>