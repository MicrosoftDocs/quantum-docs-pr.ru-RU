---
uid: Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsC
title: Операция Апплитофирстсрикубитск
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstThreeQubitsC
qsharp.summary: Applies an operation to the first three qubits in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: cb6945f5aa398d0bf6417c5cfd21142008a54b13
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217447"
---
# <a name="applytofirstthreequbitsc-operation"></a><span data-ttu-id="53db0-102">Операция Апплитофирстсрикубитск</span><span class="sxs-lookup"><span data-stu-id="53db0-102">ApplyToFirstThreeQubitsC operation</span></span>

<span data-ttu-id="53db0-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="53db0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="53db0-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="53db0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="53db0-105">Применяет операцию к первым трем Кубитс в регистре.</span><span class="sxs-lookup"><span data-stu-id="53db0-105">Applies an operation to the first three qubits in the register.</span></span>
<span data-ttu-id="53db0-106">Модификатор `C` указывает, что операция является управляемой.</span><span class="sxs-lookup"><span data-stu-id="53db0-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToFirstThreeQubitsC (op : ((Qubit, Qubit, Qubit) => Unit is Ctl), register : Qubit[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="53db0-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="53db0-107">Input</span></span>

### <a name="op--qubitqubitqubit--unit--is-ctl"></a><span data-ttu-id="53db0-108">Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit)) = [модуль](xref:microsoft.quantum.lang-ref.unit) > является CTL</span><span class="sxs-lookup"><span data-stu-id="53db0-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="53db0-109">Операция, применяемая к первым трем Кубитс</span><span class="sxs-lookup"><span data-stu-id="53db0-109">An operation to be applied to the first three qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="53db0-110">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="53db0-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="53db0-111">Массив кубит к первым трем Кубитс, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="53db0-111">Qubit array to the first three qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="53db0-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="53db0-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="53db0-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53db0-113">Remarks</span></span>

<span data-ttu-id="53db0-114">Это соответствует следующей записи:</span><span class="sxs-lookup"><span data-stu-id="53db0-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1], register[2]);
```

## <a name="see-also"></a><span data-ttu-id="53db0-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="53db0-115">See Also</span></span>

- [<span data-ttu-id="53db0-116">Microsoft. тактов. Canon. Апплитофирстсрикубитс</span><span class="sxs-lookup"><span data-stu-id="53db0-116">Microsoft.Quantum.Canon.ApplyToFirstThreeQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubits)