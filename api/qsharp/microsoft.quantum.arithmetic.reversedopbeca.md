---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBECA
title: Функция Реверседопбека
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBECA
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: da21b09110400ad4ee862f662d45e166a49e7bd8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222207"
---
# <a name="reversedopbeca-function"></a><span data-ttu-id="5c249-102">Функция Реверседопбека</span><span class="sxs-lookup"><span data-stu-id="5c249-102">ReversedOpBECA function</span></span>

<span data-ttu-id="5c249-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="5c249-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="5c249-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5c249-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5c249-105">При выполнении операции, которая принимает входные данные с обратным порядком байтов, возвращает новую операцию, которая принимает прямой порядок байтов.</span><span class="sxs-lookup"><span data-stu-id="5c249-105">Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.</span></span>

```qsharp
function ReversedOpBECA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj + Ctl)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="5c249-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5c249-106">Input</span></span>

### <a name="op--bigendian--unit--is-adj--ctl"></a><span data-ttu-id="5c249-107">Op: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [единица](xref:microsoft.quantum.lang-ref.unit) байтов — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="5c249-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="5c249-108">Операция, входные данные которой должны быть отменены.</span><span class="sxs-lookup"><span data-stu-id="5c249-108">The operation whose input is to be reversed.</span></span>



## <a name="output--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="5c249-109">Выходные данные [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) : => [единица](xref:microsoft.quantum.lang-ref.unit) литтлиндиан — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="5c249-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="5c249-110">Новая операция, принимающая свои входные данные в виде регистра с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="5c249-110">A new operation that accepts its input as a little-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="5c249-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="5c249-111">See Also</span></span>

- [<span data-ttu-id="5c249-112">Microsoft. тактов. арифметик. Апплиреверседопбека</span><span class="sxs-lookup"><span data-stu-id="5c249-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA)
- [<span data-ttu-id="5c249-113">Microsoft. тактов. арифметик. Реверседопбе</span><span class="sxs-lookup"><span data-stu-id="5c249-113">Microsoft.Quantum.Arithmetic.ReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBE)
- [<span data-ttu-id="5c249-114">Microsoft. тактов. арифметик. Реверседопбеа</span><span class="sxs-lookup"><span data-stu-id="5c249-114">Microsoft.Quantum.Arithmetic.ReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [<span data-ttu-id="5c249-115">Microsoft. тактов. арифметик. Реверседопбек</span><span class="sxs-lookup"><span data-stu-id="5c249-115">Microsoft.Quantum.Arithmetic.ReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEC)