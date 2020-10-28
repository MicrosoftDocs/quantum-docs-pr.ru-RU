---
uid: Microsoft.Quantum.Diagnostics.AssertPhase
title: Операция Ассертфасе
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertPhase
qsharp.summary: Asserts that the phase of an equal superposition state has the expected value.
ms.openlocfilehash: e042c03d2a72d9ce4816a8cdb56603e175b22807
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712948"
---
# <a name="assertphase-operation"></a><span data-ttu-id="20bcc-102">Операция Ассертфасе</span><span class="sxs-lookup"><span data-stu-id="20bcc-102">AssertPhase operation</span></span>

<span data-ttu-id="20bcc-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="20bcc-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="20bcc-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="20bcc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="20bcc-105">Утверждает, что фаза равного пресостояния перестановки имеет ожидаемое значение.</span><span class="sxs-lookup"><span data-stu-id="20bcc-105">Asserts that the phase of an equal superposition state has the expected value.</span></span>

```qsharp
operation AssertPhase (expected : Double, qubit : Qubit, tolerance : Double) : Unit
```


## <a name="description"></a><span data-ttu-id="20bcc-106">Описание</span><span class="sxs-lookup"><span data-stu-id="20bcc-106">Description</span></span>

<span data-ttu-id="20bcc-107">Эта операция подтверждает, что фаза $ \фи $ состояния такта, которая может быть выражена как $ \фрак{е ^ {i t}} {\скрт {2} } (e ^ {и\фи} \ Сисакет {0} + e ^ {-и\фи} \ Сисакет {1} ) $ для некоторых произвольных реальных $t $ имеет ожидаемое значение.</span><span class="sxs-lookup"><span data-stu-id="20bcc-107">This operation asserts that the phase $\phi$ of a quantum state that may be expressed as $\frac{e^{i t}}{\sqrt{2}}(e^{i\phi}\ket{0} + e^{-i\phi}\ket{1})$ for some arbitrary real $t$ has the expected value.</span></span>

## <a name="input"></a><span data-ttu-id="20bcc-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="20bcc-108">Input</span></span>

### <a name="expected--double"></a><span data-ttu-id="20bcc-109">ожидалось: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="20bcc-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="20bcc-110">Ожидаемое значение $ \фи \ин (-\пи, \пи] $.</span><span class="sxs-lookup"><span data-stu-id="20bcc-110">The expected value of $\phi \in (-\pi,\pi]$.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="20bcc-111">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="20bcc-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="20bcc-112">Кубит, в котором хранится ожидаемое состояние.</span><span class="sxs-lookup"><span data-stu-id="20bcc-112">The qubit that stores the expected state.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="20bcc-113">Допуск: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="20bcc-113">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="20bcc-114">Абсолютная погрешность разности между фактическим и ожидаемым.</span><span class="sxs-lookup"><span data-stu-id="20bcc-114">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="20bcc-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="20bcc-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>
