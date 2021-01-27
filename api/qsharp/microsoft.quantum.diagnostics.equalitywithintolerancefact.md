---
uid: Microsoft.Quantum.Diagnostics.EqualityWithinToleranceFact
title: Функция Екуалитивисинтолеранцефакт
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityWithinToleranceFact
qsharp.summary: Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.
ms.openlocfilehash: ab7e43d951bf741926b15f27f94d176e88609d4a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98828755"
---
# <a name="equalitywithintolerancefact-function"></a><span data-ttu-id="fc9dc-102">Функция Екуалитивисинтолеранцефакт</span><span class="sxs-lookup"><span data-stu-id="fc9dc-102">EqualityWithinToleranceFact function</span></span>

<span data-ttu-id="fc9dc-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="fc9dc-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="fc9dc-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fc9dc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fc9dc-105">Представляет утверждение, что классическое значение с плавающей запятой имеет ожидаемое значение вплоть до заданного абсолютного допуска.</span><span class="sxs-lookup"><span data-stu-id="fc9dc-105">Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.</span></span>

```qsharp
function EqualityWithinToleranceFact (actual : Double, expected : Double, tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="fc9dc-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fc9dc-106">Input</span></span>

### <a name="actual--double"></a><span data-ttu-id="fc9dc-107">фактический: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fc9dc-107">actual : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fc9dc-108">Число для проверки.</span><span class="sxs-lookup"><span data-stu-id="fc9dc-108">The number to be checked.</span></span>


### <a name="expected--double"></a><span data-ttu-id="fc9dc-109">ожидалось: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fc9dc-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fc9dc-110">Ожидаемое значение.</span><span class="sxs-lookup"><span data-stu-id="fc9dc-110">The expected value.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="fc9dc-111">Допуск: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fc9dc-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fc9dc-112">Абсолютная погрешность разности между фактическим и ожидаемым.</span><span class="sxs-lookup"><span data-stu-id="fc9dc-112">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fc9dc-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fc9dc-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

