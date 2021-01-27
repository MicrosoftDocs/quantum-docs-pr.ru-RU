---
uid: Microsoft.Quantum.Arithmetic.CompareGTSI
title: Операция Компарегтси
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGTSI
qsharp.summary: 'Wrapper for signed integer comparison: `result = xs > ys`.'
ms.openlocfilehash: f725bdbaa945a4f87e90fc71930c37642113c21a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846697"
---
# <a name="comparegtsi-operation"></a><span data-ttu-id="b3710-102">Операция Компарегтси</span><span class="sxs-lookup"><span data-stu-id="b3710-102">CompareGTSI operation</span></span>

<span data-ttu-id="b3710-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="b3710-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="b3710-104">Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="b3710-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="b3710-105">Оболочка для сравнения целых чисел со знаком: `result = xs > ys` .</span><span class="sxs-lookup"><span data-stu-id="b3710-105">Wrapper for signed integer comparison: `result = xs > ys`.</span></span>

```qsharp
operation CompareGTSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, ys : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="b3710-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b3710-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="b3710-107">xs: [сигнедлиттлиндиан](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="b3710-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="b3710-108">Первое $n $-разрядное число</span><span class="sxs-lookup"><span data-stu-id="b3710-108">First $n$-bit number</span></span>


### <a name="ys--signedlittleendian"></a><span data-ttu-id="b3710-109">ИС: [сигнедлиттлиндиан](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="b3710-109">ys : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="b3710-110">Второе $n $-разрядное число</span><span class="sxs-lookup"><span data-stu-id="b3710-110">Second $n$-bit number</span></span>


### <a name="result--qubit"></a><span data-ttu-id="b3710-111">результат: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="b3710-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="b3710-112">Будет отражено, если $xs > ИС $</span><span class="sxs-lookup"><span data-stu-id="b3710-112">Will be flipped if $xs > ys$</span></span>



## <a name="output--unit"></a><span data-ttu-id="b3710-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b3710-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

