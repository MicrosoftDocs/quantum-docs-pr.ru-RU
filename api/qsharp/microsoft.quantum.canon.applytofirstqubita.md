---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitA
title: Операция Апплитофирсткубита
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitA
qsharp.summary: Applies an operation to the first qubit in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 00dbff0b562f90653c8569589e838f11e6c938e8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717400"
---
# <a name="applytofirstqubita-operation"></a><span data-ttu-id="ebe52-102">Операция Апплитофирсткубита</span><span class="sxs-lookup"><span data-stu-id="ebe52-102">ApplyToFirstQubitA operation</span></span>

<span data-ttu-id="ebe52-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ebe52-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ebe52-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ebe52-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ebe52-105">Применяет операцию к первому кубиту в регистре.</span><span class="sxs-lookup"><span data-stu-id="ebe52-105">Applies an operation to the first qubit in the register.</span></span>
<span data-ttu-id="ebe52-106">Модификатор `A` указывает, что операция является аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="ebe52-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToFirstQubitA (op : (Qubit => Unit is Adj), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="ebe52-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ebe52-107">Input</span></span>

### <a name="op--qubit--unit-adj"></a><span data-ttu-id="ebe52-108">Op: [кубит](xref:microsoft.quantum.lang-ref.qubit) => [единицы измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ebe52-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="ebe52-109">Операция, применяемая к первому кубит</span><span class="sxs-lookup"><span data-stu-id="ebe52-109">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="ebe52-110">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ebe52-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="ebe52-111">Массив кубит к первому кубит, к которому применяется операция</span><span class="sxs-lookup"><span data-stu-id="ebe52-111">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="ebe52-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ebe52-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="ebe52-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="ebe52-113">See Also</span></span>

- [<span data-ttu-id="ebe52-114">Microsoft. тактов. Canon. Апплитофирсткубит</span><span class="sxs-lookup"><span data-stu-id="ebe52-114">Microsoft.Quantum.Canon.ApplyToFirstQubit</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)