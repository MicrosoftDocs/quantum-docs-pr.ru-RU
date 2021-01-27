---
uid: Microsoft.Quantum.Diagnostics.AssertAllZeroWithinTolerance
title: Операция Ассерталлзеровисинтолеранце
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertAllZeroWithinTolerance
qsharp.summary: Assert that given qubits are all in $\ket{0}$ state up to a given tolerance.
ms.openlocfilehash: 281855ec79d280c903ebb4d05614081767840778
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830861"
---
# <a name="assertallzerowithintolerance-operation"></a><span data-ttu-id="a7dc3-102">Операция Ассерталлзеровисинтолеранце</span><span class="sxs-lookup"><span data-stu-id="a7dc3-102">AssertAllZeroWithinTolerance operation</span></span>

<span data-ttu-id="a7dc3-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="a7dc3-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="a7dc3-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="a7dc3-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="a7dc3-105">Утверждение о том, что все заданные Кубитс находятся в состоянии $ \кет {0} $ вплоть до заданного допуска.</span><span class="sxs-lookup"><span data-stu-id="a7dc3-105">Assert that given qubits are all in $\ket{0}$ state up to a given tolerance.</span></span>

```qsharp
operation AssertAllZeroWithinTolerance (qubits : Qubit[], tolerance : Double) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="a7dc3-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a7dc3-106">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="a7dc3-107">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a7dc3-107">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a7dc3-108">Кубитс, которые подтверждаются в $ \кет {0} $ State.</span><span class="sxs-lookup"><span data-stu-id="a7dc3-108">Qubits that are asserted to be in $\ket{0}$ state.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="a7dc3-109">Допуск: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a7dc3-109">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="a7dc3-110">Точность, с которой состояние должно находиться в $ \кет {0} $ State</span><span class="sxs-lookup"><span data-stu-id="a7dc3-110">Accuracy with which the state should be in $\ket{0}$ state</span></span>



## <a name="output--unit"></a><span data-ttu-id="a7dc3-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a7dc3-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="a7dc3-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="a7dc3-112">See Also</span></span>

- [<span data-ttu-id="a7dc3-113">Microsoft. тактов. Diagnostics. Ассерткубитвисинтолеранце</span><span class="sxs-lookup"><span data-stu-id="a7dc3-113">Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance)