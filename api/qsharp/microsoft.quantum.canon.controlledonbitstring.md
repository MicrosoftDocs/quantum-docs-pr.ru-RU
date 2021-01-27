---
uid: Microsoft.Quantum.Canon.ControlledOnBitString
title: Функция Контролледонбитстринг
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnBitString
qsharp.summary: Returns a unitary operation that applies an oracle on the target register if the control register state corresponds to a specified bit mask.
ms.openlocfilehash: 176170cc972ca67b812b84f79cf97ba5418be9b6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840802"
---
# <a name="controlledonbitstring-function"></a><span data-ttu-id="94f78-102">Функция Контролледонбитстринг</span><span class="sxs-lookup"><span data-stu-id="94f78-102">ControlledOnBitString function</span></span>

<span data-ttu-id="94f78-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="94f78-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="94f78-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="94f78-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="94f78-105">Возвращает единую операцию, которая применяет Oracle к целевой регистрации, если состояние регистра элемента управления соответствует заданной битовой маске.</span><span class="sxs-lookup"><span data-stu-id="94f78-105">Returns a unitary operation that applies an oracle on the target register if the control register state corresponds to a specified bit mask.</span></span>

```qsharp
function ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="description"></a><span data-ttu-id="94f78-106">Описание</span><span class="sxs-lookup"><span data-stu-id="94f78-106">Description</span></span>

<span data-ttu-id="94f78-107">Выходные данные этой функции представляют собой операцию, которая может быть представлена единым преобразованием $U $ таким, что \бегин{алигн} U \кет{b_0 b_1 \кдотс b_ {n-1}} \кет{\пси} = \кет{b_0 b_1 \кдотс b_ {n-1}} \отимес \бегин{Касес} V \кет{\пси} & \textrm{if} (b_0 b_1 \cdots b_ {n-1}) = \texttt{BITS} \\ \\ \ket{\psi} & \textrm{otherwise} \end{cases} \end{align}, где $V $ является единым преобразованием, представляющим действие `oracle` операции.</span><span class="sxs-lookup"><span data-stu-id="94f78-107">The output of this function is an operation that can be represented by a unitary transformation $U$ such that \begin{align} U \ket{b_0 b_1 \cdots b_{n - 1}} \ket{\psi} = \ket{b_0 b_1 \cdots b_{n-1}} \otimes \begin{cases} V \ket{\psi} & \textrm{if} (b_0 b_1 \cdots b_{n - 1}) = \texttt{bits} \\\\ \ket{\psi} & \textrm{otherwise} \end{cases}, \end{align} where $V$ is a unitary transformation that represents the action of the `oracle` operation.</span></span>

## <a name="input"></a><span data-ttu-id="94f78-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="94f78-108">Input</span></span>

### <a name="bits--bool"></a><span data-ttu-id="94f78-109">Разрядность: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="94f78-109">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="94f78-110">Битовая строка для управления данной единой операцией в.</span><span class="sxs-lookup"><span data-stu-id="94f78-110">The bit string to control the given unitary operation on.</span></span>


### <a name="oracle--t--unit--is-adj--ctl"></a><span data-ttu-id="94f78-111">Oracle: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="94f78-111">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="94f78-112">Единая операция, применяемая к целевому регистру.</span><span class="sxs-lookup"><span data-stu-id="94f78-112">The unitary operation to be applied on the target register.</span></span>



## <a name="output--qubitt--unit--is-adj--ctl"></a><span data-ttu-id="94f78-113">Выходные данные: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[], 't) => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="94f78-113">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="94f78-114">Единая операция, которая применяется к `oracle` целевому регистру, если контрольное состояние регистра соответствует битовой маске `bits` .</span><span class="sxs-lookup"><span data-stu-id="94f78-114">A unitary operation that applies `oracle` on the target register if the control register state corresponds to the bit mask `bits`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="94f78-115">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="94f78-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="94f78-116">Е</span><span class="sxs-lookup"><span data-stu-id="94f78-116">'T</span></span>



## <a name="example"></a><span data-ttu-id="94f78-117">Пример</span><span class="sxs-lookup"><span data-stu-id="94f78-117">Example</span></span>

<span data-ttu-id="94f78-118">Следующие фрагменты кода эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="94f78-118">The following code snippets are equivalent:</span></span>

```qsharp
(ControlledOnBitString(bits, oracle))(controlRegister, targetRegister);
```

<span data-ttu-id="94f78-119">и</span><span class="sxs-lookup"><span data-stu-id="94f78-119">and</span></span>

```qsharp
within {
    ApplyPauliFromBitString(PauliX, false, bits, controlRegister);
} apply {
    Controlled oracle(controlRegister, targetRegister);
}
```

<span data-ttu-id="94f78-120">Следующий код подготавливает состояние $ \фрак {1} {2} (\кет {00} -\кет {01} + \кет {10} + \кет {11} ) $:</span><span class="sxs-lookup"><span data-stu-id="94f78-120">The following code prepares a state $\frac{1}{2}(\ket{00} - \ket{01} + \ket{10} + \ket{11})$:</span></span>

```qsharp
using (register = Qubit[2]) {
    ApplyToEach(H, register);
    (ControlledOnBitString([false], Z))(register[0..0], register[1]);
}
```

## <a name="remarks"></a><span data-ttu-id="94f78-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="94f78-121">Remarks</span></span>

<span data-ttu-id="94f78-122">Шаблон, заданный параметром `bits` , может быть короче `controlRegister` , в этом случае дополнительные элементы управления Кубитс игнорируются (то есть не контролируются в $ \кет {0} $ и $ \кет {1} $).</span><span class="sxs-lookup"><span data-stu-id="94f78-122">The pattern given by `bits` may be shorter than `controlRegister`, in which case additional control qubits are ignored (that is, neither controlled on $\ket{0}$ nor $\ket{1}$).</span></span>
<span data-ttu-id="94f78-123">Если `bits` значение больше `controlRegister` , возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="94f78-123">If `bits` is longer than `controlRegister`, an error is raised.</span></span>

<span data-ttu-id="94f78-124">При наличии логического массива `bits` и отдельной операции `oracle` выходные данные этой функции являются операцией, которая выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="94f78-124">Given a Boolean array `bits` and a unitary operation `oracle`, the output of this function is an operation that performs the following steps:</span></span>

* <span data-ttu-id="94f78-125">Примените `X` операцию к каждому кубит регистру элемента управления, соответствующему `false` элементу объекта `bits` .</span><span class="sxs-lookup"><span data-stu-id="94f78-125">apply an `X` operation to each qubit of the control register that corresponds to `false` element of the `bits`;</span></span>
* <span data-ttu-id="94f78-126">применяется `Controlled oracle` к контрольным и целевым регистрам.</span><span class="sxs-lookup"><span data-stu-id="94f78-126">apply `Controlled oracle` to the control and target registers;</span></span>
* <span data-ttu-id="94f78-127">Примените `X` операцию к каждому кубит контрольного регистра, который соответствует `false` элементу объекта, `bits` чтобы вернуть Контрольный регистр к исходному состоянию.</span><span class="sxs-lookup"><span data-stu-id="94f78-127">apply an `X` operation to each qubit of the control register that corresponds to `false` element of the `bits` again to return the control register to the original state.</span></span>

<span data-ttu-id="94f78-128">Выходные данные `Controlled` функтор являются особым случаем, `ControlledOnBitString` где `bits` равно `[true, ..., true]` .</span><span class="sxs-lookup"><span data-stu-id="94f78-128">The output of the `Controlled` functor is a special case of `ControlledOnBitString` where `bits` is equal to `[true, ..., true]`.</span></span>