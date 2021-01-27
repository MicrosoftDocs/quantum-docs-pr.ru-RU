---
uid: Microsoft.Quantum.Preparation.PreparePauliEigenstate
title: Операция Препарепаулиеиженстате
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PreparePauliEigenstate
qsharp.summary: Prepares a qubit in the positive eigenstate of a given Pauli operator. If the identity operator is given, then the qubit is prepared in the maximally mixed state.
ms.openlocfilehash: 473bb2fa4429a14f69bcae4573354aad87dc37df
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854352"
---
# <a name="preparepaulieigenstate-operation"></a><span data-ttu-id="0dadb-102">Операция Препарепаулиеиженстате</span><span class="sxs-lookup"><span data-stu-id="0dadb-102">PreparePauliEigenstate operation</span></span>

<span data-ttu-id="0dadb-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="0dadb-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="0dadb-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0dadb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0dadb-105">Подготавливает кубит в положительном еиженстатее данного оператора Паули.</span><span class="sxs-lookup"><span data-stu-id="0dadb-105">Prepares a qubit in the positive eigenstate of a given Pauli operator.</span></span>
<span data-ttu-id="0dadb-106">Если указан оператор Identity, кубит подготавливается в максимально смешанном состоянии.</span><span class="sxs-lookup"><span data-stu-id="0dadb-106">If the identity operator is given, then the qubit is prepared in the maximally mixed state.</span></span>

```qsharp
operation PreparePauliEigenstate (basis : Pauli, qubit : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="0dadb-107">Описание</span><span class="sxs-lookup"><span data-stu-id="0dadb-107">Description</span></span>

<span data-ttu-id="0dadb-108">Если кубит изначально находится в состоянии $ \кет {0} $, эта операция подготавливает кубит в еиженстате $ + $1 для данного оператора Паули или, для `PauliI` , в максимально смешанном состоянии (см <xref:microsoft.quantum.preparation.preparesinglequbitidentity> .).</span><span class="sxs-lookup"><span data-stu-id="0dadb-108">If the qubit was initially in the $\ket{0}$ state, this operation prepares the qubit in the $+1$ eigenstate of a given Pauli operator, or, for `PauliI`, in the maximally mixed state instead (see <xref:microsoft.quantum.preparation.preparesinglequbitidentity>).</span></span>

<span data-ttu-id="0dadb-109">Если кубит находится в состоянии, отличном от $ \кет {0} $, эта операция применяет следующие шлюзы: $H $ for `PauliX` , $HS $ для `PauliY` , $I $ for `PauliZ` и <xref:microsoft.quantum.preparation.preparesinglequbitidentity> для `PauliI` .</span><span class="sxs-lookup"><span data-stu-id="0dadb-109">If the qubit was in a state other than $\ket{0}$, this operation applies the following gates: $H$ for `PauliX`, $HS$ for `PauliY`, $I$ for `PauliZ` and <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI`.</span></span>

## <a name="input"></a><span data-ttu-id="0dadb-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0dadb-110">Input</span></span>

### <a name="basis--pauli"></a><span data-ttu-id="0dadb-111">Базис: [Паули](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="0dadb-111">basis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="0dadb-112">Оператор Паули $P $.</span><span class="sxs-lookup"><span data-stu-id="0dadb-112">A Pauli operator $P$.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="0dadb-113">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="0dadb-113">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="0dadb-114">Кубит, который необходимо подготовить.</span><span class="sxs-lookup"><span data-stu-id="0dadb-114">A qubit to be prepared.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0dadb-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0dadb-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="0dadb-116">Пример</span><span class="sxs-lookup"><span data-stu-id="0dadb-116">Example</span></span>

<span data-ttu-id="0dadb-117">Чтобы подготовить кубит в состоянии $ \кет{+} $, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="0dadb-117">To prepare a qubit in the $\ket{+}$ state:</span></span>

```qsharp
using (q = Qubit()) {
    PreparePauliEigenstate(PauliX, qubit);
    // ...
}
```