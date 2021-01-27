---
uid: Microsoft.Quantum.Canon.QFTLE
title: Операция КФТЛЕ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: QFTLE
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.
ms.openlocfilehash: 893366833e5bd6b358884c11f4534609efd72d24
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852278"
---
# <a name="qftle-operation"></a><span data-ttu-id="884aa-102">Операция КФТЛЕ</span><span class="sxs-lookup"><span data-stu-id="884aa-102">QFTLE operation</span></span>

<span data-ttu-id="884aa-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="884aa-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="884aa-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="884aa-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="884aa-105">Выполняет преобразование Фурье в тактовую операцию для регистра такта, содержащего целое число в представлении с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="884aa-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.</span></span>

```qsharp
operation QFTLE (qs : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="884aa-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="884aa-106">Input</span></span>

### <a name="qs--littleendian"></a><span data-ttu-id="884aa-107">QS: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="884aa-107">qs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="884aa-108">Регистр такта, к которому применяется преобразование Фурье в тактовой области</span><span class="sxs-lookup"><span data-stu-id="884aa-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="884aa-109">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="884aa-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="884aa-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="884aa-110">Remarks</span></span>

<span data-ttu-id="884aa-111">Предполагается, что входные и выходные данные находятся в кодировке с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="884aa-111">The input and output are assumed to be in little endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="884aa-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="884aa-112">See Also</span></span>

- [<span data-ttu-id="884aa-113">Microsoft. тактов. Canon. Кфт</span><span class="sxs-lookup"><span data-stu-id="884aa-113">Microsoft.Quantum.Canon.QFT</span></span>](xref:Microsoft.Quantum.Canon.QFT)