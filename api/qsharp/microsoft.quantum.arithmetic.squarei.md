---
uid: Microsoft.Quantum.Arithmetic.SquareI
title: Операция Скуареи
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareI
qsharp.summary: Computes the square of the integer `xs` into `result`, which must be zero initially.
ms.openlocfilehash: d7334d50f245ba358624e6e2eee94b63d9ed7569
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730464"
---
# <a name="squarei-operation"></a><span data-ttu-id="029c2-102">Операция Скуареи</span><span class="sxs-lookup"><span data-stu-id="029c2-102">SquareI operation</span></span>

<span data-ttu-id="029c2-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="029c2-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="029c2-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="029c2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="029c2-105">Вычисляет квадрат целого числа `xs` в `result` , который должен быть равен нулю изначально.</span><span class="sxs-lookup"><span data-stu-id="029c2-105">Computes the square of the integer `xs` into `result`, which must be zero initially.</span></span>

```qsharp
operation SquareI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="029c2-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="029c2-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="029c2-107">xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="029c2-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="029c2-108">$n $-разрядное число в квадрат (Литтлиндиан)</span><span class="sxs-lookup"><span data-stu-id="029c2-108">$n$-bit number to square (LittleEndian)</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="029c2-109">результат: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="029c2-109">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="029c2-110">$2N $-bit Result (Литтлиндиан) должен находиться в состоянии $ \кет {0} $ изначально.</span><span class="sxs-lookup"><span data-stu-id="029c2-110">$2n$-bit result (LittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="029c2-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="029c2-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="029c2-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="029c2-112">Remarks</span></span>

<span data-ttu-id="029c2-113">Использует стандартный подход Shift и-Add для расчета квадрата.</span><span class="sxs-lookup"><span data-stu-id="029c2-113">Uses a standard shift-and-add approach to compute the square.</span></span> <span data-ttu-id="029c2-114">Сохраняет $n-$1 Кубитс по сравнению с прямым решением, которое сначала копирует XS перед применением обычного множителя, а затем отменяет операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="029c2-114">Saves $n-1$ qubits compared to the straight-forward solution which first copies out xs before applying a regular multiplier and then undoing the copy operation.</span></span>