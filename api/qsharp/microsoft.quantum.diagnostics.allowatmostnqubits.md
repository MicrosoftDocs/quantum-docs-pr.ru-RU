---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNQubits
title: Операция Алловатмостнкубитс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNQubits
qsharp.summary: Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.
ms.openlocfilehash: 3aa80767ac0f752e7be0efa2966c580ca3cb8f19
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830918"
---
# <a name="allowatmostnqubits-operation"></a><span data-ttu-id="fdbf5-102">Операция Алловатмостнкубитс</span><span class="sxs-lookup"><span data-stu-id="fdbf5-102">AllowAtMostNQubits operation</span></span>

<span data-ttu-id="fdbf5-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="fdbf5-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="fdbf5-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fdbf5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fdbf5-105">Между вызовом этой операции и ее примыкающей к ней утверждается, что по меньшей мере заданное число дополнительных Кубитс выделяется с помощью инструкций using.</span><span class="sxs-lookup"><span data-stu-id="fdbf5-105">Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.</span></span>

```qsharp
operation AllowAtMostNQubits (nQubits : Int, message : String) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="fdbf5-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fdbf5-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="fdbf5-107">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fdbf5-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="fdbf5-108">Максимальное число Кубитс, которые могут быть выделены.</span><span class="sxs-lookup"><span data-stu-id="fdbf5-108">The maximum number of qubits that may be allocated.</span></span>


### <a name="message--string"></a><span data-ttu-id="fdbf5-109">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="fdbf5-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="fdbf5-110">Сообщение, отображаемое при сбое.</span><span class="sxs-lookup"><span data-stu-id="fdbf5-110">A message to be displayed upon failure.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fdbf5-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fdbf5-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="fdbf5-112">Пример</span><span class="sxs-lookup"><span data-stu-id="fdbf5-112">Example</span></span>

<span data-ttu-id="fdbf5-113">Следующий фрагмент кода завершится ошибкой при выполнении на компьютерах, поддерживающих эту диагностику:</span><span class="sxs-lookup"><span data-stu-id="fdbf5-113">The following snippet will fail when executed on machines which support this diagnostic:</span></span>

```qsharp
within {
    AllowAtMostNQubits(3, "Too many qubits allocated.");
} apply {
    // Fails since this allocates four qubits.
    using (register = Qubit[4]) {
    }
}
```

## <a name="remarks"></a><span data-ttu-id="fdbf5-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="fdbf5-114">Remarks</span></span>

<span data-ttu-id="fdbf5-115">Эта операция может быть заменена на неработающие целевые объекты, которые не поддерживают эту операцию.</span><span class="sxs-lookup"><span data-stu-id="fdbf5-115">This operation may be replaced by a no-op on targets which do not support it.</span></span>