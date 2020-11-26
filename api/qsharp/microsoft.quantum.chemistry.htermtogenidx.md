---
uid: Microsoft.Quantum.Chemistry.HTermToGenIdx
title: Функция Хтермтоженидкс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermToGenIdx
qsharp.summary: Converts a Hamiltonian term in `HTerm` data format to a GeneratorIndex.
ms.openlocfilehash: 59391a882fdbc55172ee93a7428c1735bbb29500
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216036"
---
# <a name="htermtogenidx-function"></a><span data-ttu-id="7a490-102">Функция Хтермтоженидкс</span><span class="sxs-lookup"><span data-stu-id="7a490-102">HTermToGenIdx function</span></span>

<span data-ttu-id="7a490-103">Пространство имен: [Microsoft. тактов. Химия](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="7a490-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="7a490-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="7a490-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="7a490-105">Преобразует термин Хамилтониан в `HTerm` формате данных в женераториндекс.</span><span class="sxs-lookup"><span data-stu-id="7a490-105">Converts a Hamiltonian term in `HTerm` data format to a GeneratorIndex.</span></span>

```qsharp
function HTermToGenIdx (term : Microsoft.Quantum.Chemistry.HTerm, termType : Int[]) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="7a490-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7a490-106">Input</span></span>

### <a name="term--hterm"></a><span data-ttu-id="7a490-107">термин: [хтерм](xref:Microsoft.Quantum.Chemistry.HTerm)</span><span class="sxs-lookup"><span data-stu-id="7a490-107">term : [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)</span></span>

<span data-ttu-id="7a490-108">Входные данные в `HTerm` формате.</span><span class="sxs-lookup"><span data-stu-id="7a490-108">Input data in `HTerm` format.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="7a490-109">Термтипе: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="7a490-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="7a490-110">Дополнительные сведения, добавленные в Женераториндекс.</span><span class="sxs-lookup"><span data-stu-id="7a490-110">Additional information added to GeneratorIndex.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="7a490-111">Выходные данные: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="7a490-111">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="7a490-112">Женераториндекс, представляющий Хамилтониан термин, представленный `term` вместе с дополнительными сведениями, добавленными `termType` .</span><span class="sxs-lookup"><span data-stu-id="7a490-112">A GeneratorIndex representing a Hamiltonian term represented by `term`, together with additional information added by `termType`.</span></span>