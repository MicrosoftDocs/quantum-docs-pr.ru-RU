---
uid: Microsoft.Quantum.Chemistry.HTermToGenIdx
title: Функция Хтермтоженидкс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermToGenIdx
qsharp.summary: Converts a Hamiltonian term in `HTerm` data format to a GeneratorIndex.
ms.openlocfilehash: dd72355adb32f9a0d109ee36b24be2d445f3fa66
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714837"
---
# <a name="htermtogenidx-function"></a><span data-ttu-id="f3e2f-102">Функция Хтермтоженидкс</span><span class="sxs-lookup"><span data-stu-id="f3e2f-102">HTermToGenIdx function</span></span>

<span data-ttu-id="f3e2f-103">Пространство имен: [Microsoft. тактов. Химия](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="f3e2f-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="f3e2f-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f3e2f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f3e2f-105">Преобразует термин Хамилтониан в `HTerm` формате данных в женераториндекс.</span><span class="sxs-lookup"><span data-stu-id="f3e2f-105">Converts a Hamiltonian term in `HTerm` data format to a GeneratorIndex.</span></span>

```qsharp
function HTermToGenIdx (term : Microsoft.Quantum.Chemistry.HTerm, termType : Int[]) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="f3e2f-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f3e2f-106">Input</span></span>

### <a name="term--hterm"></a><span data-ttu-id="f3e2f-107">термин: [хтерм](xref:Microsoft.Quantum.Chemistry.HTerm)</span><span class="sxs-lookup"><span data-stu-id="f3e2f-107">term : [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)</span></span>

<span data-ttu-id="f3e2f-108">Входные данные в `HTerm` формате.</span><span class="sxs-lookup"><span data-stu-id="f3e2f-108">Input data in `HTerm` format.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="f3e2f-109">Термтипе: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="f3e2f-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="f3e2f-110">Дополнительные сведения, добавленные в Женераториндекс.</span><span class="sxs-lookup"><span data-stu-id="f3e2f-110">Additional information added to GeneratorIndex.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="f3e2f-111">Выходные данные: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="f3e2f-111">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="f3e2f-112">Женераториндекс, представляющий Хамилтониан термин, представленный `term` вместе с дополнительными сведениями, добавленными `termType` .</span><span class="sxs-lookup"><span data-stu-id="f3e2f-112">A GeneratorIndex representing a Hamiltonian term represented by `term`, together with additional information added by `termType`.</span></span>