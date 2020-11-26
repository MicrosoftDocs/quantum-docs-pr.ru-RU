---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLEA
title: Функция Реверседоплеа
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLEA
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: 71b6b87a44f541e5379d8de8a3562febbfa49e1d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222173"
---
# <a name="reversedoplea-function"></a><span data-ttu-id="ce274-102">Функция Реверседоплеа</span><span class="sxs-lookup"><span data-stu-id="ce274-102">ReversedOpLEA function</span></span>

<span data-ttu-id="ce274-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="ce274-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="ce274-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ce274-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ce274-105">При наличии операции, которая принимает прямой ввод с обратным порядком байтов, возвращает новую операцию, принимающую входные данные с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="ce274-105">Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.</span></span>

```qsharp
function ReversedOpLEA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="ce274-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ce274-106">Input</span></span>

### <a name="op--littleendian--unit--is-adj"></a><span data-ttu-id="ce274-107">Op: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  — это прогода</span><span class="sxs-lookup"><span data-stu-id="ce274-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="ce274-108">Операция, входные данные которой должны быть отменены.</span><span class="sxs-lookup"><span data-stu-id="ce274-108">The operation whose input is to be reversed.</span></span>



## <a name="output--bigendian--unit--is-adj"></a><span data-ttu-id="ce274-109">Выходные данные: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [единица](xref:microsoft.quantum.lang-ref.unit)  — это прогода</span><span class="sxs-lookup"><span data-stu-id="ce274-109">Output : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="ce274-110">Новая операция, принимающая свои входные данные в виде регистра с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="ce274-110">A new operation that accepts its input as a big-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce274-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="ce274-111">See Also</span></span>

- [<span data-ttu-id="ce274-112">Microsoft. тактов. арифметик. Апплиреверседоплеа</span><span class="sxs-lookup"><span data-stu-id="ce274-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA)
- [<span data-ttu-id="ce274-113">Microsoft. тактов. арифметик. Реверседопле</span><span class="sxs-lookup"><span data-stu-id="ce274-113">Microsoft.Quantum.Arithmetic.ReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLE)
- [<span data-ttu-id="ce274-114">Microsoft. тактов. арифметик. Реверседоплек</span><span class="sxs-lookup"><span data-stu-id="ce274-114">Microsoft.Quantum.Arithmetic.ReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEC)
- [<span data-ttu-id="ce274-115">Microsoft. тактов. арифметик. Реверседоплека</span><span class="sxs-lookup"><span data-stu-id="ce274-115">Microsoft.Quantum.Arithmetic.ReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLECA)