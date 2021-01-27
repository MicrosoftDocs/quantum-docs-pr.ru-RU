---
uid: Microsoft.Quantum.Diagnostics._assertEqualOnBasisVector
title: _assertEqualOnBasisVector операция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _assertEqualOnBasisVector
qsharp.summary: Checks if the result of applying two operations `givenU` and `expectedU` to a basis state is the same. The basis state is described by `basis` parameter. See <xref:microsoft.quantum.extensions.fliptobasis> function for more details on this description.
ms.openlocfilehash: 041fecfa27ae5bd17fa8fdc89ce964f985f6124b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853586"
---
# <a name="_assertequalonbasisvector-operation"></a><span data-ttu-id="b6aeb-102">_assertEqualOnBasisVector операция</span><span class="sxs-lookup"><span data-stu-id="b6aeb-102">_assertEqualOnBasisVector operation</span></span>

<span data-ttu-id="b6aeb-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="b6aeb-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="b6aeb-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="b6aeb-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="b6aeb-105">Проверяет, совпадает ли результат применения двух операций `givenU` и `expectedU` с состоянием основания.</span><span class="sxs-lookup"><span data-stu-id="b6aeb-105">Checks if the result of applying two operations `givenU` and `expectedU` to a basis state is the same.</span></span> <span data-ttu-id="b6aeb-106">Состояние основания описывается `basis` параметром.</span><span class="sxs-lookup"><span data-stu-id="b6aeb-106">The basis state is described by `basis` parameter.</span></span>
<span data-ttu-id="b6aeb-107"><xref:microsoft.quantum.extensions.fliptobasis>Дополнительные сведения об этом описании см. в разделе функция.</span><span class="sxs-lookup"><span data-stu-id="b6aeb-107">See <xref:microsoft.quantum.extensions.fliptobasis> function for more details on this description.</span></span>

```qsharp
operation _assertEqualOnBasisVector (basis : Int[], givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="b6aeb-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b6aeb-108">Input</span></span>

### <a name="basis--int"></a><span data-ttu-id="b6aeb-109">Базис: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="b6aeb-109">basis : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="b6aeb-110">Состояние основания, заданное ИДЕНТИФИКАТОРом однокубитного состояния (0 <= ID <= 3) для каждого из $n $ Кубитс.</span><span class="sxs-lookup"><span data-stu-id="b6aeb-110">Basis state specified by a single-qubit basis state ID (0 <= id <= 3) for each of $n$ qubits.</span></span>


### <a name="givenu--qubit--unit"></a><span data-ttu-id="b6aeb-111">Гивену: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="b6aeb-111">givenU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="b6aeb-112">Операция с $n $ Кубитс будет проверена.</span><span class="sxs-lookup"><span data-stu-id="b6aeb-112">Operation on $n$ qubits to be checked.</span></span>


### <a name="expectedu--qubit--unit--is-adj"></a><span data-ttu-id="b6aeb-113">Експектеду: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit) ></span><span class="sxs-lookup"><span data-stu-id="b6aeb-113">expectedU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="b6aeb-114">Операция ссылки на $n $ Кубитс, для которой требуется сравнить Гивену.</span><span class="sxs-lookup"><span data-stu-id="b6aeb-114">Reference operation on $n$ qubits that givenU is to be compared against.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b6aeb-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b6aeb-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

