---
uid: Microsoft.Quantum.Diagnostics.AssertAllZeroWithinTolerance
title: Операция Ассерталлзеровисинтолеранце
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertAllZeroWithinTolerance
qsharp.summary: Assert that given qubits are all in $\ket{0}$ state up to a given tolerance.
ms.openlocfilehash: 5e401904086323fabef7914d34463f50e4c38862
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713045"
---
# <a name="assertallzerowithintolerance-operation"></a><span data-ttu-id="76d9b-102">Операция Ассерталлзеровисинтолеранце</span><span class="sxs-lookup"><span data-stu-id="76d9b-102">AssertAllZeroWithinTolerance operation</span></span>

<span data-ttu-id="76d9b-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="76d9b-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="76d9b-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="76d9b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="76d9b-105">Утверждение о том, что все заданные Кубитс находятся в состоянии $ \кет {0} $ вплоть до заданного допуска.</span><span class="sxs-lookup"><span data-stu-id="76d9b-105">Assert that given qubits are all in $\ket{0}$ state up to a given tolerance.</span></span>

```qsharp
operation AssertAllZeroWithinTolerance (qubits : Qubit[], tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="76d9b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="76d9b-106">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="76d9b-107">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="76d9b-107">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="76d9b-108">Кубитс, которые подтверждаются в $ \кет {0} $ State.</span><span class="sxs-lookup"><span data-stu-id="76d9b-108">Qubits that are asserted to be in $\ket{0}$ state.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="76d9b-109">Допуск: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="76d9b-109">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="76d9b-110">Точность, с которой состояние должно находиться в $ \кет {0} $ State</span><span class="sxs-lookup"><span data-stu-id="76d9b-110">Accuracy with which the state should be in $\ket{0}$ state</span></span>



## <a name="output--unit"></a><span data-ttu-id="76d9b-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="76d9b-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="76d9b-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="76d9b-112">See Also</span></span>

- [<span data-ttu-id="76d9b-113">Microsoft. тактов. Diagnostics. Ассерткубитвисинтолеранце</span><span class="sxs-lookup"><span data-stu-id="76d9b-113">Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance)