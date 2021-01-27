---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA
title: Операция Апплиреверседоплеа
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpLEA
qsharp.summary: Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.
ms.openlocfilehash: 572841410f16085256fdee9302038cd347476dd9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843529"
---
# <a name="applyreversedoplea-operation"></a><span data-ttu-id="af228-102">Операция Апплиреверседоплеа</span><span class="sxs-lookup"><span data-stu-id="af228-102">ApplyReversedOpLEA operation</span></span>

<span data-ttu-id="af228-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="af228-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="af228-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="af228-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="af228-105">Применяет операцию, принимающую обратный ввод с прямым порядком байтов в кодировку для кодирования целого числа без знака с использованием формата с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="af228-105">Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.</span></span>

```qsharp
operation ApplyReversedOpLEA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj), register : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="af228-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="af228-106">Input</span></span>

### <a name="op--littleendian--unit--is-adj"></a><span data-ttu-id="af228-107">Op: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  — это прогода</span><span class="sxs-lookup"><span data-stu-id="af228-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="af228-108">Операция, которая работает с регистром с прямым порядком следования.</span><span class="sxs-lookup"><span data-stu-id="af228-108">Operation that acts on a little-endian register.</span></span>


### <a name="register--bigendian"></a><span data-ttu-id="af228-109">Регистрация: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="af228-109">register : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="af228-110">Регистр с обратным порядком байтов для преобразования.</span><span class="sxs-lookup"><span data-stu-id="af228-110">A big-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="af228-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="af228-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="af228-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="af228-112">See Also</span></span>

- [<span data-ttu-id="af228-113">Microsoft. тактов. арифметик. Апплиреверседопле</span><span class="sxs-lookup"><span data-stu-id="af228-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLE)
- [<span data-ttu-id="af228-114">Microsoft. тактов. арифметик. Апплиреверседоплек</span><span class="sxs-lookup"><span data-stu-id="af228-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC)
- [<span data-ttu-id="af228-115">Microsoft. тактов. арифметик. Апплиреверседоплека</span><span class="sxs-lookup"><span data-stu-id="af228-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)