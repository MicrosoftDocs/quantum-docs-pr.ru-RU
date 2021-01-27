---
uid: Microsoft.Quantum.Research.Chemistry.JWOptimizedGeneratorSystem
title: Функция Жвоптимизедженераторсистем
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JWOptimizedGeneratorSystem
qsharp.summary: Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.
ms.openlocfilehash: 13e3386a612b238c29a9e3368eed8628e8ed9b66
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847016"
---
# <a name="jwoptimizedgeneratorsystem-function"></a><span data-ttu-id="ad2fa-102">Функция Жвоптимизедженераторсистем</span><span class="sxs-lookup"><span data-stu-id="ad2fa-102">JWOptimizedGeneratorSystem function</span></span>

<span data-ttu-id="ad2fa-103">Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="ad2fa-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="ad2fa-104">Пакет: [Microsoft. тактов. Research. Химия](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="ad2fa-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="ad2fa-105">Преобразует Хамилтониан, описанный в `JWOptimizedHTerms` `GeneratorSystem` выражении, в терминах `GeneratorIndex` соглашения, определенного в этом файле.</span><span class="sxs-lookup"><span data-stu-id="ad2fa-105">Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.</span></span>

```qsharp
function JWOptimizedGeneratorSystem (data : Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="ad2fa-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ad2fa-106">Input</span></span>

### <a name="data--jwoptimizedhterms"></a><span data-ttu-id="ad2fa-107">данные: [жвоптимизедхтермс](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span><span class="sxs-lookup"><span data-stu-id="ad2fa-107">data : [JWOptimizedHTerms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span></span>

<span data-ttu-id="ad2fa-108">Описание Хамилтониан в `JWOptimizedHTerms` формате.</span><span class="sxs-lookup"><span data-stu-id="ad2fa-108">Description of Hamiltonian in `JWOptimizedHTerms` format.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="ad2fa-109">Выходные данные: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="ad2fa-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="ad2fa-110">Представление Хамилтониан как `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="ad2fa-110">Representation of Hamiltonian as `GeneratorSystem`.</span></span>