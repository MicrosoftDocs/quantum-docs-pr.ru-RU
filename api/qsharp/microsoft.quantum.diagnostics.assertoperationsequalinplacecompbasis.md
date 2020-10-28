---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlaceCompBasis
title: Операция Ассертоператионсекуалинплацекомпбасис
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualInPlaceCompBasis
qsharp.summary: Checks if the operation `givenU` is equal to the operation `expectedU` on the given input size  by checking the action of the operations only on the vectors from the computational basis. This is a necessary, but not sufficient, condition for the equality of two unitaries.
ms.openlocfilehash: 3275680f86ca2a178c7f044b97d226fe41c3186c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712962"
---
# <a name="assertoperationsequalinplacecompbasis-operation"></a><span data-ttu-id="62165-102">Операция Ассертоператионсекуалинплацекомпбасис</span><span class="sxs-lookup"><span data-stu-id="62165-102">AssertOperationsEqualInPlaceCompBasis operation</span></span>

<span data-ttu-id="62165-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="62165-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="62165-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="62165-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="62165-105">Проверяет, равен ли операция `givenU` операции `expectedU` с заданным размером входных данных, проверяя действие операций только на векторах от вычислительной основе.</span><span class="sxs-lookup"><span data-stu-id="62165-105">Checks if the operation `givenU` is equal to the operation `expectedU` on the given input size  by checking the action of the operations only on the vectors from the computational basis.</span></span>
<span data-ttu-id="62165-106">Это обязательное, но недостаточное условие для равенства двух унитариес.</span><span class="sxs-lookup"><span data-stu-id="62165-106">This is a necessary, but not sufficient, condition for the equality of two unitaries.</span></span>

```qsharp
operation AssertOperationsEqualInPlaceCompBasis (nQubits : Int, givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="62165-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="62165-107">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="62165-108">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="62165-108">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="62165-109">Число Кубитс $n $, с которыми работают операции `givenU` `expectedU` .</span><span class="sxs-lookup"><span data-stu-id="62165-109">The number of qubits $n$ that the operations `givenU` and `expectedU` operate on.</span></span>


### <a name="givenu--qubit--unit"></a><span data-ttu-id="62165-110">Гивену: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="62165-110">givenU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="62165-111">Операция с $n $ Кубитс будет проверена.</span><span class="sxs-lookup"><span data-stu-id="62165-111">Operation on $n$ qubits to be checked.</span></span>


### <a name="expectedu--qubit--unit-adj"></a><span data-ttu-id="62165-112">Експектеду: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="62165-112">expectedU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="62165-113">Операция ссылки на $n $ Кубитс `givenU` для сравнения с.</span><span class="sxs-lookup"><span data-stu-id="62165-113">Reference operation on $n$ qubits that `givenU` is to be compared against.</span></span>



## <a name="output--unit"></a><span data-ttu-id="62165-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="62165-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

