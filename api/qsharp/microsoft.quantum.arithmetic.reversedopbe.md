---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBE
title: Функция Реверседопбе
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBE
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 3c39a90ed4b5df09b90d8b5020d8b824285b50eb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222326"
---
# <a name="reversedopbe-function"></a><span data-ttu-id="e90bb-102">Функция Реверседопбе</span><span class="sxs-lookup"><span data-stu-id="e90bb-102">ReversedOpBE function</span></span>

<span data-ttu-id="e90bb-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="e90bb-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="e90bb-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e90bb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e90bb-105">При выполнении операции, которая принимает входные данные с обратным порядком байтов, возвращает новую операцию, которая принимает прямой порядок байтов.</span><span class="sxs-lookup"><span data-stu-id="e90bb-105">Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.</span></span>

```qsharp
function ReversedOpBE (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit)
```


## <a name="input"></a><span data-ttu-id="e90bb-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e90bb-106">Input</span></span>

### <a name="op--bigendian--unit"></a><span data-ttu-id="e90bb-107">Op: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e90bb-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="e90bb-108">Операция, входные данные которой должны быть отменены.</span><span class="sxs-lookup"><span data-stu-id="e90bb-108">The operation whose input is to be reversed.</span></span>



## <a name="output--littleendian--unit"></a><span data-ttu-id="e90bb-109">Выходные данные [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) : => [единица](xref:microsoft.quantum.lang-ref.unit) литтлиндиан</span><span class="sxs-lookup"><span data-stu-id="e90bb-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="e90bb-110">Новая операция, принимающая свои входные данные в виде регистра с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="e90bb-110">A new operation that accepts its input as a little-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="e90bb-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="e90bb-111">See Also</span></span>

- [<span data-ttu-id="e90bb-112">Microsoft. тактов. арифметик. Апплиреверседопбе</span><span class="sxs-lookup"><span data-stu-id="e90bb-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [<span data-ttu-id="e90bb-113">Microsoft. тактов. арифметик. Реверседопбеа</span><span class="sxs-lookup"><span data-stu-id="e90bb-113">Microsoft.Quantum.Arithmetic.ReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [<span data-ttu-id="e90bb-114">Microsoft. тактов. арифметик. Реверседопбек</span><span class="sxs-lookup"><span data-stu-id="e90bb-114">Microsoft.Quantum.Arithmetic.ReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEC)
- [<span data-ttu-id="e90bb-115">Microsoft. тактов. арифметик. Реверседопбека</span><span class="sxs-lookup"><span data-stu-id="e90bb-115">Microsoft.Quantum.Arithmetic.ReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)