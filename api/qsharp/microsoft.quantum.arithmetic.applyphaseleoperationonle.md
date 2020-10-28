---
uid: Microsoft.Quantum.Arithmetic.ApplyPhaseLEOperationOnLE
title: Операция Апплифаселеоператиононле
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyPhaseLEOperationOnLE
qsharp.summary: Applies an operation that takes a <xref:microsoft.quantum.arithmetic.littleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.phaselittleendian>.
ms.openlocfilehash: dacc52766cf72d2bd562b76fc4939f962133e9a7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731801"
---
# <a name="applyphaseleoperationonle-operation"></a><span data-ttu-id="c24de-102">Операция Апплифаселеоператиононле</span><span class="sxs-lookup"><span data-stu-id="c24de-102">ApplyPhaseLEOperationOnLE operation</span></span>

<span data-ttu-id="c24de-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="c24de-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="c24de-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c24de-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c24de-105">Применяет операцию, которая принимает <xref:microsoft.quantum.arithmetic.littleendian> регистрацию в качестве входных данных для целевого регистра типа <xref:microsoft.quantum.arithmetic.phaselittleendian> .</span><span class="sxs-lookup"><span data-stu-id="c24de-105">Applies an operation that takes a <xref:microsoft.quantum.arithmetic.littleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.phaselittleendian>.</span></span>

```qsharp
operation ApplyPhaseLEOperationOnLE (op : (Microsoft.Quantum.Arithmetic.PhaseLittleEndian => Unit), target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="c24de-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c24de-106">Input</span></span>

### <a name="op--phaselittleendian--unit"></a><span data-ttu-id="c24de-107">Op: [фаселиттлиндиан](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c24de-107">op : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="c24de-108">Операция, которая будет применена.</span><span class="sxs-lookup"><span data-stu-id="c24de-108">The operation to be applied.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="c24de-109">Целевой объект: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="c24de-109">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="c24de-110">Регистр, к которому применяется операция.</span><span class="sxs-lookup"><span data-stu-id="c24de-110">The register to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c24de-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c24de-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="c24de-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="c24de-112">Remarks</span></span>

<span data-ttu-id="c24de-113">Регистр преобразуется в `PhaseLittleEndian` с помощью <xref:microsoft.quantum.canon.qftle> и возвращается в исходное представление после применения `op` .</span><span class="sxs-lookup"><span data-stu-id="c24de-113">The register is transformed to `PhaseLittleEndian` by the use of <xref:microsoft.quantum.canon.qftle> and is then returned to its original representation after application of `op`.</span></span>

## <a name="see-also"></a><span data-ttu-id="c24de-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="c24de-114">See Also</span></span>

- [<span data-ttu-id="c24de-115">Microsoft. тактов. Canon. Апплифаселеоператиононлеа</span><span class="sxs-lookup"><span data-stu-id="c24de-115">Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA</span></span>](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA)
- [<span data-ttu-id="c24de-116">Microsoft. тактов. Canon. Апплифаселеоператиононлеа</span><span class="sxs-lookup"><span data-stu-id="c24de-116">Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA</span></span>](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA)
- [<span data-ttu-id="c24de-117">Microsoft. тактов. Canon. Апплифаселеоператиононлека</span><span class="sxs-lookup"><span data-stu-id="c24de-117">Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLECA</span></span>](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLECA)