---
uid: Microsoft.Quantum.Canon.ApplyQuantumFourierTransform
title: Операция Аппликуантумфауриертрансформ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyQuantumFourierTransform
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.
ms.openlocfilehash: fa8d135c0665f0a576229797d208b321ba0329a6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717792"
---
# <a name="applyquantumfouriertransform-operation"></a><span data-ttu-id="19056-102">Операция Аппликуантумфауриертрансформ</span><span class="sxs-lookup"><span data-stu-id="19056-102">ApplyQuantumFourierTransform operation</span></span>

<span data-ttu-id="19056-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="19056-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="19056-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="19056-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="19056-105">Выполняет преобразование Фурье в тактовую операцию для регистра такта, содержащего целое число в представлении с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="19056-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.</span></span>

```qsharp
operation ApplyQuantumFourierTransform (qs : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="19056-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="19056-106">Input</span></span>

### <a name="qs--littleendian"></a><span data-ttu-id="19056-107">QS: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="19056-107">qs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="19056-108">Регистр такта, к которому применяется преобразование Фурье в тактовой области</span><span class="sxs-lookup"><span data-stu-id="19056-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="19056-109">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="19056-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="19056-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="19056-110">Remarks</span></span>

<span data-ttu-id="19056-111">Предполагается, что входные и выходные данные находятся в кодировке с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="19056-111">The input and output are assumed to be in little endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="19056-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="19056-112">See Also</span></span>

- [<span data-ttu-id="19056-113">Microsoft. тактов. Canon. Аппликуантумфауриертрансформбе</span><span class="sxs-lookup"><span data-stu-id="19056-113">Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE</span></span>](xref:Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE)