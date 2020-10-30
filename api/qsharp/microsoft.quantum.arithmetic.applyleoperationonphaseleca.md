---
uid: Microsoft.Quantum.Arithmetic.ApplyLEOperationOnPhaseLECA
title: Операция Апплилеоператиононфаселека
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyLEOperationOnPhaseLECA
qsharp.summary: Applies an operation that takes a <xref:microsoft.quantum.arithmetic.phaselittleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.littleendian>.
ms.openlocfilehash: 9d70e89fe4186244361d80252b856878772eda30
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731848"
---
# <a name="applyleoperationonphaseleca-operation"></a><span data-ttu-id="a5abc-102">Операция Апплилеоператиононфаселека</span><span class="sxs-lookup"><span data-stu-id="a5abc-102">ApplyLEOperationOnPhaseLECA operation</span></span>

<span data-ttu-id="a5abc-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="a5abc-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="a5abc-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a5abc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a5abc-105">Применяет операцию, которая принимает <xref:microsoft.quantum.arithmetic.phaselittleendian> регистрацию в качестве входных данных для целевого регистра типа <xref:microsoft.quantum.arithmetic.littleendian> .</span><span class="sxs-lookup"><span data-stu-id="a5abc-105">Applies an operation that takes a <xref:microsoft.quantum.arithmetic.phaselittleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.littleendian>.</span></span>

```qsharp
operation ApplyLEOperationOnPhaseLECA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl), target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="a5abc-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a5abc-106">Input</span></span>

### <a name="op--littleendian--unit-adj--ctl"></a><span data-ttu-id="a5abc-107">Op: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="a5abc-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="a5abc-108">Операция, которая будет применена.</span><span class="sxs-lookup"><span data-stu-id="a5abc-108">The operation to be applied.</span></span>


### <a name="target--phaselittleendian"></a><span data-ttu-id="a5abc-109">Целевой объект: [фаселиттлиндиан](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a5abc-109">target : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="a5abc-110">Регистр, к которому применяется операция.</span><span class="sxs-lookup"><span data-stu-id="a5abc-110">The register to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a5abc-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a5abc-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a5abc-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="a5abc-112">Remarks</span></span>

<span data-ttu-id="a5abc-113">Регистр преобразуется в `LittleEndian` с помощью <xref:microsoft.quantum.canon.qftle> и возвращается в исходное представление после применения `op` .</span><span class="sxs-lookup"><span data-stu-id="a5abc-113">The register is transformed to `LittleEndian` by the use of <xref:microsoft.quantum.canon.qftle> and is then returned to its original representation after application of `op`.</span></span>

## <a name="see-also"></a><span data-ttu-id="a5abc-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="a5abc-114">See Also</span></span>

- [<span data-ttu-id="a5abc-115">Microsoft. тактов. Canon. Апплилеоператиононфаселе</span><span class="sxs-lookup"><span data-stu-id="a5abc-115">Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLE</span></span>](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLE)
- [<span data-ttu-id="a5abc-116">Microsoft. тактов. Canon. Апплилеоператиононфаселеа</span><span class="sxs-lookup"><span data-stu-id="a5abc-116">Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEA</span></span>](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEA)
- [<span data-ttu-id="a5abc-117">Microsoft. тактов. Canon. Апплилеоператиононфаселек</span><span class="sxs-lookup"><span data-stu-id="a5abc-117">Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEC</span></span>](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEC)