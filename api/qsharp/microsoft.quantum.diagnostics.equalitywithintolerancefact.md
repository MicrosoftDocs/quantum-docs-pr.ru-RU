---
uid: Microsoft.Quantum.Diagnostics.EqualityWithinToleranceFact
title: Функция Екуалитивисинтолеранцефакт
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityWithinToleranceFact
qsharp.summary: Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.
ms.openlocfilehash: de15a32d5b38c5ab8c681d2c052669a48cf676cc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712751"
---
# <a name="equalitywithintolerancefact-function"></a><span data-ttu-id="350d0-102">Функция Екуалитивисинтолеранцефакт</span><span class="sxs-lookup"><span data-stu-id="350d0-102">EqualityWithinToleranceFact function</span></span>

<span data-ttu-id="350d0-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="350d0-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="350d0-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="350d0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="350d0-105">Представляет утверждение, что классическое значение с плавающей запятой имеет ожидаемое значение вплоть до заданного абсолютного допуска.</span><span class="sxs-lookup"><span data-stu-id="350d0-105">Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.</span></span>

```qsharp
function EqualityWithinToleranceFact (actual : Double, expected : Double, tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="350d0-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="350d0-106">Input</span></span>

### <a name="actual--double"></a><span data-ttu-id="350d0-107">фактический: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="350d0-107">actual : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="350d0-108">Число для проверки.</span><span class="sxs-lookup"><span data-stu-id="350d0-108">The number to be checked.</span></span>


### <a name="expected--double"></a><span data-ttu-id="350d0-109">ожидалось: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="350d0-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="350d0-110">Ожидаемое значение.</span><span class="sxs-lookup"><span data-stu-id="350d0-110">The expected value.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="350d0-111">Допуск: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="350d0-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="350d0-112">Абсолютная погрешность разности между фактическим и ожидаемым.</span><span class="sxs-lookup"><span data-stu-id="350d0-112">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="350d0-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="350d0-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

