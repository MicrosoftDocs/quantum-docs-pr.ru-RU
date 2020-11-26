---
uid: Microsoft.Quantum.Canon.AndLadder
title: Операция Андладдер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: AndLadder
qsharp.summary: Performs a controlled "AND ladder" on a register of target qubits.
ms.openlocfilehash: 2c6114ec8a5caabdeea8ab7e26a4877e1633671c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209729"
---
# <a name="andladder-operation"></a><span data-ttu-id="e0ff6-102">Операция Андладдер</span><span class="sxs-lookup"><span data-stu-id="e0ff6-102">AndLadder operation</span></span>

<span data-ttu-id="e0ff6-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e0ff6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e0ff6-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e0ff6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e0ff6-105">Выполняет управляемый "и" лестницу "для регистра целевых Кубитс.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-105">Performs a controlled "AND ladder" on a register of target qubits.</span></span>

```qsharp
operation AndLadder (ccnot : Microsoft.Quantum.Canon.CCNOTop, controls : Qubit[], targets : Qubit[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="e0ff6-106">Описание</span><span class="sxs-lookup"><span data-stu-id="e0ff6-106">Description</span></span>

<span data-ttu-id="e0ff6-107">Эта операция применяет преобразование, описываемое в следующем сопоставлении вычислительной области, $ $ \бегин{алигн} \кет{КС \_ 1, \дотс, x \_ n} \кет{и \_ 1, \дотс, y \_ {n-1}} \мапсто \кет{КС \_ 1, \дотс, x \_ n} \кет{y \_ 1 \оплус (x \_ 1 \ланд x \_ 2), \дотс, y \_ {n-1} \оплус (x \_ 1 \land x \_ 2 \land \cdots \land x \_ {n-1}}, \end{align} $ $ WHERE $ \ket{x \_ 1, \dots, x \_ n} $ относится к вычислительным состояниям `controls` и где $ \ket{y \_ 1, \dots, y \_ {n-1}} $ относится к вычислительным состояниям `targets` .</span><span class="sxs-lookup"><span data-stu-id="e0ff6-107">This operation applies a transformation described by the following mapping of the computational basis, $$ \begin{align} \ket{x\_1, \dots, x\_n} \ket{y\_1, \dots, y\_{n - 1}} \mapsto \ket{x\_1, \dots, x\_n} \ket{ y\_1 \oplus (x\_1 \land x\_2), \dots, y\_{n - 1} \oplus (x\_1 \land x\_2 \land \cdots \land x\_{n - 1} }, \end{align} $$ where $\ket{x\_1, \dots, x\_n}$ refers to the computational basis states of `controls`, and where $\ket{y\_1, \dots, y\_{n - 1}}$ refers to the computational basis states of `targets`.</span></span>

## <a name="input"></a><span data-ttu-id="e0ff6-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e0ff6-108">Input</span></span>

### <a name="ccnot--ccnotop"></a><span data-ttu-id="e0ff6-109">ккнот: [ккнотоп](xref:Microsoft.Quantum.Canon.CCNOTop)</span><span class="sxs-lookup"><span data-stu-id="e0ff6-109">ccnot : [CCNOTop](xref:Microsoft.Quantum.Canon.CCNOTop)</span></span>

<span data-ttu-id="e0ff6-110">Шлюз ККНОТ, используемый для создания.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-110">The CCNOT gate to use for the construction.</span></span>


### <a name="controls--qubit"></a><span data-ttu-id="e0ff6-111">элементы управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="e0ff6-111">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e0ff6-112">Регистр Кубитс, который будет использоваться в качестве элементов управления для и в лестнице.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-112">A register of qubits to be used as controls for the and ladder.</span></span>
<span data-ttu-id="e0ff6-113">Эта операция оставляет основные состояния вычисления `controls` инвариантного.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-113">This operation leaves computational basis states of `controls` invariant.</span></span>
<span data-ttu-id="e0ff6-114">Длина `controls` должна быть не меньше 2 и должна быть равна единице плюс длина `targets` .</span><span class="sxs-lookup"><span data-stu-id="e0ff6-114">The length of `controls` must be at least 2, and must be equal to one plus the length of `targets`.</span></span>


### <a name="targets--qubit"></a><span data-ttu-id="e0ff6-115">целевые объекты: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="e0ff6-115">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e0ff6-116">Длина `targets` должна быть не меньше 1 и равна длине `controls` минус единица.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-116">The length of `targets` must be at least 1 and equal to the length of `controls` minus one.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e0ff6-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e0ff6-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="e0ff6-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e0ff6-118">Remarks</span></span>

- <span data-ttu-id="e0ff6-119">Используется как часть <xref:microsoft.quantum.canon.applymulticontrolledc> и <xref:microsoft.quantum.canon.applymulticontrolledca> .</span><span class="sxs-lookup"><span data-stu-id="e0ff6-119">Used as a part of <xref:microsoft.quantum.canon.applymulticontrolledc> and <xref:microsoft.quantum.canon.applymulticontrolledca>.</span></span>
- <span data-ttu-id="e0ff6-120">Описание и схема схемы см. на рис. 4,10 раздела 4,3 в Nielsen & Чжуанский.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-120">For the explanation and circuit diagram see Figure 4.10, Section 4.3 in Nielsen & Chuang.</span></span>

## <a name="references"></a><span data-ttu-id="e0ff6-121">Ссылки</span><span class="sxs-lookup"><span data-stu-id="e0ff6-121">References</span></span>

- [<span data-ttu-id="e0ff6-122">*Майкл A. Nielsen, Исаак L. Чжуанский*, вычисление такта и сведения о такте</span><span class="sxs-lookup"><span data-stu-id="e0ff6-122"> *Michael A. Nielsen , Isaac L. Chuang*, Quantum Computation and Quantum Information </span></span>](http://doi.org/10.1017/CBO9780511976667)