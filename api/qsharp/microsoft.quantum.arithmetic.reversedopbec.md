---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBEC
title: Функция Реверседопбек
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBEC
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 5bafe71b665eda082eafbe06be1308d6b042db2c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222275"
---
# <a name="reversedopbec-function"></a><span data-ttu-id="bfc50-102">Функция Реверседопбек</span><span class="sxs-lookup"><span data-stu-id="bfc50-102">ReversedOpBEC function</span></span>

<span data-ttu-id="bfc50-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="bfc50-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="bfc50-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bfc50-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bfc50-105">При выполнении операции, которая принимает входные данные с обратным порядком байтов, возвращает новую операцию, которая принимает прямой порядок байтов.</span><span class="sxs-lookup"><span data-stu-id="bfc50-105">Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.</span></span>

```qsharp
function ReversedOpBEC (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="bfc50-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bfc50-106">Input</span></span>

### <a name="op--bigendian--unit--is-ctl"></a><span data-ttu-id="bfc50-107">Op: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  — CTL</span><span class="sxs-lookup"><span data-stu-id="bfc50-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="bfc50-108">Операция, входные данные которой должны быть отменены.</span><span class="sxs-lookup"><span data-stu-id="bfc50-108">The operation whose input is to be reversed.</span></span>



## <a name="output--littleendian--unit--is-ctl"></a><span data-ttu-id="bfc50-109">Выходные данные: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  — CTL</span><span class="sxs-lookup"><span data-stu-id="bfc50-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="bfc50-110">Новая операция, принимающая свои входные данные в виде регистра с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="bfc50-110">A new operation that accepts its input as a little-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="bfc50-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="bfc50-111">See Also</span></span>

- [<span data-ttu-id="bfc50-112">Microsoft. тактов. арифметик. Апплиреверседопбек</span><span class="sxs-lookup"><span data-stu-id="bfc50-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC)
- [<span data-ttu-id="bfc50-113">Microsoft. тактов. арифметик. Реверседопбе</span><span class="sxs-lookup"><span data-stu-id="bfc50-113">Microsoft.Quantum.Arithmetic.ReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBE)
- [<span data-ttu-id="bfc50-114">Microsoft. тактов. арифметик. Реверседопбеа</span><span class="sxs-lookup"><span data-stu-id="bfc50-114">Microsoft.Quantum.Arithmetic.ReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [<span data-ttu-id="bfc50-115">Microsoft. тактов. арифметик. Реверседопбека</span><span class="sxs-lookup"><span data-stu-id="bfc50-115">Microsoft.Quantum.Arithmetic.ReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)