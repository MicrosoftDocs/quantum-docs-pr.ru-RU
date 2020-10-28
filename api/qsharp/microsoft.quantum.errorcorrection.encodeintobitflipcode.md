---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode
title: Операция Енкодеинтобитфлипкоде
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoBitFlipCode
qsharp.summary: Encodes into the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.
ms.openlocfilehash: 694d3f7a412b64b0ad533b4478a9274384d05c61
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712402"
---
# <a name="encodeintobitflipcode-operation"></a><span data-ttu-id="78c84-102">Операция Енкодеинтобитфлипкоде</span><span class="sxs-lookup"><span data-stu-id="78c84-102">EncodeIntoBitFlipCode operation</span></span>

<span data-ttu-id="78c84-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="78c84-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="78c84-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="78c84-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="78c84-105">Кодирует в код [3, 1, 3]/⟦ 3, 1, 1 ⟧ bit-переворот.</span><span class="sxs-lookup"><span data-stu-id="78c84-105">Encodes into the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.</span></span>

```qsharp
operation EncodeIntoBitFlipCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a><span data-ttu-id="78c84-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="78c84-106">Input</span></span>

### <a name="physregister--qubit"></a><span data-ttu-id="78c84-107">Фисрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="78c84-107">physRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="78c84-108">Регистр физических Кубитс, представляющих защищаемые данные.</span><span class="sxs-lookup"><span data-stu-id="78c84-108">A register of physical qubits representing the data to be protected.</span></span>


### <a name="auxqubits--qubit"></a><span data-ttu-id="78c84-109">Аукскубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="78c84-109">auxQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="78c84-110">Регистрация вспомогательных Кубитс изначально в состоянии $ \кет {00} $, которая используется для кодирования защищаемых данных.</span><span class="sxs-lookup"><span data-stu-id="78c84-110">A register of auxiliary qubits initially in the $\ket{00}$ state to be used in encoding the data to be protected.</span></span>



## <a name="output--logicalregister"></a><span data-ttu-id="78c84-111">Выходные данные: [логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="78c84-111">Output : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="78c84-112">Физические и вспомогательные Кубитс, используемые в кодировке, представленные в виде логического регистра.</span><span class="sxs-lookup"><span data-stu-id="78c84-112">The physical and auxiliary qubits used in encoding, represented as a logical register.</span></span>

## <a name="see-also"></a><span data-ttu-id="78c84-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="78c84-113">See Also</span></span>

- [<span data-ttu-id="78c84-114">Microsoft. тактов. Ерроркорректион. Логикалрегистер</span><span class="sxs-lookup"><span data-stu-id="78c84-114">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)