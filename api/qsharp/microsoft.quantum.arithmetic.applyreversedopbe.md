---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpBE
title: Операция Апплиреверседопбе
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpBE
qsharp.summary: Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.
ms.openlocfilehash: bf2d43d4e870150f8e6d51dc2f5fb37bdf01d6ec
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843614"
---
# <a name="applyreversedopbe-operation"></a><span data-ttu-id="1e5b0-102">Операция Апплиреверседопбе</span><span class="sxs-lookup"><span data-stu-id="1e5b0-102">ApplyReversedOpBE operation</span></span>

<span data-ttu-id="1e5b0-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="1e5b0-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="1e5b0-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1e5b0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1e5b0-105">Применяет операцию, которая принимает входные данные с обратным порядком байтов в кодировку для кодирования целого числа без знака, используя формат с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="1e5b0-105">Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.</span></span>

```qsharp
operation ApplyReversedOpBE (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="1e5b0-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="1e5b0-106">Input</span></span>

### <a name="op--bigendian--unit"></a><span data-ttu-id="1e5b0-107">Op: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1e5b0-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="1e5b0-108">Операция, которая работает с регистром с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="1e5b0-108">Operation that acts on a big-endian register.</span></span>


### <a name="register--littleendian"></a><span data-ttu-id="1e5b0-109">Регистрация: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="1e5b0-109">register : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="1e5b0-110">Регистр с прямым порядком байтов для преобразования.</span><span class="sxs-lookup"><span data-stu-id="1e5b0-110">A little-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1e5b0-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1e5b0-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="1e5b0-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="1e5b0-112">See Also</span></span>

- [<span data-ttu-id="1e5b0-113">Microsoft. тактов. арифметик. Апплиреверседопбеа</span><span class="sxs-lookup"><span data-stu-id="1e5b0-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA)
- [<span data-ttu-id="1e5b0-114">Microsoft. тактов. арифметик. Апплиреверседопбек</span><span class="sxs-lookup"><span data-stu-id="1e5b0-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC)
- [<span data-ttu-id="1e5b0-115">Microsoft. тактов. арифметик. Апплиреверседопбека</span><span class="sxs-lookup"><span data-stu-id="1e5b0-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA)