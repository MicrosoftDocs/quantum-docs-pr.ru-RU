---
uid: Microsoft.Quantum.Canon.QFT
title: Операция Кфт
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: QFT
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: 30f475c3850c248b5af58db1e4aac3638c4c0471
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852294"
---
# <a name="qft-operation"></a><span data-ttu-id="d987c-102">Операция Кфт</span><span class="sxs-lookup"><span data-stu-id="d987c-102">QFT operation</span></span>

<span data-ttu-id="d987c-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d987c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d987c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d987c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d987c-105">Выполняет преобразование Фурье в тактовую операцию для регистра такта, содержащего целое число в представлении с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="d987c-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.</span></span>

```qsharp
operation QFT (qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="d987c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d987c-106">Input</span></span>

### <a name="qs--bigendian"></a><span data-ttu-id="d987c-107">QS: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="d987c-107">qs : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="d987c-108">Регистр такта, к которому применяется преобразование Фурье в тактовой области</span><span class="sxs-lookup"><span data-stu-id="d987c-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="d987c-109">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d987c-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="d987c-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="d987c-110">Remarks</span></span>

<span data-ttu-id="d987c-111">Предполагается, что входные и выходные данные находятся в кодировке с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="d987c-111">The input and output are assumed to be in big endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="d987c-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="d987c-112">See Also</span></span>

- [<span data-ttu-id="d987c-113">Microsoft. тактов. Canon. Аппликуантумфауриертрансформбе</span><span class="sxs-lookup"><span data-stu-id="d987c-113">Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE</span></span>](xref:Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE)