---
uid: Microsoft.Quantum.Diagnostics._prepareEntangledState
title: _prepareEntangledState операция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _prepareEntangledState
qsharp.summary: >-
  Given two registers, prepares the maximally entangled state between each pair of qubits on the respective registers. All qubits must start in the |0⟩ state.

  The result is that corresponding pairs of qubits from each register are in the $\bra{\beta_{00}}\ket{\beta_{00}}$.
ms.openlocfilehash: 384dad5905cec50b500028e1bc352a742122b299
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713130"
---
# <a name="_prepareentangledstate-operation"></a><span data-ttu-id="a2756-102">_prepareEntangledState операция</span><span class="sxs-lookup"><span data-stu-id="a2756-102">_prepareEntangledState operation</span></span>

<span data-ttu-id="a2756-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="a2756-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="a2756-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a2756-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a2756-105">При наличии двух регистров подготавливает запутанными состояние между каждой парой Кубитс в соответствующих регистрах.</span><span class="sxs-lookup"><span data-stu-id="a2756-105">Given two registers, prepares the maximally entangled state between each pair of qubits on the respective registers.</span></span>
<span data-ttu-id="a2756-106">Все Кубитс должны начинаться в состоянии ⟩ | 0.</span><span class="sxs-lookup"><span data-stu-id="a2756-106">All qubits must start in the |0⟩ state.</span></span>

<span data-ttu-id="a2756-107">Результат заключается в том, что соответствующие пары Кубитс из каждой ККМ находятся в \кет{\ beta_ \бра{\ {00} {00} } $ beta_} $.</span><span class="sxs-lookup"><span data-stu-id="a2756-107">The result is that corresponding pairs of qubits from each register are in the $\bra{\beta_{00}}\ket{\beta_{00}}$.</span></span>

```qsharp
operation _prepareEntangledState (left : Qubit[], right : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="a2756-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a2756-108">Input</span></span>

### <a name="left--qubit"></a><span data-ttu-id="a2756-109">Left: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a2756-109">left : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a2756-110">Массив кубит в состоянии $ \ket{0\cdots 0} $</span><span class="sxs-lookup"><span data-stu-id="a2756-110">A qubit array in the $\ket{0\cdots 0}$ state</span></span>


### <a name="right--qubit"></a><span data-ttu-id="a2756-111">Right: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a2756-111">right : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a2756-112">Массив кубит в состоянии $ \ket{0\cdots 0} $</span><span class="sxs-lookup"><span data-stu-id="a2756-112">A qubit array in the $\ket{0\cdots 0}$ state</span></span>



## <a name="output--unit"></a><span data-ttu-id="a2756-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a2756-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

