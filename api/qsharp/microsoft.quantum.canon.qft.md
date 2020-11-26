---
uid: Microsoft.Quantum.Canon.QFT
title: Операция Кфт
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: QFT
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: 8f1aa8c3680a068e500503ca25afa9a49e4ef5bf
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205546"
---
# <a name="qft-operation"></a><span data-ttu-id="69d2a-102">Операция Кфт</span><span class="sxs-lookup"><span data-stu-id="69d2a-102">QFT operation</span></span>

<span data-ttu-id="69d2a-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="69d2a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="69d2a-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="69d2a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="69d2a-105">Выполняет преобразование Фурье в тактовую операцию для регистра такта, содержащего целое число в представлении с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="69d2a-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.</span></span>

```qsharp
operation QFT (qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="69d2a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="69d2a-106">Input</span></span>

### <a name="qs--bigendian"></a><span data-ttu-id="69d2a-107">QS: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="69d2a-107">qs : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="69d2a-108">Регистр такта, к которому применяется преобразование Фурье в тактовой области</span><span class="sxs-lookup"><span data-stu-id="69d2a-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="69d2a-109">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="69d2a-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="69d2a-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="69d2a-110">Remarks</span></span>

<span data-ttu-id="69d2a-111">Предполагается, что входные и выходные данные находятся в кодировке с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="69d2a-111">The input and output are assumed to be in big endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="69d2a-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="69d2a-112">See Also</span></span>

- [<span data-ttu-id="69d2a-113">Microsoft. тактов. Canon. Аппликуантумфауриертрансформбе</span><span class="sxs-lookup"><span data-stu-id="69d2a-113">Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE</span></span>](xref:Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE)