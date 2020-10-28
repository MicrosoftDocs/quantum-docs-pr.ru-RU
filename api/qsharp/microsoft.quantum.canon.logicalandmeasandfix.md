---
uid: Microsoft.Quantum.Canon.LogicalANDMeasAndFix
title: Операция Логикаландмеасандфикс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: LogicalANDMeasAndFix
qsharp.summary: Computes the logical AND of multiple qubits.
ms.openlocfilehash: 86e4b9a8c6ed5f4f56db0ceefc8051d34e911c4c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715929"
---
# <a name="logicalandmeasandfix-operation"></a><span data-ttu-id="ba042-102">Операция Логикаландмеасандфикс</span><span class="sxs-lookup"><span data-stu-id="ba042-102">LogicalANDMeasAndFix operation</span></span>

<span data-ttu-id="ba042-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ba042-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ba042-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ba042-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ba042-105">Вычисление логического и для нескольких Кубитс.</span><span class="sxs-lookup"><span data-stu-id="ba042-105">Computes the logical AND of multiple qubits.</span></span>

```qsharp
operation LogicalANDMeasAndFix (ctrlRegister : Qubit[], target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="ba042-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ba042-106">Input</span></span>

### <a name="ctrlregister--qubit"></a><span data-ttu-id="ba042-107">Ктрлрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ba042-107">ctrlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="ba042-108">Кубитс входные данные для нескольких входных и многоэлементных шлюзов.</span><span class="sxs-lookup"><span data-stu-id="ba042-108">Qubits input to the multiple-input AND gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="ba042-109">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="ba042-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="ba042-110">Кубит, в который записывается вывод и.</span><span class="sxs-lookup"><span data-stu-id="ba042-110">Qubit on which output of AND is written to.</span></span> <span data-ttu-id="ba042-111">Предполагается, что всегда начинается в состоянии $ \кет {0} $.</span><span class="sxs-lookup"><span data-stu-id="ba042-111">This is assumed to always start in the $\ket{0}$ state.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ba042-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ba042-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="ba042-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="ba042-113">Remarks</span></span>

<span data-ttu-id="ba042-114">Если `ctrlRegister` имеет ровно $2 $ Кубитс, это эквивалентно операции, `CCNOT` но этапу $e ^ {i \ PI/2} $ on $ \кет {001} $ и $-e ^ {i \ PI/2} $ on $ \кет {101} $ and $ \кет {011} $.</span><span class="sxs-lookup"><span data-stu-id="ba042-114">When `ctrlRegister` has exactly $2$ qubits, this is equivalent to the `CCNOT` operation but phase with a phase $e^{i\Pi/2}$ on $\ket{001}$ and $-e^{i\Pi/2}$ on $\ket{101}$ and $\ket{011}$.</span></span>
<span data-ttu-id="ba042-115">Смежная функция также является подходом меры и адресной привязки, которая является инверсией исходной операции только в особых случаях (см. ссылки), но использует меньше T-шлюзов.</span><span class="sxs-lookup"><span data-stu-id="ba042-115">The Adjoint is also measure-and-fixup approach that is the inverse of the original operation only in special cases (see references), but uses fewer T-gates.</span></span>

## <a name="references"></a><span data-ttu-id="ba042-116">Ссылки</span><span class="sxs-lookup"><span data-stu-id="ba042-116">References</span></span>

- [<span data-ttu-id="ba042-117">*Крейг гиднэй* , 1709,06648</span><span class="sxs-lookup"><span data-stu-id="ba042-117"> *Craig Gidney* , 1709.06648</span></span>](https://arxiv.org/abs/1709.06648)