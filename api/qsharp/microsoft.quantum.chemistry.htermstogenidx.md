---
uid: Microsoft.Quantum.Chemistry.HTermsToGenIdx
title: Функция Хтермстоженидкс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenIdx
qsharp.summary: Converts an index to a Hamiltonian term in `HTerm[]` data format to a GeneratorIndex.
ms.openlocfilehash: 84dc132528f8fd1c45fb2f7345111a05626ee686
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839632"
---
# <a name="htermstogenidx-function"></a><span data-ttu-id="b871a-102">Функция Хтермстоженидкс</span><span class="sxs-lookup"><span data-stu-id="b871a-102">HTermsToGenIdx function</span></span>

<span data-ttu-id="b871a-103">Пространство имен: [Microsoft. тактов. Химия](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="b871a-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="b871a-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="b871a-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="b871a-105">Преобразует индекс в Хамилтониан термин в `HTerm[]` формате данных в женераториндекс.</span><span class="sxs-lookup"><span data-stu-id="b871a-105">Converts an index to a Hamiltonian term in `HTerm[]` data format to a GeneratorIndex.</span></span>

```qsharp
function HTermsToGenIdx (data : Microsoft.Quantum.Chemistry.HTerm[], termType : Int[], idx : Int) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="b871a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b871a-106">Input</span></span>

### <a name="data--hterm"></a><span data-ttu-id="b871a-107">данные: [хтерм](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span><span class="sxs-lookup"><span data-stu-id="b871a-107">data : [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span></span>

<span data-ttu-id="b871a-108">Входные данные в `HTerm[]` формате.</span><span class="sxs-lookup"><span data-stu-id="b871a-108">Input data in `HTerm[]` format.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="b871a-109">Термтипе: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="b871a-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="b871a-110">Дополнительные сведения, добавленные в Женераториндекс.</span><span class="sxs-lookup"><span data-stu-id="b871a-110">Additional information added to GeneratorIndex.</span></span>


### <a name="idx--int"></a><span data-ttu-id="b871a-111">IDX: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b871a-111">idx : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b871a-112">Индекс в термине Хамилтониан</span><span class="sxs-lookup"><span data-stu-id="b871a-112">Index to a term of the Hamiltonian</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="b871a-113">Выходные данные: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="b871a-113">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="b871a-114">Женераториндекс, представляющий Хамилтониан термин, представленный `data[idx]` вместе с дополнительными сведениями, добавленными `termType` .</span><span class="sxs-lookup"><span data-stu-id="b871a-114">A GeneratorIndex representing a Hamiltonian term represented by `data[idx]`, together with additional information added by `termType`.</span></span>