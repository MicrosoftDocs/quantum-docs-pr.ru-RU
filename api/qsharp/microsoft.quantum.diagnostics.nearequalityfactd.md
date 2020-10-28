---
uid: Microsoft.Quantum.Diagnostics.NearEqualityFactD
title: Функция Неарекуалитифактд
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: NearEqualityFactD
qsharp.summary: Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.
ms.openlocfilehash: 5b55f515b27667071218a3f604ef703a6a15206d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712653"
---
# <a name="nearequalityfactd-function"></a><span data-ttu-id="721e3-102">Функция Неарекуалитифактд</span><span class="sxs-lookup"><span data-stu-id="721e3-102">NearEqualityFactD function</span></span>

<span data-ttu-id="721e3-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="721e3-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="721e3-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="721e3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="721e3-105">Утверждает, что классическое значение с плавающей запятой имеет ожидаемое значение вплоть до маленькой допустимой допускки 1E-10.</span><span class="sxs-lookup"><span data-stu-id="721e3-105">Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.</span></span>

```qsharp
function NearEqualityFactD (actual : Double, expected : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="721e3-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="721e3-106">Input</span></span>

### <a name="actual--double"></a><span data-ttu-id="721e3-107">фактический: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="721e3-107">actual : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="721e3-108">Число для проверки.</span><span class="sxs-lookup"><span data-stu-id="721e3-108">The number to be checked.</span></span>


### <a name="expected--double"></a><span data-ttu-id="721e3-109">ожидалось: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="721e3-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="721e3-110">Ожидаемое значение.</span><span class="sxs-lookup"><span data-stu-id="721e3-110">The expected value.</span></span>



## <a name="output--unit"></a><span data-ttu-id="721e3-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="721e3-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="721e3-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="721e3-112">Remarks</span></span>

<span data-ttu-id="721e3-113">Это эквивалентно <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact> параметру с жестким отклонением $10 ^ {-10} $.</span><span class="sxs-lookup"><span data-stu-id="721e3-113">This is equivalent to <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact> with hardcoded tolerance of $10^{-10}$.</span></span>