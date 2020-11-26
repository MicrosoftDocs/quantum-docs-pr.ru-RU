---
uid: Microsoft.Quantum.Canon.ApplyQuantumFourierTransform
title: Операция Аппликуантумфауриертрансформ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyQuantumFourierTransform
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.
ms.openlocfilehash: 6d3ad9ca2e0d10c264f8020e1f34687f6cbc9f94
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218195"
---
# <a name="applyquantumfouriertransform-operation"></a><span data-ttu-id="499f3-102">Операция Аппликуантумфауриертрансформ</span><span class="sxs-lookup"><span data-stu-id="499f3-102">ApplyQuantumFourierTransform operation</span></span>

<span data-ttu-id="499f3-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="499f3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="499f3-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="499f3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="499f3-105">Выполняет преобразование Фурье в тактовую операцию для регистра такта, содержащего целое число в представлении с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="499f3-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.</span></span>

```qsharp
operation ApplyQuantumFourierTransform (qs : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="499f3-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="499f3-106">Input</span></span>

### <a name="qs--littleendian"></a><span data-ttu-id="499f3-107">QS: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="499f3-107">qs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="499f3-108">Регистр такта, к которому применяется преобразование Фурье в тактовой области</span><span class="sxs-lookup"><span data-stu-id="499f3-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="499f3-109">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="499f3-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="499f3-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="499f3-110">Remarks</span></span>

<span data-ttu-id="499f3-111">Предполагается, что входные и выходные данные находятся в кодировке с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="499f3-111">The input and output are assumed to be in little endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="499f3-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="499f3-112">See Also</span></span>

- [<span data-ttu-id="499f3-113">Microsoft. тактов. Canon. Аппликуантумфауриертрансформбе</span><span class="sxs-lookup"><span data-stu-id="499f3-113">Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE</span></span>](xref:Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE)