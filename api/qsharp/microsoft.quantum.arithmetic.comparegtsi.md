---
uid: Microsoft.Quantum.Arithmetic.CompareGTSI
title: Операция Компарегтси
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGTSI
qsharp.summary: 'Wrapper for signed integer comparison: `result = xs > ys`.'
ms.openlocfilehash: 735ae21168d8efb3e626a8f1ea36e97f5cdf8760
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731624"
---
# <a name="comparegtsi-operation"></a><span data-ttu-id="aeeeb-102">Операция Компарегтси</span><span class="sxs-lookup"><span data-stu-id="aeeeb-102">CompareGTSI operation</span></span>

<span data-ttu-id="aeeeb-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="aeeeb-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="aeeeb-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="aeeeb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="aeeeb-105">Оболочка для сравнения целых чисел со знаком: `result = xs > ys` .</span><span class="sxs-lookup"><span data-stu-id="aeeeb-105">Wrapper for signed integer comparison: `result = xs > ys`.</span></span>

```qsharp
operation CompareGTSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, ys : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="aeeeb-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="aeeeb-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="aeeeb-107">xs: [сигнедлиттлиндиан](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="aeeeb-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="aeeeb-108">Первое $n $-разрядное число</span><span class="sxs-lookup"><span data-stu-id="aeeeb-108">First $n$-bit number</span></span>


### <a name="ys--signedlittleendian"></a><span data-ttu-id="aeeeb-109">ИС: [сигнедлиттлиндиан](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="aeeeb-109">ys : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="aeeeb-110">Второе $n $-разрядное число</span><span class="sxs-lookup"><span data-stu-id="aeeeb-110">Second $n$-bit number</span></span>


### <a name="result--qubit"></a><span data-ttu-id="aeeeb-111">результат: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="aeeeb-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="aeeeb-112">Будет отражено, если $xs > ИС $</span><span class="sxs-lookup"><span data-stu-id="aeeeb-112">Will be flipped if $xs > ys$</span></span>



## <a name="output--unit"></a><span data-ttu-id="aeeeb-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="aeeeb-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

