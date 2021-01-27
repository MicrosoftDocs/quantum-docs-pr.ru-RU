---
uid: Microsoft.Quantum.Canon.ControlledOnInt
title: Функция Контролледонинт
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnInt
qsharp.summary: Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 6c7f46c44f2a2427f702e463195f26660cb4fca1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840784"
---
# <a name="controlledonint-function"></a><span data-ttu-id="c1433-102">Функция Контролледонинт</span><span class="sxs-lookup"><span data-stu-id="c1433-102">ControlledOnInt function</span></span>

<span data-ttu-id="c1433-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c1433-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c1433-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c1433-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c1433-105">Возвращает оператор, который применяет объект Oracle к целевой регистрации, если состояние регистра элемента управления соответствует заданному положительному целому числу.</span><span class="sxs-lookup"><span data-stu-id="c1433-105">Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.</span></span>

```qsharp
function ControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="c1433-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c1433-106">Input</span></span>

### <a name="numberstate--int"></a><span data-ttu-id="c1433-107">Нумберстате: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c1433-107">numberState : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c1433-108">Положительное целое число.</span><span class="sxs-lookup"><span data-stu-id="c1433-108">Positive integer.</span></span>


### <a name="oracle--t--unit--is-adj--ctl"></a><span data-ttu-id="c1433-109">Oracle: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="c1433-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="c1433-110">Оператор с единым.</span><span class="sxs-lookup"><span data-stu-id="c1433-110">Unitary operator.</span></span>



## <a name="output--qubitt--unit--is-adj--ctl"></a><span data-ttu-id="c1433-111">Выходные данные: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[], 't) => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="c1433-111">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="c1433-112">Оператор, применяемый к `oracle` целевому регистру, если состояние регистра элемента управления соответствует состоянию числа `numberState` .</span><span class="sxs-lookup"><span data-stu-id="c1433-112">A unitary operator that applies `oracle` on the target register if the control register state corresponds to the number state `numberState`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="c1433-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="c1433-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c1433-114">Е</span><span class="sxs-lookup"><span data-stu-id="c1433-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="c1433-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="c1433-115">Remarks</span></span>

<span data-ttu-id="c1433-116">Значение `numberState` интерпретируется с помощью кодировки с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="c1433-116">The value of `numberState` is interpreted using a little-endian encoding.</span></span>