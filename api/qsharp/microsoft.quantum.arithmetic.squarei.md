---
uid: Microsoft.Quantum.Arithmetic.SquareI
title: Операция Скуареи
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareI
qsharp.summary: Computes the square of the integer `xs` into `result`, which must be zero initially.
ms.openlocfilehash: 79a431d411c4ffd502fb5338b5396341fd63aea8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221867"
---
# <a name="squarei-operation"></a><span data-ttu-id="e93a8-102">Операция Скуареи</span><span class="sxs-lookup"><span data-stu-id="e93a8-102">SquareI operation</span></span>

<span data-ttu-id="e93a8-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="e93a8-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="e93a8-104">Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="e93a8-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="e93a8-105">Вычисляет квадрат целого числа `xs` в `result` , который должен быть равен нулю изначально.</span><span class="sxs-lookup"><span data-stu-id="e93a8-105">Computes the square of the integer `xs` into `result`, which must be zero initially.</span></span>

```qsharp
operation SquareI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="e93a8-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e93a8-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="e93a8-107">xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="e93a8-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="e93a8-108">$n $-разрядное число в квадрат (Литтлиндиан)</span><span class="sxs-lookup"><span data-stu-id="e93a8-108">$n$-bit number to square (LittleEndian)</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="e93a8-109">результат: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="e93a8-109">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="e93a8-110">$2N $-bit Result (Литтлиндиан) должен находиться в состоянии $ \кет {0} $ изначально.</span><span class="sxs-lookup"><span data-stu-id="e93a8-110">$2n$-bit result (LittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e93a8-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e93a8-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="e93a8-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e93a8-112">Remarks</span></span>

<span data-ttu-id="e93a8-113">Использует стандартный подход Shift и-Add для расчета квадрата.</span><span class="sxs-lookup"><span data-stu-id="e93a8-113">Uses a standard shift-and-add approach to compute the square.</span></span> <span data-ttu-id="e93a8-114">Сохраняет $n-$1 Кубитс по сравнению с прямым решением, которое сначала копирует XS перед применением обычного множителя, а затем отменяет операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="e93a8-114">Saves $n-1$ qubits compared to the straight-forward solution which first copies out xs before applying a regular multiplier and then undoing the copy operation.</span></span>