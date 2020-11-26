---
uid: Microsoft.Quantum.Math._ContinuedFractionConvergentI
title: Функция _ContinuedFractionConvergentI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: _ContinuedFractionConvergentI
qsharp.summary: Internal recursive call to calculate the GCD with a bound
ms.openlocfilehash: 337ef5e90f98b3529ccda628abe203d391877646
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211514"
---
# <a name="_continuedfractionconvergenti-function"></a><span data-ttu-id="40a24-102">Функция _ContinuedFractionConvergentI</span><span class="sxs-lookup"><span data-stu-id="40a24-102">_ContinuedFractionConvergentI function</span></span>

<span data-ttu-id="40a24-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="40a24-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="40a24-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="40a24-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="40a24-105">Внутренний рекурсивный вызов для вычисления GCD с границей</span><span class="sxs-lookup"><span data-stu-id="40a24-105">Internal recursive call to calculate the GCD with a bound</span></span>

```qsharp
function _ContinuedFractionConvergentI (signA : Int, signB : Int, r : (Int, Int), s : (Int, Int), t : (Int, Int), denominatorBound : Int) : Microsoft.Quantum.Math.Fraction
```


## <a name="input"></a><span data-ttu-id="40a24-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="40a24-106">Input</span></span>

### <a name="signa--int"></a><span data-ttu-id="40a24-107">Подпись: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="40a24-107">signA : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="signb--int"></a><span data-ttu-id="40a24-108">Сигнб: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="40a24-108">signB : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="r--intint"></a><span data-ttu-id="40a24-109">r: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="40a24-109">r : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>




### <a name="s--intint"></a><span data-ttu-id="40a24-110">s: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="40a24-110">s : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>




### <a name="t--intint"></a><span data-ttu-id="40a24-111">t: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="40a24-111">t : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>




### <a name="denominatorbound--int"></a><span data-ttu-id="40a24-112">Деноминаторбаунд: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="40a24-112">denominatorBound : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--fraction"></a><span data-ttu-id="40a24-113">Выходные данные: [дробь](xref:Microsoft.Quantum.Math.Fraction)</span><span class="sxs-lookup"><span data-stu-id="40a24-113">Output : [Fraction](xref:Microsoft.Quantum.Math.Fraction)</span></span>

