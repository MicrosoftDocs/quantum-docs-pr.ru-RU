---
uid: Microsoft.Quantum.Preparation.PrepareQubit
title: Операция Препарекубит
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareQubit
qsharp.summary: >-
  > [!WARNING]

  > PrepareQubit has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PreparePauliEigenstate> instead.


  Prepares a qubit in the +1 (`Zero`) eigenstate of the given Pauli operator. If the identity operator is given, then the qubit is prepared in the maximally mixed state.

  If the qubit was initially in the $\ket{0}$ state, this operation prepares the qubit in the $+1$ eigenstate of a given Pauli operator, or, for `PauliI`, in the maximally mixed state instead (see <xref:microsoft.quantum.preparation.preparesinglequbitidentity>).

  If the qubit was in a state other than $\ket{0}$, this operation applies the following gates: $H$ for `PauliX`, $HS$ for `PauliY`, $I$ for `PauliZ` and <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI`.
ms.openlocfilehash: 84674d70d6a038ceaf1c637b22afa1b724d90795
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193528"
---
# <a name="preparequbit-operation"></a><span data-ttu-id="b73a7-102">Операция Препарекубит</span><span class="sxs-lookup"><span data-stu-id="b73a7-102">PrepareQubit operation</span></span>

<span data-ttu-id="b73a7-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="b73a7-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="b73a7-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b73a7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="b73a7-105">Препарекубит является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="b73a7-105">PrepareQubit has been deprecated.</span></span> <span data-ttu-id="b73a7-106">Взамен рекомендуется использовать <xref:Microsoft.Quantum.Preparation.PreparePauliEigenstate>.</span><span class="sxs-lookup"><span data-stu-id="b73a7-106">Please use <xref:Microsoft.Quantum.Preparation.PreparePauliEigenstate> instead.</span></span>

<span data-ttu-id="b73a7-107">Подготавливает кубит в еиженстате + 1 ( `Zero` ) для данного оператора Паули.</span><span class="sxs-lookup"><span data-stu-id="b73a7-107">Prepares a qubit in the +1 (`Zero`) eigenstate of the given Pauli operator.</span></span>
<span data-ttu-id="b73a7-108">Если указан оператор Identity, кубит подготавливается в максимально смешанном состоянии.</span><span class="sxs-lookup"><span data-stu-id="b73a7-108">If the identity operator is given, then the qubit is prepared in the maximally mixed state.</span></span>

<span data-ttu-id="b73a7-109">Если кубит изначально находится в состоянии $ \кет {0} $, эта операция подготавливает кубит в еиженстате $ + $1 для данного оператора Паули или, для `PauliI` , в максимально смешанном состоянии (см <xref:microsoft.quantum.preparation.preparesinglequbitidentity> .).</span><span class="sxs-lookup"><span data-stu-id="b73a7-109">If the qubit was initially in the $\ket{0}$ state, this operation prepares the qubit in the $+1$ eigenstate of a given Pauli operator, or, for `PauliI`, in the maximally mixed state instead (see <xref:microsoft.quantum.preparation.preparesinglequbitidentity>).</span></span>

<span data-ttu-id="b73a7-110">Если кубит находится в состоянии, отличном от $ \кет {0} $, эта операция применяет следующие шлюзы: $H $ for `PauliX` , $HS $ для `PauliY` , $I $ for `PauliZ` и <xref:microsoft.quantum.preparation.preparesinglequbitidentity> для `PauliI` .</span><span class="sxs-lookup"><span data-stu-id="b73a7-110">If the qubit was in a state other than $\ket{0}$, this operation applies the following gates: $H$ for `PauliX`, $HS$ for `PauliY`, $I$ for `PauliZ` and <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI`.</span></span>

```qsharp
operation PrepareQubit (basis : Pauli, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="b73a7-111">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b73a7-111">Input</span></span>

### <a name="basis--pauli"></a><span data-ttu-id="b73a7-112">Базис: [Паули](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="b73a7-112">basis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="b73a7-113">Оператор Паули $P $.</span><span class="sxs-lookup"><span data-stu-id="b73a7-113">A Pauli operator $P$.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="b73a7-114">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="b73a7-114">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="b73a7-115">Кубит, который необходимо подготовить.</span><span class="sxs-lookup"><span data-stu-id="b73a7-115">A qubit to be prepared.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b73a7-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b73a7-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

