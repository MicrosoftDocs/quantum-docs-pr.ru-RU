---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitCA
title: Операция Апплитофирсткубитка
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitCA
qsharp.summary: Applies operation op to the first qubit in the register. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: ba82199cc7a548d771027141780873c05de71c57
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841431"
---
# <a name="applytofirstqubitca-operation"></a><span data-ttu-id="0d13f-102">Операция Апплитофирсткубитка</span><span class="sxs-lookup"><span data-stu-id="0d13f-102">ApplyToFirstQubitCA operation</span></span>

<span data-ttu-id="0d13f-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0d13f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0d13f-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0d13f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0d13f-105">Применяет Op операции к первому кубит в регистре.</span><span class="sxs-lookup"><span data-stu-id="0d13f-105">Applies operation op to the first qubit in the register.</span></span>
<span data-ttu-id="0d13f-106">Модификатор `CA` указывает, что операция является управляемой и аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="0d13f-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToFirstQubitCA (op : (Qubit => Unit is Adj + Ctl), register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="0d13f-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0d13f-107">Input</span></span>

### <a name="op--qubit--unit--is-adj--ctl"></a><span data-ttu-id="0d13f-108">Op: [](xref:microsoft.quantum.lang-ref.qubit) => [единица](xref:microsoft.quantum.lang-ref.unit) кубит — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="0d13f-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="0d13f-109">Операция, применяемая к первому кубит</span><span class="sxs-lookup"><span data-stu-id="0d13f-109">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="0d13f-110">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="0d13f-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="0d13f-111">Массив кубит к первому кубит, к которому применяется операция</span><span class="sxs-lookup"><span data-stu-id="0d13f-111">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="0d13f-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0d13f-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="0d13f-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="0d13f-113">See Also</span></span>

- [<span data-ttu-id="0d13f-114">Microsoft. тактов. Canon. Апплитофирсткубит</span><span class="sxs-lookup"><span data-stu-id="0d13f-114">Microsoft.Quantum.Canon.ApplyToFirstQubit</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)