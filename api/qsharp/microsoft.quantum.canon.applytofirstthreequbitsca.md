---
uid: Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsCA
title: Операция Апплитофирстсрикубитска
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstThreeQubitsCA
qsharp.summary: Applies an operation to the first three qubits in the register. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 9bc5248b5de0db60f54bbec4cb33dde1160c2b41
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841378"
---
# <a name="applytofirstthreequbitsca-operation"></a><span data-ttu-id="1429b-102">Операция Апплитофирстсрикубитска</span><span class="sxs-lookup"><span data-stu-id="1429b-102">ApplyToFirstThreeQubitsCA operation</span></span>

<span data-ttu-id="1429b-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1429b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1429b-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1429b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1429b-105">Применяет операцию к первым трем Кубитс в регистре.</span><span class="sxs-lookup"><span data-stu-id="1429b-105">Applies an operation to the first three qubits in the register.</span></span>
<span data-ttu-id="1429b-106">Модификатор `CA` указывает, что операция является управляемой и аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="1429b-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToFirstThreeQubitsCA (op : ((Qubit, Qubit, Qubit) => Unit is Adj + Ctl), register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="1429b-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="1429b-107">Input</span></span>

### <a name="op--qubitqubitqubit--unit--is-adj--ctl"></a><span data-ttu-id="1429b-108">Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit)) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="1429b-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="1429b-109">Операция, применяемая к первым трем Кубитс</span><span class="sxs-lookup"><span data-stu-id="1429b-109">An operation to be applied to the first three qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="1429b-110">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="1429b-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="1429b-111">Массив кубит к первым трем Кубитс, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="1429b-111">Qubit array to the first three qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1429b-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1429b-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="1429b-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="1429b-113">Remarks</span></span>

<span data-ttu-id="1429b-114">Это соответствует следующей записи:</span><span class="sxs-lookup"><span data-stu-id="1429b-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1], register[2]);
```

## <a name="see-also"></a><span data-ttu-id="1429b-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="1429b-115">See Also</span></span>

- [<span data-ttu-id="1429b-116">Microsoft. тактов. Canon. Апплитофирстсрикубитс</span><span class="sxs-lookup"><span data-stu-id="1429b-116">Microsoft.Quantum.Canon.ApplyToFirstThreeQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubits)