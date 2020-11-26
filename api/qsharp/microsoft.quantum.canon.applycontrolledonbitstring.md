---
uid: Microsoft.Quantum.Canon.ApplyControlledOnBitString
title: Операция Аппликонтролледонбитстринг
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnBitString
qsharp.summary: Applies a unitary operation on the target register, controlled on a a state specified by a given bit mask.
ms.openlocfilehash: 6947d2dbdec4cfbb592143024a7c8ccd53a32029
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219079"
---
# <a name="applycontrolledonbitstring-operation"></a><span data-ttu-id="d3598-102">Операция Аппликонтролледонбитстринг</span><span class="sxs-lookup"><span data-stu-id="d3598-102">ApplyControlledOnBitString operation</span></span>

<span data-ttu-id="d3598-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d3598-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d3598-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d3598-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d3598-105">Применяет единую операцию к целевой регистру, контролируя состояние, заданное заданной битовой маской.</span><span class="sxs-lookup"><span data-stu-id="d3598-105">Applies a unitary operation on the target register, controlled on a a state specified by a given bit mask.</span></span>

```qsharp
operation ApplyControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="d3598-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d3598-106">Input</span></span>

### <a name="bits--bool"></a><span data-ttu-id="d3598-107">Разрядность: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="d3598-107">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="d3598-108">Битовая строка для управления данной единой операцией в.</span><span class="sxs-lookup"><span data-stu-id="d3598-108">The bit string to control the given unitary operation on.</span></span>


### <a name="oracle--t--unit--is-adj--ctl"></a><span data-ttu-id="d3598-109">Oracle: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="d3598-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="d3598-110">Единая операция, применяемая к целевому регистру.</span><span class="sxs-lookup"><span data-stu-id="d3598-110">The unitary operation to be applied on the target register.</span></span>


### <a name="controlregister--qubit"></a><span data-ttu-id="d3598-111">Контролрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d3598-111">controlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d3598-112">Регистр такта, который управляет приложением `oracle` .</span><span class="sxs-lookup"><span data-stu-id="d3598-112">A quantum register that controls application of `oracle`.</span></span>


### <a name="targetregister--t"></a><span data-ttu-id="d3598-113">Таржетрегистер: 'T</span><span class="sxs-lookup"><span data-stu-id="d3598-113">targetRegister : 'T</span></span>

<span data-ttu-id="d3598-114">Целевой регистр, передаваемый в `oracle` качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="d3598-114">The target register to be passed to `oracle` as an input.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d3598-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d3598-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d3598-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="d3598-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d3598-117">Е</span><span class="sxs-lookup"><span data-stu-id="d3598-117">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="d3598-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d3598-118">Remarks</span></span>

<span data-ttu-id="d3598-119">Шаблон, заданный параметром `bits` , может быть короче `controlRegister` , в этом случае дополнительные элементы управления Кубитс игнорируются (то есть не контролируются в $ \кет {0} $ и $ \кет {1} $).</span><span class="sxs-lookup"><span data-stu-id="d3598-119">The pattern given by `bits` may be shorter than `controlRegister`, in which case additional control qubits are ignored (that is, neither controlled on $\ket{0}$ nor $\ket{1}$).</span></span>
<span data-ttu-id="d3598-120">Если `bits` значение больше `controlRegister` , возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="d3598-120">If `bits` is longer than `controlRegister`, an error is raised.</span></span>

<span data-ttu-id="d3598-121">Например, это `bits = [0,1,0,0,1]` означает, что `oracle` применяется только в том случае, если `controlRegister` параметр имеет значение в состоянии $ \кет {0} \кет {1} \кет {0} \кет {0} \кет {1} $.</span><span class="sxs-lookup"><span data-stu-id="d3598-121">For example, `bits = [0,1,0,0,1]` means that `oracle` is applied if and only if `controlRegister` is in the state $\ket{0}\ket{1}\ket{0}\ket{0}\ket{1}$.</span></span>