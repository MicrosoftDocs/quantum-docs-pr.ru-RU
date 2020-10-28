---
uid: Microsoft.Quantum.Arithmetic.CopyMostSignificantBit
title: Операция Копимостсигнификантбит
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CopyMostSignificantBit
qsharp.summary: Copies the most significant bit of a qubit register `from` representing an unsigned integer into the qubit `target`.
ms.openlocfilehash: 02119103fa7b5776f0e1681535115e0773a34c4c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731577"
---
# <a name="copymostsignificantbit-operation"></a><span data-ttu-id="f0334-102">Операция Копимостсигнификантбит</span><span class="sxs-lookup"><span data-stu-id="f0334-102">CopyMostSignificantBit operation</span></span>

<span data-ttu-id="f0334-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="f0334-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="f0334-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f0334-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f0334-105">Копирует наиболее значащий бит регистра кубит `from` , представляющий целое число без знака, в кубит `target` .</span><span class="sxs-lookup"><span data-stu-id="f0334-105">Copies the most significant bit of a qubit register `from` representing an unsigned integer into the qubit `target`.</span></span>

```qsharp
operation CopyMostSignificantBit (from : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="f0334-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f0334-106">Input</span></span>

### <a name="from--littleendian"></a><span data-ttu-id="f0334-107">с: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f0334-107">from : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="f0334-108">Целое число без знака, из которого копируется наибольший бит.</span><span class="sxs-lookup"><span data-stu-id="f0334-108">The unsigned integer from which the highest bit is copied from.</span></span>
<span data-ttu-id="f0334-109">целое число кодируется в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="f0334-109">the integer is encoded in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="f0334-110">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f0334-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f0334-111">Кубит, в котором копируется наибольший бит.</span><span class="sxs-lookup"><span data-stu-id="f0334-111">The qubit in which the highest bit is being copied.</span></span> <span data-ttu-id="f0334-112">Битовая кодировка определяется на основе вычислений.</span><span class="sxs-lookup"><span data-stu-id="f0334-112">The bit encoding is in computational basis.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f0334-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f0334-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="f0334-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="f0334-114">See Also</span></span>

- [<span data-ttu-id="f0334-115">Microsoft. тактов. арифметик. Литтлиндиан</span><span class="sxs-lookup"><span data-stu-id="f0334-115">Microsoft.Quantum.Arithmetic.LittleEndian</span></span>](xref:Microsoft.Quantum.Arithmetic.LittleEndian)