---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLECA
title: Функция Реверседоплека
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLECA
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: d4245437f2b71abb8bf1bbe4db43ae7d2ee23799
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845757"
---
# <a name="reversedopleca-function"></a><span data-ttu-id="4b189-102">Функция Реверседоплека</span><span class="sxs-lookup"><span data-stu-id="4b189-102">ReversedOpLECA function</span></span>

<span data-ttu-id="4b189-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="4b189-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="4b189-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4b189-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4b189-105">При наличии операции, которая принимает прямой ввод с обратным порядком байтов, возвращает новую операцию, принимающую входные данные с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="4b189-105">Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.</span></span>

```qsharp
function ReversedOpLECA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="4b189-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4b189-106">Input</span></span>

### <a name="op--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="4b189-107">Op: [](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [единица](xref:microsoft.quantum.lang-ref.unit) литтлиндиан — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="4b189-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="4b189-108">Операция, входные данные которой должны быть отменены.</span><span class="sxs-lookup"><span data-stu-id="4b189-108">The operation whose input is to be reversed.</span></span>



## <a name="output--bigendian--unit--is-adj--ctl"></a><span data-ttu-id="4b189-109">Выходные данные [](xref:Microsoft.Quantum.Arithmetic.BigEndian) : => [единица](xref:microsoft.quantum.lang-ref.unit) байтов — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="4b189-109">Output : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="4b189-110">Новая операция, принимающая свои входные данные в виде регистра с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="4b189-110">A new operation that accepts its input as a big-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="4b189-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="4b189-111">See Also</span></span>

- [<span data-ttu-id="4b189-112">Microsoft. тактов. арифметик. Апплиреверседоплека</span><span class="sxs-lookup"><span data-stu-id="4b189-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)
- [<span data-ttu-id="4b189-113">Microsoft. тактов. арифметик. Реверседопле</span><span class="sxs-lookup"><span data-stu-id="4b189-113">Microsoft.Quantum.Arithmetic.ReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLE)
- [<span data-ttu-id="4b189-114">Microsoft. тактов. арифметик. Реверседоплеа</span><span class="sxs-lookup"><span data-stu-id="4b189-114">Microsoft.Quantum.Arithmetic.ReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEA)
- [<span data-ttu-id="4b189-115">Microsoft. тактов. арифметик. Реверседоплек</span><span class="sxs-lookup"><span data-stu-id="4b189-115">Microsoft.Quantum.Arithmetic.ReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEC)