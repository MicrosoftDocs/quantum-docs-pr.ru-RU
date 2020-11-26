---
uid: Microsoft.Quantum.Canon.ApplyToFirstThreeQubits
title: Операция Апплитофирстсрикубитс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstThreeQubits
qsharp.summary: Applies an operation to the first three qubits in the register.
ms.openlocfilehash: 5572bd2a096a4f9bdb1153ae80950ae854965b82
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217464"
---
# <a name="applytofirstthreequbits-operation"></a><span data-ttu-id="4b665-102">Операция Апплитофирстсрикубитс</span><span class="sxs-lookup"><span data-stu-id="4b665-102">ApplyToFirstThreeQubits operation</span></span>

<span data-ttu-id="4b665-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4b665-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4b665-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4b665-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4b665-105">Применяет операцию к первым трем Кубитс в регистре.</span><span class="sxs-lookup"><span data-stu-id="4b665-105">Applies an operation to the first three qubits in the register.</span></span>

```qsharp
operation ApplyToFirstThreeQubits (op : ((Qubit, Qubit, Qubit) => Unit), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="4b665-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4b665-106">Input</span></span>

### <a name="op--qubitqubitqubit--unit"></a><span data-ttu-id="4b665-107">Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit)) = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="4b665-107">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="4b665-108">Операция, применяемая к первым трем Кубитс</span><span class="sxs-lookup"><span data-stu-id="4b665-108">An operation to be applied to the first three qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="4b665-109">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="4b665-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="4b665-110">Массив кубит к первым трем Кубитс, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="4b665-110">Qubit array to the first three qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4b665-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4b665-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="4b665-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b665-112">Remarks</span></span>

<span data-ttu-id="4b665-113">Это соответствует следующей записи:</span><span class="sxs-lookup"><span data-stu-id="4b665-113">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1], register[2]);
```

## <a name="see-also"></a><span data-ttu-id="4b665-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="4b665-114">See Also</span></span>

- [<span data-ttu-id="4b665-115">Microsoft. тактов. Canon. Апплитофирстсрикубитск</span><span class="sxs-lookup"><span data-stu-id="4b665-115">Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsC)
- [<span data-ttu-id="4b665-116">Microsoft. тактов. Canon. Апплитофирстсрикубитса</span><span class="sxs-lookup"><span data-stu-id="4b665-116">Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsA)
- [<span data-ttu-id="4b665-117">Microsoft. тактов. Canon. Апплитофирстсрикубитска</span><span class="sxs-lookup"><span data-stu-id="4b665-117">Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsCA)