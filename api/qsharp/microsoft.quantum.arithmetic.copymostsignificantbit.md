---
uid: Microsoft.Quantum.Arithmetic.CopyMostSignificantBit
title: Операция Копимостсигнификантбит
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CopyMostSignificantBit
qsharp.summary: Copies the most significant bit of a qubit register `from` representing an unsigned integer into the qubit `target`.
ms.openlocfilehash: 609e937a03bebf45aa9398225bd1b7e2b717807a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843269"
---
# <a name="copymostsignificantbit-operation"></a><span data-ttu-id="8c39e-102">Операция Копимостсигнификантбит</span><span class="sxs-lookup"><span data-stu-id="8c39e-102">CopyMostSignificantBit operation</span></span>

<span data-ttu-id="8c39e-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="8c39e-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="8c39e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8c39e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8c39e-105">Копирует наиболее значащий бит регистра кубит `from` , представляющий целое число без знака, в кубит `target` .</span><span class="sxs-lookup"><span data-stu-id="8c39e-105">Copies the most significant bit of a qubit register `from` representing an unsigned integer into the qubit `target`.</span></span>

```qsharp
operation CopyMostSignificantBit (from : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="8c39e-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8c39e-106">Input</span></span>

### <a name="from--littleendian"></a><span data-ttu-id="8c39e-107">с: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="8c39e-107">from : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="8c39e-108">Целое число без знака, из которого копируется наибольший бит.</span><span class="sxs-lookup"><span data-stu-id="8c39e-108">The unsigned integer from which the highest bit is copied from.</span></span>
<span data-ttu-id="8c39e-109">целое число кодируется в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="8c39e-109">the integer is encoded in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="8c39e-110">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="8c39e-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="8c39e-111">Кубит, в котором копируется наибольший бит.</span><span class="sxs-lookup"><span data-stu-id="8c39e-111">The qubit in which the highest bit is being copied.</span></span> <span data-ttu-id="8c39e-112">Битовая кодировка определяется на основе вычислений.</span><span class="sxs-lookup"><span data-stu-id="8c39e-112">The bit encoding is in computational basis.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8c39e-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8c39e-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="8c39e-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="8c39e-114">See Also</span></span>

- [<span data-ttu-id="8c39e-115">Microsoft. тактов. арифметик. Литтлиндиан</span><span class="sxs-lookup"><span data-stu-id="8c39e-115">Microsoft.Quantum.Arithmetic.LittleEndian</span></span>](xref:Microsoft.Quantum.Arithmetic.LittleEndian)