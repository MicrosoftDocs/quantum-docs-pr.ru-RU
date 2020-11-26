---
uid: Microsoft.Quantum.Canon.ApplyControlledOnInt
title: Операция Аппликонтролледонинт
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnInt
qsharp.summary: Applies a unitary operation on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 3dd17e6bc913e84941a6b81f134e60536a4c4122
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219011"
---
# <a name="applycontrolledonint-operation"></a><span data-ttu-id="52793-102">Операция Аппликонтролледонинт</span><span class="sxs-lookup"><span data-stu-id="52793-102">ApplyControlledOnInt operation</span></span>

<span data-ttu-id="52793-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="52793-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="52793-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="52793-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="52793-105">Применяет единую операцию к целевой регистрации, если контрольное состояние реестра соответствует заданному положительному целому числу.</span><span class="sxs-lookup"><span data-stu-id="52793-105">Applies a unitary operation on the target register if the control register state corresponds to a specified positive integer.</span></span>

```qsharp
operation ApplyControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="52793-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="52793-106">Input</span></span>

### <a name="numberstate--int"></a><span data-ttu-id="52793-107">Нумберстате: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="52793-107">numberState : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="52793-108">Неотрицательное целое число, на которое `oracle` должна контролироваться операция.</span><span class="sxs-lookup"><span data-stu-id="52793-108">A nonnegative integer on which the operation `oracle` should be controlled.</span></span>


### <a name="oracle--t--unit--is-adj--ctl"></a><span data-ttu-id="52793-109">Oracle: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="52793-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="52793-110">Единая операция для управления.</span><span class="sxs-lookup"><span data-stu-id="52793-110">A unitary operation to be controlled.</span></span>


### <a name="controlregister--qubit"></a><span data-ttu-id="52793-111">Контролрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="52793-111">controlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="52793-112">Регистр такта, который управляет приложением `oracle` .</span><span class="sxs-lookup"><span data-stu-id="52793-112">A quantum register that controls application of `oracle`.</span></span>


### <a name="targetregister--t"></a><span data-ttu-id="52793-113">Таржетрегистер: 'T</span><span class="sxs-lookup"><span data-stu-id="52793-113">targetRegister : 'T</span></span>

<span data-ttu-id="52793-114">Регистр, к которому применяется `oracle` .</span><span class="sxs-lookup"><span data-stu-id="52793-114">A register on which to apply `oracle`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="52793-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="52793-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="52793-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="52793-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="52793-117">Е</span><span class="sxs-lookup"><span data-stu-id="52793-117">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="52793-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="52793-118">Remarks</span></span>

<span data-ttu-id="52793-119">Значение `numberState` интерпретируется с помощью кодировки с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="52793-119">The value of `numberState` is interpreted using a little-endian encoding.</span></span>

<span data-ttu-id="52793-120">`numberState` должно быть не более $2 ^ \Тексттт{ленгс (Контролрегистер)}-$1.</span><span class="sxs-lookup"><span data-stu-id="52793-120">`numberState` must be at most $2^\texttt{Length(controlRegister)} - 1$.</span></span>
<span data-ttu-id="52793-121">Например, это `numberState = 537` означает, что `oracle` применяется только в том случае, если `controlRegister` параметр имеет значение в состоянии $ \кет {537} $.</span><span class="sxs-lookup"><span data-stu-id="52793-121">For example, `numberState = 537` means that `oracle` is applied if and only if `controlRegister` is in the state $\ket{537}$.</span></span>