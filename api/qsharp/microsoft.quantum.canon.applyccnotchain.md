---
uid: Microsoft.Quantum.Canon.ApplyCCNOTChain
title: Операция Аппликкнотчаин
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCCNOTChain
qsharp.summary: Implements a cascade of CCNOT gates controlled on corresponding bits of two qubit registers, acting on the next qubit of one of the registers. Starting from the qubits at position 0 in both registers as controls, CCNOT is applied to the qubit at position 1 of the target register, then controlled by the qubits at position 1 acting on the qubit at position 2 in the target register, etc., ending with an action on the target qubit in position `Length(nQubits)-1`.
ms.openlocfilehash: e4f38e9bb54839076b817f6e61e96ca6a550576b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729696"
---
# <a name="applyccnotchain-operation"></a><span data-ttu-id="3715d-102">Операция Аппликкнотчаин</span><span class="sxs-lookup"><span data-stu-id="3715d-102">ApplyCCNOTChain operation</span></span>

<span data-ttu-id="3715d-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3715d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3715d-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3715d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3715d-105">Реализует каскадный шлюз ККНОТ, управляемый по соответствующим битам двух регистров кубит, который действует на следующий кубит одного из регистров.</span><span class="sxs-lookup"><span data-stu-id="3715d-105">Implements a cascade of CCNOT gates controlled on corresponding bits of two qubit registers, acting on the next qubit of one of the registers.</span></span>
<span data-ttu-id="3715d-106">Начиная с Кубитс в позиции 0 в обоих регистрах как элементы управления, ККНОТ применяется к кубит в позиции 1 целевого регистра, затем управляется Кубитс в позиции 1, действующей на кубит в позиции 2 в целевой регистрации, и т. д., заканчивая действием на целевом кубит в позиции `Length(nQubits)-1` .</span><span class="sxs-lookup"><span data-stu-id="3715d-106">Starting from the qubits at position 0 in both registers as controls, CCNOT is applied to the qubit at position 1 of the target register, then controlled by the qubits at position 1 acting on the qubit at position 2 in the target register, etc., ending with an action on the target qubit in position `Length(nQubits)-1`.</span></span>

```qsharp
operation ApplyCCNOTChain (register : Qubit[], targets : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="3715d-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3715d-107">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="3715d-108">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="3715d-108">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="3715d-109">Кубит регистр, используемый только для элементов управления.</span><span class="sxs-lookup"><span data-stu-id="3715d-109">Qubit register, only used for controls.</span></span>


### <a name="targets--qubit"></a><span data-ttu-id="3715d-110">целевые объекты: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="3715d-110">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="3715d-111">Регистр кубит, используемый для элементов управления и в качестве целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="3715d-111">Qubit register, used for controls and as target.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3715d-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3715d-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="3715d-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="3715d-113">Remarks</span></span>

<span data-ttu-id="3715d-114">Целевой регистр кубит должен иметь один кубит больше, чем другой регистр.</span><span class="sxs-lookup"><span data-stu-id="3715d-114">The target qubit register must have one qubit more than the other register.</span></span>