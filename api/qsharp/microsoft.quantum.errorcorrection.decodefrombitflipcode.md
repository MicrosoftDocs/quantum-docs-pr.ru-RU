---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromBitFlipCode
title: Операция Декодефромбитфлипкоде
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromBitFlipCode
qsharp.summary: Decodes from the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.
ms.openlocfilehash: b16e84340053b6c1eab7b91ed8db0461b9eac98e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827566"
---
# <a name="decodefrombitflipcode-operation"></a><span data-ttu-id="ab379-102">Операция Декодефромбитфлипкоде</span><span class="sxs-lookup"><span data-stu-id="ab379-102">DecodeFromBitFlipCode operation</span></span>

<span data-ttu-id="ab379-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="ab379-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="ab379-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ab379-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ab379-105">Декодирования из кода [3, 1, 3]/⟦ 3, 1, 1 ⟧ bit-переворот Code.</span><span class="sxs-lookup"><span data-stu-id="ab379-105">Decodes from the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.</span></span>

```qsharp
operation DecodeFromBitFlipCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a><span data-ttu-id="ab379-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ab379-106">Input</span></span>

### <a name="logicalregister--logicalregister"></a><span data-ttu-id="ab379-107">Логикалрегистер: [логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="ab379-107">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="ab379-108">Блок кода побитового отражения.</span><span class="sxs-lookup"><span data-stu-id="ab379-108">A code block of the bit-flip code.</span></span>



## <a name="output--qubitqubit"></a><span data-ttu-id="ab379-109">Выходные данные: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[])</span><span class="sxs-lookup"><span data-stu-id="ab379-109">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span></span>

<span data-ttu-id="ab379-110">Кортеж данных, закодированных в логическую регистрацию, и вспомогательный Кубитс, используемый для представления синдром.</span><span class="sxs-lookup"><span data-stu-id="ab379-110">A tuple of the data encoded into the logical register, and the auxiliary qubits used to represent the syndrome.</span></span>

## <a name="see-also"></a><span data-ttu-id="ab379-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="ab379-111">See Also</span></span>

- [<span data-ttu-id="ab379-112">Microsoft. тактов. Ерроркорректион. Логикалрегистер</span><span class="sxs-lookup"><span data-stu-id="ab379-112">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [<span data-ttu-id="ab379-113">Microsoft. тактов. Ерроркорректион. Енкодеинтобитфлипкоде</span><span class="sxs-lookup"><span data-stu-id="ab379-113">Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode</span></span>](xref:Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode)