---
uid: Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsA
title: Операция Апплитофирстсрикубитса
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstThreeQubitsA
qsharp.summary: Applies an operation to the first three qubits in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 7c464b1decb5a30a996dfc1df9f1f1921613c73e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841413"
---
# <a name="applytofirstthreequbitsa-operation"></a><span data-ttu-id="39856-102">Операция Апплитофирстсрикубитса</span><span class="sxs-lookup"><span data-stu-id="39856-102">ApplyToFirstThreeQubitsA operation</span></span>

<span data-ttu-id="39856-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="39856-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="39856-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="39856-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="39856-105">Применяет операцию к первым трем Кубитс в регистре.</span><span class="sxs-lookup"><span data-stu-id="39856-105">Applies an operation to the first three qubits in the register.</span></span>
<span data-ttu-id="39856-106">Модификатор `A` указывает, что операция является аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="39856-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToFirstThreeQubitsA (op : ((Qubit, Qubit, Qubit) => Unit is Adj), register : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="39856-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="39856-107">Input</span></span>

### <a name="op--qubitqubitqubit--unit--is-adj"></a><span data-ttu-id="39856-108">Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit),[кубит](xref:microsoft.quantum.lang-ref.qubit)) => [единица](xref:microsoft.quantum.lang-ref.unit)  в сумме</span><span class="sxs-lookup"><span data-stu-id="39856-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="39856-109">Операция, применяемая к первым трем Кубитс</span><span class="sxs-lookup"><span data-stu-id="39856-109">An operation to be applied to the first three qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="39856-110">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="39856-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="39856-111">Массив кубит к первым трем Кубитс, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="39856-111">Qubit array to the first three qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="39856-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="39856-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="39856-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="39856-113">Remarks</span></span>

<span data-ttu-id="39856-114">Это соответствует следующей записи:</span><span class="sxs-lookup"><span data-stu-id="39856-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1], register[2]);
```

## <a name="see-also"></a><span data-ttu-id="39856-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="39856-115">See Also</span></span>

- [<span data-ttu-id="39856-116">Microsoft. тактов. Canon. Апплитофирстсрикубитс</span><span class="sxs-lookup"><span data-stu-id="39856-116">Microsoft.Quantum.Canon.ApplyToFirstThreeQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubits)