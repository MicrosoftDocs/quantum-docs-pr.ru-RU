---
uid: Microsoft.Quantum.Arithmetic.CompareGTI
title: Операция Компарегти
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGTI
qsharp.summary: 'Wrapper for integer comparison: `result = x > y`.'
ms.openlocfilehash: e9c245fb7c0cf3a6b1b98eb01cd582c325917602
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843300"
---
# <a name="comparegti-operation"></a><span data-ttu-id="16350-102">Операция Компарегти</span><span class="sxs-lookup"><span data-stu-id="16350-102">CompareGTI operation</span></span>

<span data-ttu-id="16350-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="16350-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="16350-104">Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="16350-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="16350-105">Оболочка для сравнения целых чисел: `result = x > y` .</span><span class="sxs-lookup"><span data-stu-id="16350-105">Wrapper for integer comparison: `result = x > y`.</span></span>

```qsharp
operation CompareGTI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="16350-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="16350-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="16350-107">xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="16350-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="16350-108">Первое $n $-разрядное число</span><span class="sxs-lookup"><span data-stu-id="16350-108">First $n$-bit number</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="16350-109">ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="16350-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="16350-110">Второе $n $-разрядное число</span><span class="sxs-lookup"><span data-stu-id="16350-110">Second $n$-bit number</span></span>


### <a name="result--qubit"></a><span data-ttu-id="16350-111">результат: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="16350-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="16350-112">Будет отражено, если $x > y $</span><span class="sxs-lookup"><span data-stu-id="16350-112">Will be flipped if $x > y$</span></span>



## <a name="output--unit"></a><span data-ttu-id="16350-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="16350-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

