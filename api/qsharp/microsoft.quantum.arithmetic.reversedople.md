---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLE
title: Функция Реверседопле
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLE
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: 91b98663028b8a1d54c546e70d8bfe603d71d041
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222258"
---
# <a name="reversedople-function"></a><span data-ttu-id="b8986-102">Функция Реверседопле</span><span class="sxs-lookup"><span data-stu-id="b8986-102">ReversedOpLE function</span></span>

<span data-ttu-id="b8986-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="b8986-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="b8986-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b8986-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b8986-105">При наличии операции, которая принимает прямой ввод с обратным порядком байтов, возвращает новую операцию, принимающую входные данные с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="b8986-105">Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.</span></span>

```qsharp
function ReversedOpLE (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit)
```


## <a name="input"></a><span data-ttu-id="b8986-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b8986-106">Input</span></span>

### <a name="op--littleendian--unit"></a><span data-ttu-id="b8986-107">Op: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b8986-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="b8986-108">Операция, входные данные которой должны быть отменены.</span><span class="sxs-lookup"><span data-stu-id="b8986-108">The operation whose input is to be reversed.</span></span>



## <a name="output--bigendian--unit"></a><span data-ttu-id="b8986-109">Выходные данные [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) : => [единица](xref:microsoft.quantum.lang-ref.unit) байтов</span><span class="sxs-lookup"><span data-stu-id="b8986-109">Output : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="b8986-110">Новая операция, принимающая свои входные данные в виде регистра с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="b8986-110">A new operation that accepts its input as a big-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="b8986-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="b8986-111">See Also</span></span>

- [<span data-ttu-id="b8986-112">Microsoft. тактов. арифметик. Апплиреверседопле</span><span class="sxs-lookup"><span data-stu-id="b8986-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLE)
- [<span data-ttu-id="b8986-113">Microsoft. тактов. арифметик. Реверседоплеа</span><span class="sxs-lookup"><span data-stu-id="b8986-113">Microsoft.Quantum.Arithmetic.ReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEA)
- [<span data-ttu-id="b8986-114">Microsoft. тактов. арифметик. Реверседоплек</span><span class="sxs-lookup"><span data-stu-id="b8986-114">Microsoft.Quantum.Arithmetic.ReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEC)
- [<span data-ttu-id="b8986-115">Microsoft. тактов. арифметик. Реверседоплека</span><span class="sxs-lookup"><span data-stu-id="b8986-115">Microsoft.Quantum.Arithmetic.ReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLECA)