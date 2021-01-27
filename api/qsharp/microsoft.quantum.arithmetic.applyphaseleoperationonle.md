---
uid: Microsoft.Quantum.Arithmetic.ApplyPhaseLEOperationOnLE
title: Операция Апплифаселеоператиононле
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyPhaseLEOperationOnLE
qsharp.summary: Applies an operation that takes a <xref:microsoft.quantum.arithmetic.littleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.phaselittleendian>.
ms.openlocfilehash: d94fdb55e051e76dd518eff14b80d1a24516bf8a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843675"
---
# <a name="applyphaseleoperationonle-operation"></a><span data-ttu-id="baf6c-102">Операция Апплифаселеоператиононле</span><span class="sxs-lookup"><span data-stu-id="baf6c-102">ApplyPhaseLEOperationOnLE operation</span></span>

<span data-ttu-id="baf6c-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="baf6c-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="baf6c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="baf6c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="baf6c-105">Применяет операцию, которая принимает <xref:microsoft.quantum.arithmetic.littleendian> регистрацию в качестве входных данных для целевого регистра типа <xref:microsoft.quantum.arithmetic.phaselittleendian> .</span><span class="sxs-lookup"><span data-stu-id="baf6c-105">Applies an operation that takes a <xref:microsoft.quantum.arithmetic.littleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.phaselittleendian>.</span></span>

```qsharp
operation ApplyPhaseLEOperationOnLE (op : (Microsoft.Quantum.Arithmetic.PhaseLittleEndian => Unit), target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="baf6c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="baf6c-106">Input</span></span>

### <a name="op--phaselittleendian--unit"></a><span data-ttu-id="baf6c-107">Op: [фаселиттлиндиан](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="baf6c-107">op : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="baf6c-108">Операция, которая будет применена.</span><span class="sxs-lookup"><span data-stu-id="baf6c-108">The operation to be applied.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="baf6c-109">Целевой объект: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="baf6c-109">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="baf6c-110">Регистр, к которому применяется операция.</span><span class="sxs-lookup"><span data-stu-id="baf6c-110">The register to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="baf6c-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="baf6c-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="baf6c-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="baf6c-112">Remarks</span></span>

<span data-ttu-id="baf6c-113">Регистр преобразуется в `PhaseLittleEndian` с помощью <xref:microsoft.quantum.canon.qftle> и возвращается в исходное представление после применения `op` .</span><span class="sxs-lookup"><span data-stu-id="baf6c-113">The register is transformed to `PhaseLittleEndian` by the use of <xref:microsoft.quantum.canon.qftle> and is then returned to its original representation after application of `op`.</span></span>

## <a name="see-also"></a><span data-ttu-id="baf6c-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="baf6c-114">See Also</span></span>

- [<span data-ttu-id="baf6c-115">Microsoft. тактов. Canon. Апплифаселеоператиононлеа</span><span class="sxs-lookup"><span data-stu-id="baf6c-115">Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA</span></span>](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA)
- [<span data-ttu-id="baf6c-116">Microsoft. тактов. Canon. Апплифаселеоператиононлеа</span><span class="sxs-lookup"><span data-stu-id="baf6c-116">Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA</span></span>](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA)
- [<span data-ttu-id="baf6c-117">Microsoft. тактов. Canon. Апплифаселеоператиононлека</span><span class="sxs-lookup"><span data-stu-id="baf6c-117">Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLECA</span></span>](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLECA)