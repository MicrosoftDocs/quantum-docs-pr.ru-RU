---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC
title: Операция Апплиреверседоплек
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpLEC
qsharp.summary: Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.
ms.openlocfilehash: ac9a6000140445a457a9abc46d5143dcb089883e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731736"
---
# <a name="applyreversedoplec-operation"></a><span data-ttu-id="9baae-102">Операция Апплиреверседоплек</span><span class="sxs-lookup"><span data-stu-id="9baae-102">ApplyReversedOpLEC operation</span></span>

<span data-ttu-id="9baae-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="9baae-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="9baae-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9baae-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9baae-105">Применяет операцию, принимающую обратный ввод с прямым порядком байтов в кодировку для кодирования целого числа без знака с использованием формата с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="9baae-105">Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.</span></span>

```qsharp
operation ApplyReversedOpLEC (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl), register : Microsoft.Quantum.Arithmetic.BigEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="9baae-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9baae-106">Input</span></span>

### <a name="op--littleendian--unit-ctl"></a><span data-ttu-id="9baae-107">Op: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="9baae-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="9baae-108">Операция, которая работает с регистром с прямым порядком следования.</span><span class="sxs-lookup"><span data-stu-id="9baae-108">Operation that acts on a little-endian register.</span></span>


### <a name="register--bigendian"></a><span data-ttu-id="9baae-109">Регистрация: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="9baae-109">register : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="9baae-110">Регистр с обратным порядком байтов для преобразования.</span><span class="sxs-lookup"><span data-stu-id="9baae-110">A big-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9baae-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9baae-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="9baae-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="9baae-112">See Also</span></span>

- [<span data-ttu-id="9baae-113">Microsoft. тактов. арифметик. Апплиреверседопле</span><span class="sxs-lookup"><span data-stu-id="9baae-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLE)
- [<span data-ttu-id="9baae-114">Microsoft. тактов. арифметик. Апплиреверседоплеа</span><span class="sxs-lookup"><span data-stu-id="9baae-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA)
- [<span data-ttu-id="9baae-115">Microsoft. тактов. арифметик. Апплиреверседоплека</span><span class="sxs-lookup"><span data-stu-id="9baae-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)