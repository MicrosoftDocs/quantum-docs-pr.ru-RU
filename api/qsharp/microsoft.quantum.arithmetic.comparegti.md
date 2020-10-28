---
uid: Microsoft.Quantum.Arithmetic.CompareGTI
title: Операция Компарегти
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGTI
qsharp.summary: 'Wrapper for integer comparison: `result = x > y`.'
ms.openlocfilehash: c60c2827060f4ef223ebaf80ccdef09faaf56098
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731625"
---
# <a name="comparegti-operation"></a><span data-ttu-id="d49f1-102">Операция Компарегти</span><span class="sxs-lookup"><span data-stu-id="d49f1-102">CompareGTI operation</span></span>

<span data-ttu-id="d49f1-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="d49f1-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="d49f1-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d49f1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d49f1-105">Оболочка для сравнения целых чисел: `result = x > y` .</span><span class="sxs-lookup"><span data-stu-id="d49f1-105">Wrapper for integer comparison: `result = x > y`.</span></span>

```qsharp
operation CompareGTI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="d49f1-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d49f1-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="d49f1-107">xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="d49f1-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="d49f1-108">Первое $n $-разрядное число</span><span class="sxs-lookup"><span data-stu-id="d49f1-108">First $n$-bit number</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="d49f1-109">ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="d49f1-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="d49f1-110">Второе $n $-разрядное число</span><span class="sxs-lookup"><span data-stu-id="d49f1-110">Second $n$-bit number</span></span>


### <a name="result--qubit"></a><span data-ttu-id="d49f1-111">результат: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d49f1-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="d49f1-112">Будет отражено, если $x > y $</span><span class="sxs-lookup"><span data-stu-id="d49f1-112">Will be flipped if $x > y$</span></span>



## <a name="output--unit"></a><span data-ttu-id="d49f1-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d49f1-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

