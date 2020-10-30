---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA
title: Операция Апплиреверседопбека
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpBECA
qsharp.summary: Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.
ms.openlocfilehash: 1a11b85e4eca627246d7b9d3b4c10824296e9a77
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731752"
---
# <a name="applyreversedopbeca-operation"></a><span data-ttu-id="c3452-102">Операция Апплиреверседопбека</span><span class="sxs-lookup"><span data-stu-id="c3452-102">ApplyReversedOpBECA operation</span></span>

<span data-ttu-id="c3452-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="c3452-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="c3452-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c3452-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c3452-105">Применяет операцию, которая принимает входные данные с обратным порядком байтов в кодировку для кодирования целого числа без знака, используя формат с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="c3452-105">Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.</span></span>

```qsharp
operation ApplyReversedOpBECA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl + Adj), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="c3452-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c3452-106">Input</span></span>

### <a name="op--bigendian--unit-ctl--adj"></a><span data-ttu-id="c3452-107">Op: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + прилагательные</span><span class="sxs-lookup"><span data-stu-id="c3452-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="c3452-108">Операция, которая работает с регистром с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="c3452-108">Operation that acts on a big-endian register.</span></span>


### <a name="register--littleendian"></a><span data-ttu-id="c3452-109">Регистрация: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="c3452-109">register : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="c3452-110">Регистр с прямым порядком байтов для преобразования.</span><span class="sxs-lookup"><span data-stu-id="c3452-110">A little-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c3452-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c3452-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="c3452-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="c3452-112">See Also</span></span>

- [<span data-ttu-id="c3452-113">Microsoft. тактов. арифметик. Апплиреверседопбе</span><span class="sxs-lookup"><span data-stu-id="c3452-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [<span data-ttu-id="c3452-114">Microsoft. тактов. арифметик. Апплиреверседопбеа</span><span class="sxs-lookup"><span data-stu-id="c3452-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA)
- [<span data-ttu-id="c3452-115">Microsoft. тактов. арифметик. Апплиреверседопбек</span><span class="sxs-lookup"><span data-stu-id="c3452-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC)