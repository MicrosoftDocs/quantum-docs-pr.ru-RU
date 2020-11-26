---
uid: Microsoft.Quantum.Diagnostics.NearEqualityFactD
title: Функция Неарекуалитифактд
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: NearEqualityFactD
qsharp.summary: Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.
ms.openlocfilehash: 5acfe5043342fd88276910a9fd0347f7d2f6960f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201518"
---
# <a name="nearequalityfactd-function"></a><span data-ttu-id="af56b-102">Функция Неарекуалитифактд</span><span class="sxs-lookup"><span data-stu-id="af56b-102">NearEqualityFactD function</span></span>

<span data-ttu-id="af56b-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="af56b-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="af56b-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="af56b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="af56b-105">Утверждает, что классическое значение с плавающей запятой имеет ожидаемое значение вплоть до маленькой допустимой допускки 1E-10.</span><span class="sxs-lookup"><span data-stu-id="af56b-105">Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.</span></span>

```qsharp
function NearEqualityFactD (actual : Double, expected : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="af56b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="af56b-106">Input</span></span>

### <a name="actual--double"></a><span data-ttu-id="af56b-107">фактический: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="af56b-107">actual : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="af56b-108">Число для проверки.</span><span class="sxs-lookup"><span data-stu-id="af56b-108">The number to be checked.</span></span>


### <a name="expected--double"></a><span data-ttu-id="af56b-109">ожидалось: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="af56b-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="af56b-110">Ожидаемое значение.</span><span class="sxs-lookup"><span data-stu-id="af56b-110">The expected value.</span></span>



## <a name="output--unit"></a><span data-ttu-id="af56b-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="af56b-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="af56b-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af56b-112">Remarks</span></span>

<span data-ttu-id="af56b-113">Это эквивалентно <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact> параметру с жестким отклонением $10 ^ {-10} $.</span><span class="sxs-lookup"><span data-stu-id="af56b-113">This is equivalent to <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact> with hardcoded tolerance of $10^{-10}$.</span></span>