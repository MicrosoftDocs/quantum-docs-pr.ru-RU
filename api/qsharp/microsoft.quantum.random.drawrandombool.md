---
uid: Microsoft.Quantum.Random.DrawRandomBool
title: Операция Драврандомбул
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomBool
qsharp.summary: Given a success probability, returns a single Bernoulli trial that is true with the given probability.
ms.openlocfilehash: dbe0836af5aa19f1bdce3cfe93be6833358c22be
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192967"
---
# <a name="drawrandombool-operation"></a><span data-ttu-id="362c0-102">Операция Драврандомбул</span><span class="sxs-lookup"><span data-stu-id="362c0-102">DrawRandomBool operation</span></span>

<span data-ttu-id="362c0-103">Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="362c0-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="362c0-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="362c0-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="362c0-105">Учитывая вероятность успеха, возвращает одну пробную версию Бернулли, которая имеет значение true с заданной вероятностью.</span><span class="sxs-lookup"><span data-stu-id="362c0-105">Given a success probability, returns a single Bernoulli trial that is true with the given probability.</span></span>

```qsharp
operation DrawRandomBool (successProbability : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="362c0-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="362c0-106">Input</span></span>

### <a name="successprobability--double"></a><span data-ttu-id="362c0-107">Сукцесспробабилити: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="362c0-107">successProbability : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="362c0-108">Вероятность, с которой `true` должно возвращаться значение.</span><span class="sxs-lookup"><span data-stu-id="362c0-108">The probability with which `true` should be returned.</span></span>



## <a name="output--bool"></a><span data-ttu-id="362c0-109">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="362c0-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="362c0-110">`true` с вероятностью `successProbability` и `false` с вероятностью `1.0 - successProbability` .</span><span class="sxs-lookup"><span data-stu-id="362c0-110">`true` with probability `successProbability` and `false` with probability `1.0 - successProbability`.</span></span>