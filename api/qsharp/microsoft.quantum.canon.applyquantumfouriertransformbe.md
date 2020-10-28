---
uid: Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE
title: Операция Аппликуантумфауриертрансформбе
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyQuantumFourierTransformBE
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: d15310298dc138bdffb612895bbf20ca1371db6f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717791"
---
# <a name="applyquantumfouriertransformbe-operation"></a><span data-ttu-id="ce3e0-102">Операция Аппликуантумфауриертрансформбе</span><span class="sxs-lookup"><span data-stu-id="ce3e0-102">ApplyQuantumFourierTransformBE operation</span></span>

<span data-ttu-id="ce3e0-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ce3e0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ce3e0-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ce3e0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ce3e0-105">Выполняет преобразование Фурье в тактовую операцию для регистра такта, содержащего целое число в представлении с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="ce3e0-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.</span></span>

```qsharp
operation ApplyQuantumFourierTransformBE (qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="ce3e0-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ce3e0-106">Input</span></span>

### <a name="qs--bigendian"></a><span data-ttu-id="ce3e0-107">QS: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="ce3e0-107">qs : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="ce3e0-108">Регистр такта, к которому применяется преобразование Фурье в тактовой области</span><span class="sxs-lookup"><span data-stu-id="ce3e0-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="ce3e0-109">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ce3e0-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="ce3e0-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="ce3e0-110">Remarks</span></span>

<span data-ttu-id="ce3e0-111">Предполагается, что входные и выходные данные находятся в кодировке с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="ce3e0-111">The input and output are assumed to be in big endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce3e0-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="ce3e0-112">See Also</span></span>

- [<span data-ttu-id="ce3e0-113">Microsoft. тактов. Canon. Аппроксиматекфт</span><span class="sxs-lookup"><span data-stu-id="ce3e0-113">Microsoft.Quantum.Canon.ApproximateQFT</span></span>](xref:Microsoft.Quantum.Canon.ApproximateQFT)
- [<span data-ttu-id="ce3e0-114">Microsoft. тактов. Canon. КФТЛЕ</span><span class="sxs-lookup"><span data-stu-id="ce3e0-114">Microsoft.Quantum.Canon.QFTLE</span></span>](xref:Microsoft.Quantum.Canon.QFTLE)