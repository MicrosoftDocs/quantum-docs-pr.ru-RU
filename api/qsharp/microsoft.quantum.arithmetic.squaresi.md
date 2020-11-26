---
uid: Microsoft.Quantum.Arithmetic.SquareSI
title: Операция Скуареси
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareSI
qsharp.summary: Square signed integer `xs` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 7fe4d27b974a06b019a2b15710fbc51b598027b4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221833"
---
# <a name="squaresi-operation"></a><span data-ttu-id="ac4e7-102">Операция Скуареси</span><span class="sxs-lookup"><span data-stu-id="ac4e7-102">SquareSI operation</span></span>

<span data-ttu-id="ac4e7-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="ac4e7-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="ac4e7-104">Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="ac4e7-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="ac4e7-105">Квадратное целое число со знаком `xs` и сохранение результата в `result` , который должен быть равен нулю изначально.</span><span class="sxs-lookup"><span data-stu-id="ac4e7-105">Square signed integer `xs` and store the result in `result`, which must be zero initially.</span></span>

```qsharp
operation SquareSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Microsoft.Quantum.Arithmetic.SignedLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="ac4e7-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ac4e7-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="ac4e7-107">xs: [сигнедлиттлиндиан](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="ac4e7-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="ac4e7-108">n-разрядное целое число в квадрат (Сигнедлиттлиндиан)</span><span class="sxs-lookup"><span data-stu-id="ac4e7-108">n-bit integer to square (SignedLittleEndian)</span></span>


### <a name="result--signedlittleendian"></a><span data-ttu-id="ac4e7-109">результат: [сигнедлиттлиндиан](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="ac4e7-109">result : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="ac4e7-110">2N-разрядный результат (Сигнедлиттлиндиан) должен находиться в состоянии $ \кет {0} $ изначально.</span><span class="sxs-lookup"><span data-stu-id="ac4e7-110">2n-bit result (SignedLittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ac4e7-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ac4e7-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="ac4e7-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac4e7-112">Remarks</span></span>

<span data-ttu-id="ac4e7-113">Реализация основывается на Интежерскуаре.</span><span class="sxs-lookup"><span data-stu-id="ac4e7-113">The implementation relies on IntegerSquare.</span></span>