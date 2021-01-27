---
uid: Microsoft.Quantum.Arithmetic.ApplyLEOperationOnPhaseLEC
title: Операция Апплилеоператиононфаселек
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyLEOperationOnPhaseLEC
qsharp.summary: Applies an operation that takes a <xref:microsoft.quantum.arithmetic.phaselittleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.littleendian>.
ms.openlocfilehash: 60d84e2f6c3693ba0c40e2eb034b658ac8097ad8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843759"
---
# <a name="applyleoperationonphaselec-operation"></a><span data-ttu-id="aa576-102">Операция Апплилеоператиононфаселек</span><span class="sxs-lookup"><span data-stu-id="aa576-102">ApplyLEOperationOnPhaseLEC operation</span></span>

<span data-ttu-id="aa576-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="aa576-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="aa576-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="aa576-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="aa576-105">Применяет операцию, которая принимает <xref:microsoft.quantum.arithmetic.phaselittleendian> регистрацию в качестве входных данных для целевого регистра типа <xref:microsoft.quantum.arithmetic.littleendian> .</span><span class="sxs-lookup"><span data-stu-id="aa576-105">Applies an operation that takes a <xref:microsoft.quantum.arithmetic.phaselittleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.littleendian>.</span></span>

```qsharp
operation ApplyLEOperationOnPhaseLEC (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl), target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="aa576-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="aa576-106">Input</span></span>

### <a name="op--littleendian--unit--is-ctl"></a><span data-ttu-id="aa576-107">Op: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  — CTL</span><span class="sxs-lookup"><span data-stu-id="aa576-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="aa576-108">Операция, которая будет применена.</span><span class="sxs-lookup"><span data-stu-id="aa576-108">The operation to be applied.</span></span>


### <a name="target--phaselittleendian"></a><span data-ttu-id="aa576-109">Целевой объект: [фаселиттлиндиан](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="aa576-109">target : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="aa576-110">Регистр, к которому применяется операция.</span><span class="sxs-lookup"><span data-stu-id="aa576-110">The register to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="aa576-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="aa576-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="aa576-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="aa576-112">Remarks</span></span>

<span data-ttu-id="aa576-113">Регистр преобразуется в `LittleEndian` с помощью <xref:microsoft.quantum.canon.qftle> и возвращается в исходное представление после применения `op` .</span><span class="sxs-lookup"><span data-stu-id="aa576-113">The register is transformed to `LittleEndian` by the use of <xref:microsoft.quantum.canon.qftle> and is then returned to its original representation after application of `op`.</span></span>

## <a name="see-also"></a><span data-ttu-id="aa576-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="aa576-114">See Also</span></span>

- [<span data-ttu-id="aa576-115">Microsoft. тактов. Canon. Апплилеоператиононфаселе</span><span class="sxs-lookup"><span data-stu-id="aa576-115">Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLE</span></span>](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLE)
- [<span data-ttu-id="aa576-116">Microsoft. тактов. Canon. Апплилеоператиононфаселеа</span><span class="sxs-lookup"><span data-stu-id="aa576-116">Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEA</span></span>](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEA)
- [<span data-ttu-id="aa576-117">Microsoft. тактов. Canon. Апплилеоператиононфаселека</span><span class="sxs-lookup"><span data-stu-id="aa576-117">Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLECA</span></span>](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLECA)