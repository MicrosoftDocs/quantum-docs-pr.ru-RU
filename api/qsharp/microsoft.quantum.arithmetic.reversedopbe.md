---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBE
title: Функция Реверседопбе
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBE
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 878b0fae8a803b3136d1537309c945c052e1052c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846484"
---
# <a name="reversedopbe-function"></a><span data-ttu-id="efbb7-102">Функция Реверседопбе</span><span class="sxs-lookup"><span data-stu-id="efbb7-102">ReversedOpBE function</span></span>

<span data-ttu-id="efbb7-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="efbb7-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="efbb7-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="efbb7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="efbb7-105">При выполнении операции, которая принимает входные данные с обратным порядком байтов, возвращает новую операцию, которая принимает прямой порядок байтов.</span><span class="sxs-lookup"><span data-stu-id="efbb7-105">Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.</span></span>

```qsharp
function ReversedOpBE (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit)
```


## <a name="input"></a><span data-ttu-id="efbb7-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="efbb7-106">Input</span></span>

### <a name="op--bigendian--unit"></a><span data-ttu-id="efbb7-107">Op: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="efbb7-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="efbb7-108">Операция, входные данные которой должны быть отменены.</span><span class="sxs-lookup"><span data-stu-id="efbb7-108">The operation whose input is to be reversed.</span></span>



## <a name="output--littleendian--unit"></a><span data-ttu-id="efbb7-109">Выходные данные [](xref:Microsoft.Quantum.Arithmetic.LittleEndian) : => [единица](xref:microsoft.quantum.lang-ref.unit) литтлиндиан</span><span class="sxs-lookup"><span data-stu-id="efbb7-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="efbb7-110">Новая операция, принимающая свои входные данные в виде регистра с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="efbb7-110">A new operation that accepts its input as a little-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="efbb7-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="efbb7-111">See Also</span></span>

- [<span data-ttu-id="efbb7-112">Microsoft. тактов. арифметик. Апплиреверседопбе</span><span class="sxs-lookup"><span data-stu-id="efbb7-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [<span data-ttu-id="efbb7-113">Microsoft. тактов. арифметик. Реверседопбеа</span><span class="sxs-lookup"><span data-stu-id="efbb7-113">Microsoft.Quantum.Arithmetic.ReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [<span data-ttu-id="efbb7-114">Microsoft. тактов. арифметик. Реверседопбек</span><span class="sxs-lookup"><span data-stu-id="efbb7-114">Microsoft.Quantum.Arithmetic.ReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEC)
- [<span data-ttu-id="efbb7-115">Microsoft. тактов. арифметик. Реверседопбека</span><span class="sxs-lookup"><span data-stu-id="efbb7-115">Microsoft.Quantum.Arithmetic.ReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)