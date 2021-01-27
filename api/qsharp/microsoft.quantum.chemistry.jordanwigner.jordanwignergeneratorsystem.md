---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerGeneratorSystem
title: Функция Жорданвигнерженераторсистем
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerGeneratorSystem
qsharp.summary: Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.
ms.openlocfilehash: a75d46ef0b38fbcef99b7ab22454e1b5a9475b11
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98837772"
---
# <a name="jordanwignergeneratorsystem-function"></a><span data-ttu-id="02cb7-102">Функция Жорданвигнерженераторсистем</span><span class="sxs-lookup"><span data-stu-id="02cb7-102">JordanWignerGeneratorSystem function</span></span>

<span data-ttu-id="02cb7-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="02cb7-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="02cb7-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="02cb7-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="02cb7-105">Преобразует Хамилтониан, описанный в `JWOptimizedHTerms` `GeneratorSystem` выражении, в терминах `GeneratorIndex` соглашения, определенного в этом файле.</span><span class="sxs-lookup"><span data-stu-id="02cb7-105">Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.</span></span>

```qsharp
function JordanWignerGeneratorSystem (data : Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="02cb7-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="02cb7-106">Input</span></span>

### <a name="data--jwoptimizedhterms"></a><span data-ttu-id="02cb7-107">данные: [жвоптимизедхтермс](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span><span class="sxs-lookup"><span data-stu-id="02cb7-107">data : [JWOptimizedHTerms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span></span>

<span data-ttu-id="02cb7-108">Описание Хамилтониан в `JWOptimizedHTerms` формате.</span><span class="sxs-lookup"><span data-stu-id="02cb7-108">Description of Hamiltonian in `JWOptimizedHTerms` format.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="02cb7-109">Выходные данные: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="02cb7-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="02cb7-110">Представление Хамилтониан как `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="02cb7-110">Representation of Hamiltonian as `GeneratorSystem`.</span></span>