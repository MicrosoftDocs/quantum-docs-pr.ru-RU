---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubits
title: Операция Апплитофирсттвокубитс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubits
qsharp.summary: Applies an operation to the first two qubits in the register.
ms.openlocfilehash: aad07889c0dbf2329304c98b06dbd0c225df8a81
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717315"
---
# <a name="applytofirsttwoqubits-operation"></a><span data-ttu-id="58ffa-102">Операция Апплитофирсттвокубитс</span><span class="sxs-lookup"><span data-stu-id="58ffa-102">ApplyToFirstTwoQubits operation</span></span>

<span data-ttu-id="58ffa-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="58ffa-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="58ffa-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="58ffa-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="58ffa-105">Применяет операцию к первым двум Кубитс в регистре.</span><span class="sxs-lookup"><span data-stu-id="58ffa-105">Applies an operation to the first two qubits in the register.</span></span>

```qsharp
operation ApplyToFirstTwoQubits (op : ((Qubit, Qubit) => Unit), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="58ffa-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="58ffa-106">Input</span></span>

### <a name="op--qubitqubit--unit"></a><span data-ttu-id="58ffa-107">Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit)) = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="58ffa-107">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="58ffa-108">Операция, применяемая к первым двум Кубитс</span><span class="sxs-lookup"><span data-stu-id="58ffa-108">An operation to be applied to the first two qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="58ffa-109">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="58ffa-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="58ffa-110">Массив кубит к первым двум Кубитс, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="58ffa-110">Qubit array to the first two qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="58ffa-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="58ffa-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="58ffa-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="58ffa-112">Remarks</span></span>

<span data-ttu-id="58ffa-113">Это соответствует следующей записи:</span><span class="sxs-lookup"><span data-stu-id="58ffa-113">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a><span data-ttu-id="58ffa-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="58ffa-114">See Also</span></span>

- [<span data-ttu-id="58ffa-115">Microsoft. тактов. Canon. Апплитофирсттвокубитса</span><span class="sxs-lookup"><span data-stu-id="58ffa-115">Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsA)
- [<span data-ttu-id="58ffa-116">Microsoft. тактов. Canon. Апплитофирсттвокубитск</span><span class="sxs-lookup"><span data-stu-id="58ffa-116">Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsC)
- [<span data-ttu-id="58ffa-117">Microsoft. тактов. Canon. Апплитофирсттвокубитска</span><span class="sxs-lookup"><span data-stu-id="58ffa-117">Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsCA)