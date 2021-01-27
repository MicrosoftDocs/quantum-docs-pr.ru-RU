---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitA
title: Операция Апплитофирсткубита
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitA
qsharp.summary: Applies an operation to the first qubit in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 2f96c2a8ed31d295bc127c568e0ca24c267638b5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841446"
---
# <a name="applytofirstqubita-operation"></a><span data-ttu-id="3e9fe-102">Операция Апплитофирсткубита</span><span class="sxs-lookup"><span data-stu-id="3e9fe-102">ApplyToFirstQubitA operation</span></span>

<span data-ttu-id="3e9fe-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3e9fe-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3e9fe-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3e9fe-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3e9fe-105">Применяет операцию к первому кубиту в регистре.</span><span class="sxs-lookup"><span data-stu-id="3e9fe-105">Applies an operation to the first qubit in the register.</span></span>
<span data-ttu-id="3e9fe-106">Модификатор `A` указывает, что операция является аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="3e9fe-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToFirstQubitA (op : (Qubit => Unit is Adj), register : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="3e9fe-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3e9fe-107">Input</span></span>

### <a name="op--qubit--unit--is-adj"></a><span data-ttu-id="3e9fe-108">Op: [кубит](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  — это прогода</span><span class="sxs-lookup"><span data-stu-id="3e9fe-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="3e9fe-109">Операция, применяемая к первому кубит</span><span class="sxs-lookup"><span data-stu-id="3e9fe-109">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="3e9fe-110">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="3e9fe-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="3e9fe-111">Массив кубит к первому кубит, к которому применяется операция</span><span class="sxs-lookup"><span data-stu-id="3e9fe-111">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="3e9fe-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3e9fe-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="3e9fe-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="3e9fe-113">See Also</span></span>

- [<span data-ttu-id="3e9fe-114">Microsoft. тактов. Canon. Апплитофирсткубит</span><span class="sxs-lookup"><span data-stu-id="3e9fe-114">Microsoft.Quantum.Canon.ApplyToFirstQubit</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)