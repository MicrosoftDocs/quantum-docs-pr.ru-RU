---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitC
title: Операция Апплитофирсткубитк
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitC
qsharp.summary: Applies operation op to the first qubit in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 2659c3a97baa68cb4c1d7781381f89742902594d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217515"
---
# <a name="applytofirstqubitc-operation"></a><span data-ttu-id="afd6f-102">Операция Апплитофирсткубитк</span><span class="sxs-lookup"><span data-stu-id="afd6f-102">ApplyToFirstQubitC operation</span></span>

<span data-ttu-id="afd6f-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="afd6f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="afd6f-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="afd6f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="afd6f-105">Применяет Op операции к первому кубит в регистре.</span><span class="sxs-lookup"><span data-stu-id="afd6f-105">Applies operation op to the first qubit in the register.</span></span>
<span data-ttu-id="afd6f-106">Модификатор `C` указывает, что операция является управляемой.</span><span class="sxs-lookup"><span data-stu-id="afd6f-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToFirstQubitC (op : (Qubit => Unit is Ctl), register : Qubit[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="afd6f-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="afd6f-107">Input</span></span>

### <a name="op--qubit--unit--is-ctl"></a><span data-ttu-id="afd6f-108">Op: [кубит](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  — CTL</span><span class="sxs-lookup"><span data-stu-id="afd6f-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="afd6f-109">Операция, применяемая к первому кубит</span><span class="sxs-lookup"><span data-stu-id="afd6f-109">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="afd6f-110">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="afd6f-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="afd6f-111">Массив кубит к первому кубит, к которому применяется операция</span><span class="sxs-lookup"><span data-stu-id="afd6f-111">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="afd6f-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="afd6f-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="afd6f-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="afd6f-113">See Also</span></span>

- [<span data-ttu-id="afd6f-114">Microsoft. тактов. Canon. Апплитофирсткубит</span><span class="sxs-lookup"><span data-stu-id="afd6f-114">Microsoft.Quantum.Canon.ApplyToFirstQubit</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)