---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitC
title: Операция Апплитофирсткубитк
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitC
qsharp.summary: Applies operation op to the first qubit in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: e2c137ad4a8252731acf94d6f2343f8fd386b8e3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717413"
---
# <a name="applytofirstqubitc-operation"></a><span data-ttu-id="e7f3d-102">Операция Апплитофирсткубитк</span><span class="sxs-lookup"><span data-stu-id="e7f3d-102">ApplyToFirstQubitC operation</span></span>

<span data-ttu-id="e7f3d-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e7f3d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e7f3d-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e7f3d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e7f3d-105">Применяет Op операции к первому кубит в регистре.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-105">Applies operation op to the first qubit in the register.</span></span>
<span data-ttu-id="e7f3d-106">Модификатор `C` указывает, что операция является управляемой.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToFirstQubitC (op : (Qubit => Unit is Ctl), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="e7f3d-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e7f3d-107">Input</span></span>

### <a name="op--qubit--unit-ctl"></a><span data-ttu-id="e7f3d-108">Op: [кубит](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="e7f3d-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="e7f3d-109">Операция, применяемая к первому кубит</span><span class="sxs-lookup"><span data-stu-id="e7f3d-109">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="e7f3d-110">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="e7f3d-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e7f3d-111">Массив кубит к первому кубит, к которому применяется операция</span><span class="sxs-lookup"><span data-stu-id="e7f3d-111">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="e7f3d-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e7f3d-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="e7f3d-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="e7f3d-113">See Also</span></span>

- [<span data-ttu-id="e7f3d-114">Microsoft. тактов. Canon. Апплитофирсткубит</span><span class="sxs-lookup"><span data-stu-id="e7f3d-114">Microsoft.Quantum.Canon.ApplyToFirstQubit</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)