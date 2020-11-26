---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBEA
title: Функция Реверседопбеа
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBEA
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 69fd4401e6862a3a6afaa51fb5b8a3592768bb42
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222309"
---
# <a name="reversedopbea-function"></a><span data-ttu-id="7518d-102">Функция Реверседопбеа</span><span class="sxs-lookup"><span data-stu-id="7518d-102">ReversedOpBEA function</span></span>

<span data-ttu-id="7518d-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="7518d-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="7518d-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7518d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7518d-105">При выполнении операции, которая принимает входные данные с обратным порядком байтов, возвращает новую операцию, которая принимает прямой порядок байтов.</span><span class="sxs-lookup"><span data-stu-id="7518d-105">Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.</span></span>

```qsharp
function ReversedOpBEA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="7518d-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7518d-106">Input</span></span>

### <a name="op--bigendian--unit--is-adj"></a><span data-ttu-id="7518d-107">Op: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  — это прогода</span><span class="sxs-lookup"><span data-stu-id="7518d-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="7518d-108">Операция, входные данные которой должны быть отменены.</span><span class="sxs-lookup"><span data-stu-id="7518d-108">The operation whose input is to be reversed.</span></span>



## <a name="output--littleendian--unit--is-adj"></a><span data-ttu-id="7518d-109">Выходные данные: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [единица](xref:microsoft.quantum.lang-ref.unit)  — это прогода</span><span class="sxs-lookup"><span data-stu-id="7518d-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="7518d-110">Новая операция, принимающая свои входные данные в виде регистра с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="7518d-110">A new operation that accepts its input as a little-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="7518d-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="7518d-111">See Also</span></span>

- [<span data-ttu-id="7518d-112">Microsoft. тактов. арифметик. Апплиреверседопбеа</span><span class="sxs-lookup"><span data-stu-id="7518d-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA)
- [<span data-ttu-id="7518d-113">Microsoft. тактов. арифметик. Реверседопбе</span><span class="sxs-lookup"><span data-stu-id="7518d-113">Microsoft.Quantum.Arithmetic.ReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBE)
- [<span data-ttu-id="7518d-114">Microsoft. тактов. арифметик. Реверседопбек</span><span class="sxs-lookup"><span data-stu-id="7518d-114">Microsoft.Quantum.Arithmetic.ReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEC)
- [<span data-ttu-id="7518d-115">Microsoft. тактов. арифметик. Реверседопбека</span><span class="sxs-lookup"><span data-stu-id="7518d-115">Microsoft.Quantum.Arithmetic.ReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)