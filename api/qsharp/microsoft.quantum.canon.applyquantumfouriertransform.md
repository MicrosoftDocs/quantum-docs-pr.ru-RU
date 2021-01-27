---
uid: Microsoft.Quantum.Canon.ApplyQuantumFourierTransform
title: Операция Аппликуантумфауриертрансформ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyQuantumFourierTransform
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.
ms.openlocfilehash: d99000c21c79d2ca97b1fe92ad331c7ba8599700
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844764"
---
# <a name="applyquantumfouriertransform-operation"></a><span data-ttu-id="3d612-102">Операция Аппликуантумфауриертрансформ</span><span class="sxs-lookup"><span data-stu-id="3d612-102">ApplyQuantumFourierTransform operation</span></span>

<span data-ttu-id="3d612-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3d612-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3d612-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3d612-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3d612-105">Выполняет преобразование Фурье в тактовую операцию для регистра такта, содержащего целое число в представлении с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="3d612-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.</span></span>

```qsharp
operation ApplyQuantumFourierTransform (qs : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="3d612-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3d612-106">Input</span></span>

### <a name="qs--littleendian"></a><span data-ttu-id="3d612-107">QS: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="3d612-107">qs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="3d612-108">Регистр такта, к которому применяется преобразование Фурье в тактовой области</span><span class="sxs-lookup"><span data-stu-id="3d612-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="3d612-109">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3d612-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="3d612-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="3d612-110">Remarks</span></span>

<span data-ttu-id="3d612-111">Предполагается, что входные и выходные данные находятся в кодировке с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="3d612-111">The input and output are assumed to be in little endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="3d612-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="3d612-112">See Also</span></span>

- [<span data-ttu-id="3d612-113">Microsoft. тактов. Canon. Аппликуантумфауриертрансформбе</span><span class="sxs-lookup"><span data-stu-id="3d612-113">Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE</span></span>](xref:Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE)