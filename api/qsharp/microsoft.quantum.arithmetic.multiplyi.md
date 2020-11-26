---
uid: Microsoft.Quantum.Arithmetic.MultiplyI
title: Операция Мултипли
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyI
qsharp.summary: Multiply integer `xs` by integer `ys` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 96922f0147788b37cc9bace5154288a722d4ba95
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222513"
---
# <a name="multiplyi-operation"></a><span data-ttu-id="011a2-102">Операция Мултипли</span><span class="sxs-lookup"><span data-stu-id="011a2-102">MultiplyI operation</span></span>

<span data-ttu-id="011a2-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="011a2-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="011a2-104">Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="011a2-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="011a2-105">Умножьте целое число `xs` на целое `ys` и сохраните результат в `result` , который должен быть равен нулю изначально.</span><span class="sxs-lookup"><span data-stu-id="011a2-105">Multiply integer `xs` by integer `ys` and store the result in `result`, which must be zero initially.</span></span>

```qsharp
operation MultiplyI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="011a2-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="011a2-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="011a2-107">xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="011a2-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="011a2-108">$n $-bit множимое (Литтлиндиан)</span><span class="sxs-lookup"><span data-stu-id="011a2-108">$n$-bit multiplicand (LittleEndian)</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="011a2-109">ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="011a2-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="011a2-110">$n $-разрядный множитель (Литтлиндиан)</span><span class="sxs-lookup"><span data-stu-id="011a2-110">$n$-bit multiplier (LittleEndian)</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="011a2-111">результат: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="011a2-111">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="011a2-112">$2N $-bit Result (Литтлиндиан) должен находиться в состоянии $ \кет {0} $ изначально.</span><span class="sxs-lookup"><span data-stu-id="011a2-112">$2n$-bit result (LittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="011a2-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="011a2-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="011a2-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="011a2-114">Remarks</span></span>

<span data-ttu-id="011a2-115">Использует стандартный подход Shift и-Add для реализации умножения.</span><span class="sxs-lookup"><span data-stu-id="011a2-115">Uses a standard shift-and-add approach to implement the multiplication.</span></span>
<span data-ttu-id="011a2-116">Управляемая версия была улучшена путем копирования $x _i $ в анЦилла кубит, на Кубитс элемента управления, а затем управления добавлением анЦилла кубит.</span><span class="sxs-lookup"><span data-stu-id="011a2-116">The controlled version was improved by copying out $x_i$ to an ancilla qubit conditioned on the control qubits, and then controlling the addition on the ancilla qubit.</span></span>