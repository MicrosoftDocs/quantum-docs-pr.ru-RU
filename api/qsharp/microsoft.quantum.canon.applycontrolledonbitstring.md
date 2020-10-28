---
uid: Microsoft.Quantum.Canon.ApplyControlledOnBitString
title: Операция Аппликонтролледонбитстринг
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnBitString
qsharp.summary: Applies a unitary operation on the target register, controlled on a a state specified by a given bit mask.
ms.openlocfilehash: 7a054511bacff574e6f7e889ace048c78886cf91
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729673"
---
# <a name="applycontrolledonbitstring-operation"></a><span data-ttu-id="e3dbb-102">Операция Аппликонтролледонбитстринг</span><span class="sxs-lookup"><span data-stu-id="e3dbb-102">ApplyControlledOnBitString operation</span></span>

<span data-ttu-id="e3dbb-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e3dbb-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e3dbb-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e3dbb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e3dbb-105">Применяет единую операцию к целевой регистру, контролируя состояние, заданное заданной битовой маской.</span><span class="sxs-lookup"><span data-stu-id="e3dbb-105">Applies a unitary operation on the target register, controlled on a a state specified by a given bit mask.</span></span>

```qsharp
operation ApplyControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="e3dbb-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e3dbb-106">Input</span></span>

### <a name="bits--bool"></a><span data-ttu-id="e3dbb-107">Разрядность: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="e3dbb-107">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="e3dbb-108">Битовая строка для управления данной единой операцией в.</span><span class="sxs-lookup"><span data-stu-id="e3dbb-108">The bit string to control the given unitary operation on.</span></span>


### <a name="oracle--t--unit-adj--ctl"></a><span data-ttu-id="e3dbb-109">Oracle: 'T => [модульные](xref:microsoft.quantum.lang-ref.unit) года + CTL</span><span class="sxs-lookup"><span data-stu-id="e3dbb-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="e3dbb-110">Единая операция, применяемая к целевому регистру.</span><span class="sxs-lookup"><span data-stu-id="e3dbb-110">The unitary operation to be applied on the target register.</span></span>


### <a name="controlregister--qubit"></a><span data-ttu-id="e3dbb-111">Контролрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="e3dbb-111">controlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e3dbb-112">Регистр такта, который управляет приложением `oracle` .</span><span class="sxs-lookup"><span data-stu-id="e3dbb-112">A quantum register that controls application of `oracle`.</span></span>


### <a name="targetregister--t"></a><span data-ttu-id="e3dbb-113">Таржетрегистер: 'T</span><span class="sxs-lookup"><span data-stu-id="e3dbb-113">targetRegister : 'T</span></span>

<span data-ttu-id="e3dbb-114">Целевой регистр, передаваемый в `oracle` качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="e3dbb-114">The target register to be passed to `oracle` as an input.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e3dbb-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e3dbb-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e3dbb-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="e3dbb-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e3dbb-117">Е</span><span class="sxs-lookup"><span data-stu-id="e3dbb-117">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="e3dbb-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="e3dbb-118">Remarks</span></span>

<span data-ttu-id="e3dbb-119">Шаблон, заданный параметром `bits` , может быть короче `controlRegister` , в этом случае дополнительные элементы управления Кубитс игнорируются (то есть не контролируются в $ \кет {0} $ и $ \кет {1} $).</span><span class="sxs-lookup"><span data-stu-id="e3dbb-119">The pattern given by `bits` may be shorter than `controlRegister`, in which case additional control qubits are ignored (that is, neither controlled on $\ket{0}$ nor $\ket{1}$).</span></span>
<span data-ttu-id="e3dbb-120">Если `bits` значение больше `controlRegister` , возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="e3dbb-120">If `bits` is longer than `controlRegister`, an error is raised.</span></span>

<span data-ttu-id="e3dbb-121">Например, это `bits = [0,1,0,0,1]` означает, что `oracle` применяется только в том случае, если `controlRegister` параметр имеет значение в состоянии $ \кет {0} \кет {1} \кет {0} \кет {0} \кет {1} $.</span><span class="sxs-lookup"><span data-stu-id="e3dbb-121">For example, `bits = [0,1,0,0,1]` means that `oracle` is applied if and only if `controlRegister` is in the state $\ket{0}\ket{1}\ket{0}\ket{0}\ket{1}$.</span></span>