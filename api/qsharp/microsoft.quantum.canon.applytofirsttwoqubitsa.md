---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsA
title: Операция Апплитофирсттвокубитса
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubitsA
qsharp.summary: Applies an operation to the first two qubits in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 911e9bc3d02bf6c0395c30fa167a6cb730dc666e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717302"
---
# <a name="applytofirsttwoqubitsa-operation"></a><span data-ttu-id="ec930-102">Операция Апплитофирсттвокубитса</span><span class="sxs-lookup"><span data-stu-id="ec930-102">ApplyToFirstTwoQubitsA operation</span></span>

<span data-ttu-id="ec930-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ec930-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ec930-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ec930-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ec930-105">Применяет операцию к первым двум Кубитс в регистре.</span><span class="sxs-lookup"><span data-stu-id="ec930-105">Applies an operation to the first two qubits in the register.</span></span>
<span data-ttu-id="ec930-106">Модификатор `A` указывает, что операция является аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="ec930-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToFirstTwoQubitsA (op : ((Qubit, Qubit) => Unit is Adj), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="ec930-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ec930-107">Input</span></span>

### <a name="op--qubitqubit--unit-adj"></a><span data-ttu-id="ec930-108">Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit)) [=>ное](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="ec930-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="ec930-109">Операция, применяемая к первым двум Кубитс</span><span class="sxs-lookup"><span data-stu-id="ec930-109">An operation to be applied to the first two qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="ec930-110">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ec930-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="ec930-111">Массив кубит к первым двум Кубитс, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="ec930-111">Qubit array to the first two qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ec930-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ec930-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="ec930-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="ec930-113">Remarks</span></span>

<span data-ttu-id="ec930-114">Это соответствует следующей записи:</span><span class="sxs-lookup"><span data-stu-id="ec930-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a><span data-ttu-id="ec930-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="ec930-115">See Also</span></span>

- [<span data-ttu-id="ec930-116">Microsoft. тактов. Canon. Апплитофирсттвокубитс</span><span class="sxs-lookup"><span data-stu-id="ec930-116">Microsoft.Quantum.Canon.ApplyToFirstTwoQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubits)