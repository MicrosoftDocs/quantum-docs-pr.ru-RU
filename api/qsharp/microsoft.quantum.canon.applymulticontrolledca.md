---
uid: Microsoft.Quantum.Canon.ApplyMultiControlledCA
title: Операция Апплимултиконтролледка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiControlledCA
qsharp.summary: Applies a multiply controlled version of a singly controlled operation. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: 5662efe0dc6f665206b8773596bf885ce631413c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717960"
---
# <a name="applymulticontrolledca-operation"></a><span data-ttu-id="f0acc-102">Операция Апплимултиконтролледка</span><span class="sxs-lookup"><span data-stu-id="f0acc-102">ApplyMultiControlledCA operation</span></span>

<span data-ttu-id="f0acc-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f0acc-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f0acc-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f0acc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f0acc-105">Применяет версию управляемой операции с одной операцией умножения.</span><span class="sxs-lookup"><span data-stu-id="f0acc-105">Applies a multiply controlled version of a singly controlled operation.</span></span>
<span data-ttu-id="f0acc-106">Модификатор `CA` указывает, что одна операция кубит является управляемой и аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="f0acc-106">The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyMultiControlledCA (singlyControlledOp : (Qubit[] => Unit is Adj), ccnot : Microsoft.Quantum.Canon.CCNOTop, controls : Qubit[], targets : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="f0acc-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f0acc-107">Input</span></span>

### <a name="singlycontrolledop--qubit--unit-adj"></a><span data-ttu-id="f0acc-108">Сингликонтролледоп: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="f0acc-108">singlyControlledOp : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="f0acc-109">Операция, управляемая для одного кубит.</span><span class="sxs-lookup"><span data-stu-id="f0acc-109">An operation controlled on a single qubit.</span></span>
<span data-ttu-id="f0acc-110">Первым кубит в аргументе операции считается элемент управления, а остальные считаются целевыми Кубитс.</span><span class="sxs-lookup"><span data-stu-id="f0acc-110">The first qubit in the argument of the operation assumed to be a control and the rest are assumed to be target qubits.</span></span>
<span data-ttu-id="f0acc-111">`ApplyMultiControlled` всегда вызывает `singlyControlledOp` аргумент длиной не менее 1.</span><span class="sxs-lookup"><span data-stu-id="f0acc-111">`ApplyMultiControlled` always calls `singlyControlledOp` with an argument of length at least 1.</span></span>


### <a name="ccnot--ccnotop"></a><span data-ttu-id="f0acc-112">ккнот: [ккнотоп](xref:Microsoft.Quantum.Canon.CCNOTop)</span><span class="sxs-lookup"><span data-stu-id="f0acc-112">ccnot : [CCNOTop](xref:Microsoft.Quantum.Canon.CCNOTop)</span></span>

<span data-ttu-id="f0acc-113">Шлюз с управляемым контролем, не используемый для построения.</span><span class="sxs-lookup"><span data-stu-id="f0acc-113">The controlled-controlled-NOT gate to use for the construction.</span></span>


### <a name="controls--qubit"></a><span data-ttu-id="f0acc-114">элементы управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f0acc-114">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f0acc-115">Кубитс, управление которым должно осуществляться `singlyControlledOp` .</span><span class="sxs-lookup"><span data-stu-id="f0acc-115">The qubits that `singlyControlledOp` is to be controlled on.</span></span>
<span data-ttu-id="f0acc-116">Длина `controls` должна быть не меньше 1.</span><span class="sxs-lookup"><span data-stu-id="f0acc-116">The length of `controls` must be at least 1.</span></span>


### <a name="targets--qubit"></a><span data-ttu-id="f0acc-117">целевые объекты: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f0acc-117">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f0acc-118">Целевой Кубитс, на `singlyControlledOp` основе которого действует.</span><span class="sxs-lookup"><span data-stu-id="f0acc-118">The target qubits that `singlyControlledOp` acts upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f0acc-119">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f0acc-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f0acc-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="f0acc-120">Remarks</span></span>

<span data-ttu-id="f0acc-121">Эта операция использует только чистый анЦилла Кубитс.</span><span class="sxs-lookup"><span data-stu-id="f0acc-121">This operation uses only clean ancilla qubits.</span></span>

<span data-ttu-id="f0acc-122">Описание и схема схемы см. на рис. 4,10 раздела 4,3 в Nielsen & Чжуанский</span><span class="sxs-lookup"><span data-stu-id="f0acc-122">For the explanation and circuit diagram see Figure 4.10, Section 4.3 in Nielsen & Chuang</span></span>

## <a name="references"></a><span data-ttu-id="f0acc-123">Ссылки</span><span class="sxs-lookup"><span data-stu-id="f0acc-123">References</span></span>

- [<span data-ttu-id="f0acc-124">*Майкл A. Nielsen, Исаак L. Чжуанский* , вычисление такта и сведения о такте</span><span class="sxs-lookup"><span data-stu-id="f0acc-124"> *Michael A. Nielsen , Isaac L. Chuang* , Quantum Computation and Quantum Information </span></span>](http://doi.org/10.1017/CBO9780511976667)

## <a name="see-also"></a><span data-ttu-id="f0acc-125">См. также:</span><span class="sxs-lookup"><span data-stu-id="f0acc-125">See Also</span></span>

- [<span data-ttu-id="f0acc-126">Microsoft. тактов. Canon. Апплимултиконтролледк</span><span class="sxs-lookup"><span data-stu-id="f0acc-126">Microsoft.Quantum.Canon.ApplyMultiControlledC</span></span>](xref:Microsoft.Quantum.Canon.ApplyMultiControlledC)