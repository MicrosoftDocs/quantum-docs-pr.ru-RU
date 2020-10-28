---
uid: Microsoft.Quantum.Preparation.PrepareQubit
title: Операция Препарекубит
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareQubit
qsharp.summary: >-
  Prepares a qubit in the +1 (`Zero`) eigenstate of the given Pauli operator. If the identity operator is given, then the qubit is prepared in the maximally mixed state.

  If the qubit was initially in the $\ket{0}$ state, this operation prepares the qubit in the $+1$ eigenstate of a given Pauli operator, or, for `PauliI`, in the maximally mixed state instead (see <xref:microsoft.quantum.preparation.preparesinglequbitidentity>).

  If the qubit was in a state other than $\ket{0}$, this operation applies the following gates: $H$ for `PauliX`, $HS$ for `PauliY`, $I$ for `PauliZ` and <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI`.
ms.openlocfilehash: 5f42bf26a8f9638ea88c035a18846050c3776b45
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732649"
---
# <a name="preparequbit-operation"></a><span data-ttu-id="e01d3-102">Операция Препарекубит</span><span class="sxs-lookup"><span data-stu-id="e01d3-102">PrepareQubit operation</span></span>

<span data-ttu-id="e01d3-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="e01d3-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="e01d3-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e01d3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e01d3-105">Подготавливает кубит в еиженстате + 1 ( `Zero` ) для данного оператора Паули.</span><span class="sxs-lookup"><span data-stu-id="e01d3-105">Prepares a qubit in the +1 (`Zero`) eigenstate of the given Pauli operator.</span></span>
<span data-ttu-id="e01d3-106">Если указан оператор Identity, кубит подготавливается в максимально смешанном состоянии.</span><span class="sxs-lookup"><span data-stu-id="e01d3-106">If the identity operator is given, then the qubit is prepared in the maximally mixed state.</span></span>

<span data-ttu-id="e01d3-107">Если кубит изначально находится в состоянии $ \кет {0} $, эта операция подготавливает кубит в еиженстате $ + $1 для данного оператора Паули или, для `PauliI` , в максимально смешанном состоянии (см <xref:microsoft.quantum.preparation.preparesinglequbitidentity> .).</span><span class="sxs-lookup"><span data-stu-id="e01d3-107">If the qubit was initially in the $\ket{0}$ state, this operation prepares the qubit in the $+1$ eigenstate of a given Pauli operator, or, for `PauliI`, in the maximally mixed state instead (see <xref:microsoft.quantum.preparation.preparesinglequbitidentity>).</span></span>

<span data-ttu-id="e01d3-108">Если кубит находится в состоянии, отличном от $ \кет {0} $, эта операция применяет следующие шлюзы: $H $ for `PauliX` , $HS $ для `PauliY` , $I $ for `PauliZ` и <xref:microsoft.quantum.preparation.preparesinglequbitidentity> для `PauliI` .</span><span class="sxs-lookup"><span data-stu-id="e01d3-108">If the qubit was in a state other than $\ket{0}$, this operation applies the following gates: $H$ for `PauliX`, $HS$ for `PauliY`, $I$ for `PauliZ` and <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI`.</span></span>

```qsharp
operation PrepareQubit (basis : Pauli, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="e01d3-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e01d3-109">Input</span></span>

### <a name="basis--pauli"></a><span data-ttu-id="e01d3-110">Базис: [Паули](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="e01d3-110">basis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="e01d3-111">Оператор Паули $P $.</span><span class="sxs-lookup"><span data-stu-id="e01d3-111">A Pauli operator $P$.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="e01d3-112">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e01d3-112">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e01d3-113">Кубит, который необходимо подготовить.</span><span class="sxs-lookup"><span data-stu-id="e01d3-113">A qubit to be prepared.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e01d3-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e01d3-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

