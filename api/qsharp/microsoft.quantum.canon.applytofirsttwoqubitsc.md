---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsC
title: Операция Апплитофирсттвокубитск
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubitsC
qsharp.summary: Applies an operation to the first two qubits in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 97706ffcc8700a0055ff37bbbaccc6fb4f8854b6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717287"
---
# <a name="applytofirsttwoqubitsc-operation"></a><span data-ttu-id="97fbc-102">Операция Апплитофирсттвокубитск</span><span class="sxs-lookup"><span data-stu-id="97fbc-102">ApplyToFirstTwoQubitsC operation</span></span>

<span data-ttu-id="97fbc-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="97fbc-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="97fbc-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="97fbc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="97fbc-105">Применяет операцию к первым двум Кубитс в регистре.</span><span class="sxs-lookup"><span data-stu-id="97fbc-105">Applies an operation to the first two qubits in the register.</span></span>
<span data-ttu-id="97fbc-106">Модификатор `C` указывает, что операция является управляемой.</span><span class="sxs-lookup"><span data-stu-id="97fbc-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToFirstTwoQubitsC (op : ((Qubit, Qubit) => Unit is Ctl), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="97fbc-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="97fbc-107">Input</span></span>

### <a name="op--qubitqubit--unit-ctl"></a><span data-ttu-id="97fbc-108">Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit)) = CTL [единицы](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="97fbc-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="97fbc-109">Операция, применяемая к первым двум Кубитс</span><span class="sxs-lookup"><span data-stu-id="97fbc-109">An operation to be applied to the first two qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="97fbc-110">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="97fbc-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="97fbc-111">Массив кубит к первым двум Кубитс, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="97fbc-111">Qubit array to the first two qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="97fbc-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="97fbc-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="97fbc-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="97fbc-113">Remarks</span></span>

<span data-ttu-id="97fbc-114">Это соответствует следующей записи:</span><span class="sxs-lookup"><span data-stu-id="97fbc-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a><span data-ttu-id="97fbc-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="97fbc-115">See Also</span></span>

- [<span data-ttu-id="97fbc-116">Microsoft. тактов. Canon. Апплитофирсттвокубитс</span><span class="sxs-lookup"><span data-stu-id="97fbc-116">Microsoft.Quantum.Canon.ApplyToFirstTwoQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubits)