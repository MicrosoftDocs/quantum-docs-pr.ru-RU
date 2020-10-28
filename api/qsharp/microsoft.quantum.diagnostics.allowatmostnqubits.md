---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNQubits
title: Операция Алловатмостнкубитс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNQubits
qsharp.summary: Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.
ms.openlocfilehash: ddbed96df0d95cfd78730c091a6a81ee6e49c349
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713059"
---
# <a name="allowatmostnqubits-operation"></a><span data-ttu-id="99407-102">Операция Алловатмостнкубитс</span><span class="sxs-lookup"><span data-stu-id="99407-102">AllowAtMostNQubits operation</span></span>

<span data-ttu-id="99407-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="99407-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="99407-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="99407-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="99407-105">Между вызовом этой операции и ее примыкающей к ней утверждается, что по меньшей мере заданное число дополнительных Кубитс выделяется с помощью инструкций using.</span><span class="sxs-lookup"><span data-stu-id="99407-105">Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.</span></span>

```qsharp
operation AllowAtMostNQubits (nQubits : Int, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="99407-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="99407-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="99407-107">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="99407-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="99407-108">Максимальное число Кубитс, которые могут быть выделены.</span><span class="sxs-lookup"><span data-stu-id="99407-108">The maximum number of qubits that may be allocated.</span></span>


### <a name="message--string"></a><span data-ttu-id="99407-109">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="99407-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="99407-110">Сообщение, отображаемое при сбое.</span><span class="sxs-lookup"><span data-stu-id="99407-110">A message to be displayed upon failure.</span></span>



## <a name="output--unit"></a><span data-ttu-id="99407-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="99407-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="99407-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="99407-112">Remarks</span></span>

<span data-ttu-id="99407-113">Эта операция может быть заменена на неработающие целевые объекты, которые не поддерживают эту операцию.</span><span class="sxs-lookup"><span data-stu-id="99407-113">This operation may be replaced by a no-op on targets which do not support it.</span></span>