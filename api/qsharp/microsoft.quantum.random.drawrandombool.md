---
uid: Microsoft.Quantum.Random.DrawRandomBool
title: Операция Драврандомбул
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomBool
qsharp.summary: Given a success probability, returns a single Bernoulli trial that is true with the given probability.
ms.openlocfilehash: 05cf8ad939691aac90625c5d056ea79aa062f553
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730953"
---
# <a name="drawrandombool-operation"></a><span data-ttu-id="faf2d-102">Операция Драврандомбул</span><span class="sxs-lookup"><span data-stu-id="faf2d-102">DrawRandomBool operation</span></span>

<span data-ttu-id="faf2d-103">Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="faf2d-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="faf2d-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="faf2d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="faf2d-105">Учитывая вероятность успеха, возвращает одну пробную версию Бернулли, которая имеет значение true с заданной вероятностью.</span><span class="sxs-lookup"><span data-stu-id="faf2d-105">Given a success probability, returns a single Bernoulli trial that is true with the given probability.</span></span>

```qsharp
operation DrawRandomBool (successProbability : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="faf2d-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="faf2d-106">Input</span></span>

### <a name="successprobability--double"></a><span data-ttu-id="faf2d-107">Сукцесспробабилити: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="faf2d-107">successProbability : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="faf2d-108">Вероятность, с которой `true` должно возвращаться значение.</span><span class="sxs-lookup"><span data-stu-id="faf2d-108">The probability with which `true` should be returned.</span></span>



## <a name="output--bool"></a><span data-ttu-id="faf2d-109">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="faf2d-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="faf2d-110">`true` с вероятностью `successProbability` и `false` с вероятностью `1.0 - successProbability` .</span><span class="sxs-lookup"><span data-stu-id="faf2d-110">`true` with probability `successProbability` and `false` with probability `1.0 - successProbability`.</span></span>