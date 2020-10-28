---
uid: Microsoft.Quantum.Canon.ControlledOnInt
title: Функция Контролледонинт
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnInt
qsharp.summary: Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 4c48f3257f91fc50040d02cae7c2f7bdf87ea7c5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716419"
---
# <a name="controlledonint-function"></a><span data-ttu-id="206a1-102">Функция Контролледонинт</span><span class="sxs-lookup"><span data-stu-id="206a1-102">ControlledOnInt function</span></span>

<span data-ttu-id="206a1-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="206a1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="206a1-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="206a1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="206a1-105">Возвращает оператор, который применяет объект Oracle к целевой регистрации, если состояние регистра элемента управления соответствует заданному положительному целому числу.</span><span class="sxs-lookup"><span data-stu-id="206a1-105">Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.</span></span>

```qsharp
function ControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="206a1-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="206a1-106">Input</span></span>

### <a name="numberstate--int"></a><span data-ttu-id="206a1-107">Нумберстате: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="206a1-107">numberState : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="206a1-108">Положительное целое число.</span><span class="sxs-lookup"><span data-stu-id="206a1-108">Positive integer.</span></span>


### <a name="oracle--t--unit-adj--ctl"></a><span data-ttu-id="206a1-109">Oracle: 'T => [модульные](xref:microsoft.quantum.lang-ref.unit) года + CTL</span><span class="sxs-lookup"><span data-stu-id="206a1-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="206a1-110">Оператор с единым.</span><span class="sxs-lookup"><span data-stu-id="206a1-110">Unitary operator.</span></span>



## <a name="output--qubitt--unit-adj--ctl"></a><span data-ttu-id="206a1-111">Выходные данные: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[], 't) = [>ная](xref:microsoft.quantum.lang-ref.unit) Расгода и список доверия</span><span class="sxs-lookup"><span data-stu-id="206a1-111">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="206a1-112">Оператор, применяемый к `oracle` целевому регистру, если состояние регистра элемента управления соответствует состоянию числа `numberState` .</span><span class="sxs-lookup"><span data-stu-id="206a1-112">A unitary operator that applies `oracle` on the target register if the control register state corresponds to the number state `numberState`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="206a1-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="206a1-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="206a1-114">Е</span><span class="sxs-lookup"><span data-stu-id="206a1-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="206a1-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="206a1-115">Remarks</span></span>

<span data-ttu-id="206a1-116">Значение `numberState` интерпретируется с помощью кодировки с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="206a1-116">The value of `numberState` is interpreted using a little-endian encoding.</span></span>