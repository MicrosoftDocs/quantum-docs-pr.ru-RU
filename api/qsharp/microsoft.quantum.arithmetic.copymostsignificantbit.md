---
uid: Microsoft.Quantum.Arithmetic.CopyMostSignificantBit
title: Операция Копимостсигнификантбит
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CopyMostSignificantBit
qsharp.summary: Copies the most significant bit of a qubit register `from` representing an unsigned integer into the qubit `target`.
ms.openlocfilehash: 39a2dc2fe33f46c2767def06a44cde07e2f01497
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223295"
---
# <a name="copymostsignificantbit-operation"></a><span data-ttu-id="04494-102">Операция Копимостсигнификантбит</span><span class="sxs-lookup"><span data-stu-id="04494-102">CopyMostSignificantBit operation</span></span>

<span data-ttu-id="04494-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="04494-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="04494-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="04494-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="04494-105">Копирует наиболее значащий бит регистра кубит `from` , представляющий целое число без знака, в кубит `target` .</span><span class="sxs-lookup"><span data-stu-id="04494-105">Copies the most significant bit of a qubit register `from` representing an unsigned integer into the qubit `target`.</span></span>

```qsharp
operation CopyMostSignificantBit (from : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="04494-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="04494-106">Input</span></span>

### <a name="from--littleendian"></a><span data-ttu-id="04494-107">с: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="04494-107">from : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="04494-108">Целое число без знака, из которого копируется наибольший бит.</span><span class="sxs-lookup"><span data-stu-id="04494-108">The unsigned integer from which the highest bit is copied from.</span></span>
<span data-ttu-id="04494-109">целое число кодируется в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="04494-109">the integer is encoded in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="04494-110">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="04494-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="04494-111">Кубит, в котором копируется наибольший бит.</span><span class="sxs-lookup"><span data-stu-id="04494-111">The qubit in which the highest bit is being copied.</span></span> <span data-ttu-id="04494-112">Битовая кодировка определяется на основе вычислений.</span><span class="sxs-lookup"><span data-stu-id="04494-112">The bit encoding is in computational basis.</span></span>



## <a name="output--unit"></a><span data-ttu-id="04494-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="04494-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="04494-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="04494-114">See Also</span></span>

- [<span data-ttu-id="04494-115">Microsoft. тактов. арифметик. Литтлиндиан</span><span class="sxs-lookup"><span data-stu-id="04494-115">Microsoft.Quantum.Arithmetic.LittleEndian</span></span>](xref:Microsoft.Quantum.Arithmetic.LittleEndian)