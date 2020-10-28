---
uid: Microsoft.Quantum.Chemistry.HTermsToGenSys
title: Функция Хтермстоженсис
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenSys
qsharp.summary: Converts a Hamiltonian in `HTerm[]` data format to a GeneratorSystem.
ms.openlocfilehash: b78ff393fa1e51c38028ef56bb3c61b8f1d5e478
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714838"
---
# <a name="htermstogensys-function"></a><span data-ttu-id="0f417-102">Функция Хтермстоженсис</span><span class="sxs-lookup"><span data-stu-id="0f417-102">HTermsToGenSys function</span></span>

<span data-ttu-id="0f417-103">Пространство имен: [Microsoft. тактов. Химия](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="0f417-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="0f417-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0f417-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0f417-105">Преобразует Хамилтониан в `HTerm[]` формате данных в женераторсистем.</span><span class="sxs-lookup"><span data-stu-id="0f417-105">Converts a Hamiltonian in `HTerm[]` data format to a GeneratorSystem.</span></span>

```qsharp
function HTermsToGenSys (data : Microsoft.Quantum.Chemistry.HTerm[], termType : Int[]) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="0f417-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0f417-106">Input</span></span>

### <a name="data--hterm"></a><span data-ttu-id="0f417-107">данные: [хтерм](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span><span class="sxs-lookup"><span data-stu-id="0f417-107">data : [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span></span>

<span data-ttu-id="0f417-108">Входные данные в `HTerm[]` формате.</span><span class="sxs-lookup"><span data-stu-id="0f417-108">Input data in `HTerm[]` format.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="0f417-109">Термтипе: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="0f417-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="0f417-110">Дополнительные сведения, добавленные в Женераториндекс.</span><span class="sxs-lookup"><span data-stu-id="0f417-110">Additional information added to GeneratorIndex.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="0f417-111">Выходные данные: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="0f417-111">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="0f417-112">Объект Женераторсистем, представляющий Хамилтониан, представленный входными данными `data` .</span><span class="sxs-lookup"><span data-stu-id="0f417-112">A GeneratorSystem representing a Hamiltonian represented by the input `data`.</span></span>