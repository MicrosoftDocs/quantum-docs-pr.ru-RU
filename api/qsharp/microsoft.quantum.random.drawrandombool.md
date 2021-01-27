---
uid: Microsoft.Quantum.Random.DrawRandomBool
title: Операция Драврандомбул
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomBool
qsharp.summary: Given a success probability, returns a single Bernoulli trial that is true with the given probability.
ms.openlocfilehash: 7c13f8305756421b8d07baf22ff87764efac0418
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853696"
---
# <a name="drawrandombool-operation"></a><span data-ttu-id="9ba22-102">Операция Драврандомбул</span><span class="sxs-lookup"><span data-stu-id="9ba22-102">DrawRandomBool operation</span></span>

<span data-ttu-id="9ba22-103">Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="9ba22-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="9ba22-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="9ba22-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="9ba22-105">Учитывая вероятность успеха, возвращает одну пробную версию Бернулли, которая имеет значение true с заданной вероятностью.</span><span class="sxs-lookup"><span data-stu-id="9ba22-105">Given a success probability, returns a single Bernoulli trial that is true with the given probability.</span></span>

```qsharp
operation DrawRandomBool (successProbability : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="9ba22-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9ba22-106">Input</span></span>

### <a name="successprobability--double"></a><span data-ttu-id="9ba22-107">Сукцесспробабилити: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="9ba22-107">successProbability : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="9ba22-108">Вероятность, с которой `true` должно возвращаться значение.</span><span class="sxs-lookup"><span data-stu-id="9ba22-108">The probability with which `true` should be returned.</span></span>



## <a name="output--bool"></a><span data-ttu-id="9ba22-109">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="9ba22-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="9ba22-110">`true` с вероятностью `successProbability` и `false` с вероятностью `1.0 - successProbability` .</span><span class="sxs-lookup"><span data-stu-id="9ba22-110">`true` with probability `successProbability` and `false` with probability `1.0 - successProbability`.</span></span>

## <a name="example"></a><span data-ttu-id="9ba22-111">Пример</span><span class="sxs-lookup"><span data-stu-id="9ba22-111">Example</span></span>

<span data-ttu-id="9ba22-112">Следующие примеры кода Q # переворачиваются с смещенной монет:</span><span class="sxs-lookup"><span data-stu-id="9ba22-112">The following Q# snippet samples flips from a biased coin:</span></span>

```qsharp
let flips = DrawMany(DrawRandomBool, 10, 0.6);
```