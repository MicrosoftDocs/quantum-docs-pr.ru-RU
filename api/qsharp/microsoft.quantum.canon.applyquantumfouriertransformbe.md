---
uid: Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE
title: Операция Аппликуантумфауриертрансформбе
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyQuantumFourierTransformBE
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: a1f4a0a5e94465fc8bf3af344e2e19ee0d1d15e2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841566"
---
# <a name="applyquantumfouriertransformbe-operation"></a><span data-ttu-id="125fd-102">Операция Аппликуантумфауриертрансформбе</span><span class="sxs-lookup"><span data-stu-id="125fd-102">ApplyQuantumFourierTransformBE operation</span></span>

<span data-ttu-id="125fd-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="125fd-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="125fd-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="125fd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="125fd-105">Выполняет преобразование Фурье в тактовую операцию для регистра такта, содержащего целое число в представлении с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="125fd-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.</span></span>

```qsharp
operation ApplyQuantumFourierTransformBE (qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="125fd-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="125fd-106">Input</span></span>

### <a name="qs--bigendian"></a><span data-ttu-id="125fd-107">QS: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="125fd-107">qs : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="125fd-108">Регистр такта, к которому применяется преобразование Фурье в тактовой области</span><span class="sxs-lookup"><span data-stu-id="125fd-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="125fd-109">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="125fd-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="125fd-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="125fd-110">Remarks</span></span>

<span data-ttu-id="125fd-111">Предполагается, что входные и выходные данные находятся в кодировке с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="125fd-111">The input and output are assumed to be in big endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="125fd-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="125fd-112">See Also</span></span>

- [<span data-ttu-id="125fd-113">Microsoft. тактов. Canon. Аппроксиматекфт</span><span class="sxs-lookup"><span data-stu-id="125fd-113">Microsoft.Quantum.Canon.ApproximateQFT</span></span>](xref:Microsoft.Quantum.Canon.ApproximateQFT)
- [<span data-ttu-id="125fd-114">Microsoft. тактов. Canon. КФТЛЕ</span><span class="sxs-lookup"><span data-stu-id="125fd-114">Microsoft.Quantum.Canon.QFTLE</span></span>](xref:Microsoft.Quantum.Canon.QFTLE)