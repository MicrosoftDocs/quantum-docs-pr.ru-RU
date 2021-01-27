---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsC
title: Операция Апплитофирсттвокубитск
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubitsC
qsharp.summary: Applies an operation to the first two qubits in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: f71209a806b0d1d712a3c776eb45e62d1cd5d5f7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841353"
---
# <a name="applytofirsttwoqubitsc-operation"></a><span data-ttu-id="3ba39-102">Операция Апплитофирсттвокубитск</span><span class="sxs-lookup"><span data-stu-id="3ba39-102">ApplyToFirstTwoQubitsC operation</span></span>

<span data-ttu-id="3ba39-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3ba39-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3ba39-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3ba39-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3ba39-105">Применяет операцию к первым двум Кубитс в регистре.</span><span class="sxs-lookup"><span data-stu-id="3ba39-105">Applies an operation to the first two qubits in the register.</span></span>
<span data-ttu-id="3ba39-106">Модификатор `C` указывает, что операция является управляемой.</span><span class="sxs-lookup"><span data-stu-id="3ba39-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToFirstTwoQubitsC (op : ((Qubit, Qubit) => Unit is Ctl), register : Qubit[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="3ba39-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3ba39-107">Input</span></span>

### <a name="op--qubitqubit--unit--is-ctl"></a><span data-ttu-id="3ba39-108">Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit)) => [единица](xref:microsoft.quantum.lang-ref.unit)  — CTL</span><span class="sxs-lookup"><span data-stu-id="3ba39-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="3ba39-109">Операция, применяемая к первым двум Кубитс</span><span class="sxs-lookup"><span data-stu-id="3ba39-109">An operation to be applied to the first two qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="3ba39-110">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="3ba39-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="3ba39-111">Массив кубит к первым двум Кубитс, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="3ba39-111">Qubit array to the first two qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3ba39-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3ba39-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="3ba39-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="3ba39-113">Remarks</span></span>

<span data-ttu-id="3ba39-114">Это соответствует следующей записи:</span><span class="sxs-lookup"><span data-stu-id="3ba39-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a><span data-ttu-id="3ba39-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="3ba39-115">See Also</span></span>

- [<span data-ttu-id="3ba39-116">Microsoft. тактов. Canon. Апплитофирсттвокубитс</span><span class="sxs-lookup"><span data-stu-id="3ba39-116">Microsoft.Quantum.Canon.ApplyToFirstTwoQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubits)