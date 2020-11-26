---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpLE
title: Операция Апплиреверседопле
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpLE
qsharp.summary: Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.
ms.openlocfilehash: 16ce6842cdef8e519a13a45640edc3d79cdbce25
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202759"
---
# <a name="applyreversedople-operation"></a><span data-ttu-id="66d9e-102">Операция Апплиреверседопле</span><span class="sxs-lookup"><span data-stu-id="66d9e-102">ApplyReversedOpLE operation</span></span>

<span data-ttu-id="66d9e-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="66d9e-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="66d9e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="66d9e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="66d9e-105">Применяет операцию, принимающую обратный ввод с прямым порядком байтов в кодировку для кодирования целого числа без знака с использованием формата с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="66d9e-105">Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.</span></span>

```qsharp
operation ApplyReversedOpLE (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit), register : Microsoft.Quantum.Arithmetic.BigEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="66d9e-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="66d9e-106">Input</span></span>

### <a name="op--littleendian--unit"></a><span data-ttu-id="66d9e-107">Op: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="66d9e-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="66d9e-108">Операция, которая работает с регистром с прямым порядком следования.</span><span class="sxs-lookup"><span data-stu-id="66d9e-108">Operation that acts on a little-endian register.</span></span>


### <a name="register--bigendian"></a><span data-ttu-id="66d9e-109">Регистрация: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="66d9e-109">register : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="66d9e-110">Регистр с обратным порядком байтов для преобразования.</span><span class="sxs-lookup"><span data-stu-id="66d9e-110">A big-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="66d9e-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="66d9e-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="66d9e-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="66d9e-112">See Also</span></span>

- [<span data-ttu-id="66d9e-113">Microsoft. тактов. арифметик. Апплиреверседоплеа</span><span class="sxs-lookup"><span data-stu-id="66d9e-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA)
- [<span data-ttu-id="66d9e-114">Microsoft. тактов. арифметик. Апплиреверседоплек</span><span class="sxs-lookup"><span data-stu-id="66d9e-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC)
- [<span data-ttu-id="66d9e-115">Microsoft. тактов. арифметик. Апплиреверседоплека</span><span class="sxs-lookup"><span data-stu-id="66d9e-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)