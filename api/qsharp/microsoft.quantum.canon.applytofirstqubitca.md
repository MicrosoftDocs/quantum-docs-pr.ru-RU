---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitCA
title: Операция Апплитофирсткубитка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitCA
qsharp.summary: Applies operation op to the first qubit in the register. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 2e1db23ad819a85df99a826f406d9b0fbcc7a175
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717399"
---
# <a name="applytofirstqubitca-operation"></a><span data-ttu-id="5c264-102">Операция Апплитофирсткубитка</span><span class="sxs-lookup"><span data-stu-id="5c264-102">ApplyToFirstQubitCA operation</span></span>

<span data-ttu-id="5c264-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5c264-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5c264-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5c264-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5c264-105">Применяет Op операции к первому кубит в регистре.</span><span class="sxs-lookup"><span data-stu-id="5c264-105">Applies operation op to the first qubit in the register.</span></span>
<span data-ttu-id="5c264-106">Модификатор `CA` указывает, что операция является управляемой и аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="5c264-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToFirstQubitCA (op : (Qubit => Unit is Adj + Ctl), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="5c264-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5c264-107">Input</span></span>

### <a name="op--qubit--unit-adj--ctl"></a><span data-ttu-id="5c264-108">Op: [кубит](xref:microsoft.quantum.lang-ref.qubit) => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="5c264-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="5c264-109">Операция, применяемая к первому кубит</span><span class="sxs-lookup"><span data-stu-id="5c264-109">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="5c264-110">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="5c264-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="5c264-111">Массив кубит к первому кубит, к которому применяется операция</span><span class="sxs-lookup"><span data-stu-id="5c264-111">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="5c264-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5c264-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="5c264-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="5c264-113">See Also</span></span>

- [<span data-ttu-id="5c264-114">Microsoft. тактов. Canon. Апплитофирсткубит</span><span class="sxs-lookup"><span data-stu-id="5c264-114">Microsoft.Quantum.Canon.ApplyToFirstQubit</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)