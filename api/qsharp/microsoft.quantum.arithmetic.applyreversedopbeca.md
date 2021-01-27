---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA
title: Операция Апплиреверседопбека
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpBECA
qsharp.summary: Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.
ms.openlocfilehash: 71e99d3390a2e510fd7ed28f3f6d8ed43b3ca7e6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843582"
---
# <a name="applyreversedopbeca-operation"></a><span data-ttu-id="12598-102">Операция Апплиреверседопбека</span><span class="sxs-lookup"><span data-stu-id="12598-102">ApplyReversedOpBECA operation</span></span>

<span data-ttu-id="12598-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="12598-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="12598-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="12598-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="12598-105">Применяет операцию, которая принимает входные данные с обратным порядком байтов в кодировку для кодирования целого числа без знака, используя формат с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="12598-105">Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.</span></span>

```qsharp
operation ApplyReversedOpBECA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl + Adj), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="12598-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="12598-106">Input</span></span>

### <a name="op--bigendian--unit--is-adj--ctl"></a><span data-ttu-id="12598-107">Op: [](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [единица](xref:microsoft.quantum.lang-ref.unit) байтов — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="12598-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="12598-108">Операция, которая работает с регистром с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="12598-108">Operation that acts on a big-endian register.</span></span>


### <a name="register--littleendian"></a><span data-ttu-id="12598-109">Регистрация: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="12598-109">register : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="12598-110">Регистр с прямым порядком байтов для преобразования.</span><span class="sxs-lookup"><span data-stu-id="12598-110">A little-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="12598-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="12598-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="12598-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="12598-112">See Also</span></span>

- [<span data-ttu-id="12598-113">Microsoft. тактов. арифметик. Апплиреверседопбе</span><span class="sxs-lookup"><span data-stu-id="12598-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [<span data-ttu-id="12598-114">Microsoft. тактов. арифметик. Апплиреверседопбеа</span><span class="sxs-lookup"><span data-stu-id="12598-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA)
- [<span data-ttu-id="12598-115">Microsoft. тактов. арифметик. Апплиреверседопбек</span><span class="sxs-lookup"><span data-stu-id="12598-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC)