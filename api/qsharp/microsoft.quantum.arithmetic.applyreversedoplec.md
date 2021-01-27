---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC
title: Операция Апплиреверседоплек
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpLEC
qsharp.summary: Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.
ms.openlocfilehash: 74ecc705a6e3d1d59c4c4ae71d30171c12fa45ae
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843501"
---
# <a name="applyreversedoplec-operation"></a><span data-ttu-id="2e100-102">Операция Апплиреверседоплек</span><span class="sxs-lookup"><span data-stu-id="2e100-102">ApplyReversedOpLEC operation</span></span>

<span data-ttu-id="2e100-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="2e100-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="2e100-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2e100-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2e100-105">Применяет операцию, принимающую обратный ввод с прямым порядком байтов в кодировку для кодирования целого числа без знака с использованием формата с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="2e100-105">Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.</span></span>

```qsharp
operation ApplyReversedOpLEC (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl), register : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="2e100-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2e100-106">Input</span></span>

### <a name="op--littleendian--unit--is-ctl"></a><span data-ttu-id="2e100-107">Op: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  — CTL</span><span class="sxs-lookup"><span data-stu-id="2e100-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="2e100-108">Операция, которая работает с регистром с прямым порядком следования.</span><span class="sxs-lookup"><span data-stu-id="2e100-108">Operation that acts on a little-endian register.</span></span>


### <a name="register--bigendian"></a><span data-ttu-id="2e100-109">Регистрация: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="2e100-109">register : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="2e100-110">Регистр с обратным порядком байтов для преобразования.</span><span class="sxs-lookup"><span data-stu-id="2e100-110">A big-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2e100-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2e100-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="2e100-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="2e100-112">See Also</span></span>

- [<span data-ttu-id="2e100-113">Microsoft. тактов. арифметик. Апплиреверседопле</span><span class="sxs-lookup"><span data-stu-id="2e100-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLE)
- [<span data-ttu-id="2e100-114">Microsoft. тактов. арифметик. Апплиреверседоплеа</span><span class="sxs-lookup"><span data-stu-id="2e100-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA)
- [<span data-ttu-id="2e100-115">Microsoft. тактов. арифметик. Апплиреверседоплека</span><span class="sxs-lookup"><span data-stu-id="2e100-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)