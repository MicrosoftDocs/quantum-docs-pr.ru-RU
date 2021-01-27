---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpLE
title: Операция Апплиреверседопле
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpLE
qsharp.summary: Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.
ms.openlocfilehash: 5f26a25afe5e3d52bae7f7c1b9c8146e5f8a747c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843549"
---
# <a name="applyreversedople-operation"></a><span data-ttu-id="8fed6-102">Операция Апплиреверседопле</span><span class="sxs-lookup"><span data-stu-id="8fed6-102">ApplyReversedOpLE operation</span></span>

<span data-ttu-id="8fed6-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="8fed6-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="8fed6-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8fed6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8fed6-105">Применяет операцию, принимающую обратный ввод с прямым порядком байтов в кодировку для кодирования целого числа без знака с использованием формата с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="8fed6-105">Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.</span></span>

```qsharp
operation ApplyReversedOpLE (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit), register : Microsoft.Quantum.Arithmetic.BigEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="8fed6-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8fed6-106">Input</span></span>

### <a name="op--littleendian--unit"></a><span data-ttu-id="8fed6-107">Op: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8fed6-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="8fed6-108">Операция, которая работает с регистром с прямым порядком следования.</span><span class="sxs-lookup"><span data-stu-id="8fed6-108">Operation that acts on a little-endian register.</span></span>


### <a name="register--bigendian"></a><span data-ttu-id="8fed6-109">Регистрация: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="8fed6-109">register : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="8fed6-110">Регистр с обратным порядком байтов для преобразования.</span><span class="sxs-lookup"><span data-stu-id="8fed6-110">A big-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8fed6-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8fed6-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="8fed6-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="8fed6-112">See Also</span></span>

- [<span data-ttu-id="8fed6-113">Microsoft. тактов. арифметик. Апплиреверседоплеа</span><span class="sxs-lookup"><span data-stu-id="8fed6-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA)
- [<span data-ttu-id="8fed6-114">Microsoft. тактов. арифметик. Апплиреверседоплек</span><span class="sxs-lookup"><span data-stu-id="8fed6-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC)
- [<span data-ttu-id="8fed6-115">Microsoft. тактов. арифметик. Апплиреверседоплека</span><span class="sxs-lookup"><span data-stu-id="8fed6-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)