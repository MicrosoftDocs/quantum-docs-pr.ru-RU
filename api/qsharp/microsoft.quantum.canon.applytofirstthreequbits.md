---
uid: Microsoft.Quantum.Canon.ApplyToFirstThreeQubits
title: Операция Апплитофирстсрикубитс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstThreeQubits
qsharp.summary: Applies an operation to the first three qubits in the register.
ms.openlocfilehash: b01c1072306cfdebcb90827a14683a32312481fc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850704"
---
# <a name="applytofirstthreequbits-operation"></a><span data-ttu-id="b9c0a-102">Операция Апплитофирстсрикубитс</span><span class="sxs-lookup"><span data-stu-id="b9c0a-102">ApplyToFirstThreeQubits operation</span></span>

<span data-ttu-id="b9c0a-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b9c0a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b9c0a-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b9c0a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b9c0a-105">Применяет операцию к первым трем Кубитс в регистре.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-105">Applies an operation to the first three qubits in the register.</span></span>

```qsharp
operation ApplyToFirstThreeQubits (op : ((Qubit, Qubit, Qubit) => Unit), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="b9c0a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b9c0a-106">Input</span></span>

### <a name="op--qubitqubitqubit--unit"></a><span data-ttu-id="b9c0a-107">Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit)) = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="b9c0a-107">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="b9c0a-108">Операция, применяемая к первым трем Кубитс</span><span class="sxs-lookup"><span data-stu-id="b9c0a-108">An operation to be applied to the first three qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="b9c0a-109">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b9c0a-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b9c0a-110">Массив кубит к первым трем Кубитс, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-110">Qubit array to the first three qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b9c0a-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b9c0a-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="b9c0a-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="b9c0a-112">Remarks</span></span>

<span data-ttu-id="b9c0a-113">Это соответствует следующей записи:</span><span class="sxs-lookup"><span data-stu-id="b9c0a-113">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1], register[2]);
```

## <a name="see-also"></a><span data-ttu-id="b9c0a-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="b9c0a-114">See Also</span></span>

- [<span data-ttu-id="b9c0a-115">Microsoft. тактов. Canon. Апплитофирстсрикубитск</span><span class="sxs-lookup"><span data-stu-id="b9c0a-115">Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsC)
- [<span data-ttu-id="b9c0a-116">Microsoft. тактов. Canon. Апплитофирстсрикубитса</span><span class="sxs-lookup"><span data-stu-id="b9c0a-116">Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsA)
- [<span data-ttu-id="b9c0a-117">Microsoft. тактов. Canon. Апплитофирстсрикубитска</span><span class="sxs-lookup"><span data-stu-id="b9c0a-117">Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsCA)