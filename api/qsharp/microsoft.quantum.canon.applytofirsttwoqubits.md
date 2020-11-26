---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubits
title: Операция Апплитофирсттвокубитс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubits
qsharp.summary: Applies an operation to the first two qubits in the register.
ms.openlocfilehash: e4f1eb396efb390c7470ea2aaf5c3b5be60b8c1b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217413"
---
# <a name="applytofirsttwoqubits-operation"></a><span data-ttu-id="ae5e7-102">Операция Апплитофирсттвокубитс</span><span class="sxs-lookup"><span data-stu-id="ae5e7-102">ApplyToFirstTwoQubits operation</span></span>

<span data-ttu-id="ae5e7-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ae5e7-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ae5e7-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ae5e7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ae5e7-105">Применяет операцию к первым двум Кубитс в регистре.</span><span class="sxs-lookup"><span data-stu-id="ae5e7-105">Applies an operation to the first two qubits in the register.</span></span>

```qsharp
operation ApplyToFirstTwoQubits (op : ((Qubit, Qubit) => Unit), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="ae5e7-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ae5e7-106">Input</span></span>

### <a name="op--qubitqubit--unit"></a><span data-ttu-id="ae5e7-107">Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit)) = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="ae5e7-107">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="ae5e7-108">Операция, применяемая к первым двум Кубитс</span><span class="sxs-lookup"><span data-stu-id="ae5e7-108">An operation to be applied to the first two qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="ae5e7-109">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ae5e7-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="ae5e7-110">Массив кубит к первым двум Кубитс, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="ae5e7-110">Qubit array to the first two qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ae5e7-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ae5e7-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="ae5e7-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ae5e7-112">Remarks</span></span>

<span data-ttu-id="ae5e7-113">Это соответствует следующей записи:</span><span class="sxs-lookup"><span data-stu-id="ae5e7-113">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a><span data-ttu-id="ae5e7-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="ae5e7-114">See Also</span></span>

- [<span data-ttu-id="ae5e7-115">Microsoft. тактов. Canon. Апплитофирсттвокубитса</span><span class="sxs-lookup"><span data-stu-id="ae5e7-115">Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsA)
- [<span data-ttu-id="ae5e7-116">Microsoft. тактов. Canon. Апплитофирсттвокубитск</span><span class="sxs-lookup"><span data-stu-id="ae5e7-116">Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsC)
- [<span data-ttu-id="ae5e7-117">Microsoft. тактов. Canon. Апплитофирсттвокубитска</span><span class="sxs-lookup"><span data-stu-id="ae5e7-117">Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsCA)