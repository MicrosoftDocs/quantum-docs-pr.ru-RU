---
uid: Microsoft.Quantum.Diagnostics._assertEqualOnBasisVector
title: _assertEqualOnBasisVector операция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _assertEqualOnBasisVector
qsharp.summary: Checks if the result of applying two operations `givenU` and `expectedU` to a basis state is the same. The basis state is described by `basis` parameter. See <xref:microsoft.quantum.extensions.fliptobasis> function for more details on this description.
ms.openlocfilehash: 01b6d5aede102e47df86ea70d071d81eba1ade6f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713157"
---
# <a name="_assertequalonbasisvector-operation"></a><span data-ttu-id="33d06-102">_assertEqualOnBasisVector операция</span><span class="sxs-lookup"><span data-stu-id="33d06-102">_assertEqualOnBasisVector operation</span></span>

<span data-ttu-id="33d06-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="33d06-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="33d06-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="33d06-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="33d06-105">Проверяет, совпадает ли результат применения двух операций `givenU` и `expectedU` с состоянием основания.</span><span class="sxs-lookup"><span data-stu-id="33d06-105">Checks if the result of applying two operations `givenU` and `expectedU` to a basis state is the same.</span></span> <span data-ttu-id="33d06-106">Состояние основания описывается `basis` параметром.</span><span class="sxs-lookup"><span data-stu-id="33d06-106">The basis state is described by `basis` parameter.</span></span>
<span data-ttu-id="33d06-107"><xref:microsoft.quantum.extensions.fliptobasis>Дополнительные сведения об этом описании см. в разделе функция.</span><span class="sxs-lookup"><span data-stu-id="33d06-107">See <xref:microsoft.quantum.extensions.fliptobasis> function for more details on this description.</span></span>

```qsharp
operation _assertEqualOnBasisVector (basis : Int[], givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="33d06-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="33d06-108">Input</span></span>

### <a name="basis--int"></a><span data-ttu-id="33d06-109">Базис: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="33d06-109">basis : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="33d06-110">Состояние основания, заданное ИДЕНТИФИКАТОРом однокубитного состояния (0 <= ID <= 3) для каждого из $n $ Кубитс.</span><span class="sxs-lookup"><span data-stu-id="33d06-110">Basis state specified by a single-qubit basis state ID (0 <= id <= 3) for each of $n$ qubits.</span></span>


### <a name="givenu--qubit--unit"></a><span data-ttu-id="33d06-111">Гивену: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="33d06-111">givenU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="33d06-112">Операция с $n $ Кубитс будет проверена.</span><span class="sxs-lookup"><span data-stu-id="33d06-112">Operation on $n$ qubits to be checked.</span></span>


### <a name="expectedu--qubit--unit-adj"></a><span data-ttu-id="33d06-113">Експектеду: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="33d06-113">expectedU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="33d06-114">Операция ссылки на $n $ Кубитс, для которой требуется сравнить Гивену.</span><span class="sxs-lookup"><span data-stu-id="33d06-114">Reference operation on $n$ qubits that givenU is to be compared against.</span></span>



## <a name="output--unit"></a><span data-ttu-id="33d06-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="33d06-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

