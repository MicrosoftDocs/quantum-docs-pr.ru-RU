---
uid: Microsoft.Quantum.Canon.ApplyToFirstThreeQubits
title: Операция Апплитофирстсрикубитс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstThreeQubits
qsharp.summary: Applies an operation to the first three qubits in the register.
ms.openlocfilehash: 61330f9e9b1f6b9f3965c9240505814b295aaefe
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717385"
---
# <a name="applytofirstthreequbits-operation"></a><span data-ttu-id="09976-102">Операция Апплитофирстсрикубитс</span><span class="sxs-lookup"><span data-stu-id="09976-102">ApplyToFirstThreeQubits operation</span></span>

<span data-ttu-id="09976-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="09976-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="09976-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="09976-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="09976-105">Применяет операцию к первым трем Кубитс в регистре.</span><span class="sxs-lookup"><span data-stu-id="09976-105">Applies an operation to the first three qubits in the register.</span></span>

```qsharp
operation ApplyToFirstThreeQubits (op : ((Qubit, Qubit, Qubit) => Unit), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="09976-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="09976-106">Input</span></span>

### <a name="op--qubitqubitqubit--unit"></a><span data-ttu-id="09976-107">Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit)) = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="09976-107">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="09976-108">Операция, применяемая к первым трем Кубитс</span><span class="sxs-lookup"><span data-stu-id="09976-108">An operation to be applied to the first three qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="09976-109">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="09976-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="09976-110">Массив кубит к первым трем Кубитс, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="09976-110">Qubit array to the first three qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="09976-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="09976-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="09976-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="09976-112">Remarks</span></span>

<span data-ttu-id="09976-113">Это соответствует следующей записи:</span><span class="sxs-lookup"><span data-stu-id="09976-113">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1], register[2]);
```

## <a name="see-also"></a><span data-ttu-id="09976-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="09976-114">See Also</span></span>

- [<span data-ttu-id="09976-115">Microsoft. тактов. Canon. Апплитофирстсрикубитск</span><span class="sxs-lookup"><span data-stu-id="09976-115">Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsC)
- [<span data-ttu-id="09976-116">Microsoft. тактов. Canon. Апплитофирстсрикубитса</span><span class="sxs-lookup"><span data-stu-id="09976-116">Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsA)
- [<span data-ttu-id="09976-117">Microsoft. тактов. Canon. Апплитофирстсрикубитска</span><span class="sxs-lookup"><span data-stu-id="09976-117">Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsCA)