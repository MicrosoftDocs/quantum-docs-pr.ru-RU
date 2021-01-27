---
uid: Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBlockEncodingGeneratorSystem
title: Функция Оптимизедблоккенкодингженераторсистем
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: OptimizedBlockEncodingGeneratorSystem
qsharp.summary: Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the Pauli `GeneratorIndex`.
ms.openlocfilehash: 4320f111fe7a367bce0f79b04b37639090ddb838
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98837120"
---
# <a name="optimizedblockencodinggeneratorsystem-function"></a><span data-ttu-id="7464e-102">Функция Оптимизедблоккенкодингженераторсистем</span><span class="sxs-lookup"><span data-stu-id="7464e-102">OptimizedBlockEncodingGeneratorSystem function</span></span>

<span data-ttu-id="7464e-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="7464e-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="7464e-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="7464e-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="7464e-105">Преобразует Хамилтониан, описанный в `JWOptimizedHTerms` `GeneratorSystem` выражении в виде Паули `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="7464e-105">Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the Pauli `GeneratorIndex`.</span></span>

```qsharp
function OptimizedBlockEncodingGeneratorSystem (data : Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms) : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEGeneratorSystem
```


## <a name="input"></a><span data-ttu-id="7464e-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7464e-106">Input</span></span>

### <a name="data--jwoptimizedhterms"></a><span data-ttu-id="7464e-107">данные: [жвоптимизедхтермс](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span><span class="sxs-lookup"><span data-stu-id="7464e-107">data : [JWOptimizedHTerms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span></span>

<span data-ttu-id="7464e-108">Описание Хамилтониан в `JWOptimizedHTerms` формате.</span><span class="sxs-lookup"><span data-stu-id="7464e-108">Description of Hamiltonian in `JWOptimizedHTerms` format.</span></span>



## <a name="output--optimizedbegeneratorsystem"></a><span data-ttu-id="7464e-109">Выходные данные: [оптимизедбеженераторсистем](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEGeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="7464e-109">Output : [OptimizedBEGeneratorSystem](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEGeneratorSystem)</span></span>

<span data-ttu-id="7464e-110">Представление Хамилтониан как `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="7464e-110">Representation of Hamiltonian as `GeneratorSystem`.</span></span>