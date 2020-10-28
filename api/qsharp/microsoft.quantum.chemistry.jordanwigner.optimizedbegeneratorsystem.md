---
uid: Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEGeneratorSystem
title: Определяемый пользователем тип Оптимизедбеженераторсистем
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: OptimizedBEGeneratorSystem
qsharp.summary: Function that returns `OptimizedBETermIndex` data for term `n` given an integer `n`, together with the number of terms in the first `Int` and the sum of absolute-values of all term coefficients in the `Double`.
ms.openlocfilehash: 06d13a8a64a3c572821ec97f8776d6f1dbe4a4ce
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713941"
---
# <a name="optimizedbegeneratorsystem-user-defined-type"></a><span data-ttu-id="3b5cf-102">Определяемый пользователем тип Оптимизедбеженераторсистем</span><span class="sxs-lookup"><span data-stu-id="3b5cf-102">OptimizedBEGeneratorSystem user defined type</span></span>

<span data-ttu-id="3b5cf-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="3b5cf-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="3b5cf-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3b5cf-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3b5cf-105">Функция, возвращающая `OptimizedBETermIndex` данные для Терма `n` `n` , имеющего целое число, вместе с числом терминов в первой `Int` и сумме абсолютных значений всех термов в `Double` .</span><span class="sxs-lookup"><span data-stu-id="3b5cf-105">Function that returns `OptimizedBETermIndex` data for term `n` given an integer `n`, together with the number of terms in the first `Int` and the sum of absolute-values of all term coefficients in the `Double`.</span></span>

```qsharp

newtype OptimizedBEGeneratorSystem = (Int, Double, (Int -> Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex));
```

