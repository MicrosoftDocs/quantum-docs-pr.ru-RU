---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLEC
title: Функция Реверседоплек
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLEC
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: 8c91391691b23786df02ae2a35264b578dccad41
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222088"
---
# <a name="reversedoplec-function"></a><span data-ttu-id="a0ca2-102">Функция Реверседоплек</span><span class="sxs-lookup"><span data-stu-id="a0ca2-102">ReversedOpLEC function</span></span>

<span data-ttu-id="a0ca2-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="a0ca2-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="a0ca2-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a0ca2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a0ca2-105">При наличии операции, которая принимает прямой ввод с обратным порядком байтов, возвращает новую операцию, принимающую входные данные с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-105">Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.</span></span>

```qsharp
function ReversedOpLEC (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="a0ca2-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a0ca2-106">Input</span></span>

### <a name="op--littleendian--unit--is-ctl"></a><span data-ttu-id="a0ca2-107">Op: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  — CTL</span><span class="sxs-lookup"><span data-stu-id="a0ca2-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="a0ca2-108">Операция, входные данные которой должны быть отменены.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-108">The operation whose input is to be reversed.</span></span>



## <a name="output--bigendian--unit--is-ctl"></a><span data-ttu-id="a0ca2-109">Выходные данные: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  — CTL</span><span class="sxs-lookup"><span data-stu-id="a0ca2-109">Output : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="a0ca2-110">Новая операция, принимающая свои входные данные в виде регистра с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-110">A new operation that accepts its input as a big-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="a0ca2-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="a0ca2-111">See Also</span></span>

- [<span data-ttu-id="a0ca2-112">Microsoft. тактов. арифметик. Апплиреверседоплек</span><span class="sxs-lookup"><span data-stu-id="a0ca2-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC)
- [<span data-ttu-id="a0ca2-113">Microsoft. тактов. арифметик. Реверседопле</span><span class="sxs-lookup"><span data-stu-id="a0ca2-113">Microsoft.Quantum.Arithmetic.ReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLE)
- [<span data-ttu-id="a0ca2-114">Microsoft. тактов. арифметик. Реверседоплеа</span><span class="sxs-lookup"><span data-stu-id="a0ca2-114">Microsoft.Quantum.Arithmetic.ReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEA)
- [<span data-ttu-id="a0ca2-115">Microsoft. тактов. арифметик. Реверседоплека</span><span class="sxs-lookup"><span data-stu-id="a0ca2-115">Microsoft.Quantum.Arithmetic.ReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLECA)