---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromBitFlipCode
title: Операция Декодефромбитфлипкоде
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromBitFlipCode
qsharp.summary: Decodes from the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.
ms.openlocfilehash: be6ad5fce9eeb3eea031ff301b78dbb3680b66f0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712485"
---
# <a name="decodefrombitflipcode-operation"></a><span data-ttu-id="538b3-102">Операция Декодефромбитфлипкоде</span><span class="sxs-lookup"><span data-stu-id="538b3-102">DecodeFromBitFlipCode operation</span></span>

<span data-ttu-id="538b3-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="538b3-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="538b3-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="538b3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="538b3-105">Декодирования из кода [3, 1, 3]/⟦ 3, 1, 1 ⟧ bit-переворот Code.</span><span class="sxs-lookup"><span data-stu-id="538b3-105">Decodes from the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.</span></span>

```qsharp
operation DecodeFromBitFlipCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a><span data-ttu-id="538b3-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="538b3-106">Input</span></span>

### <a name="logicalregister--logicalregister"></a><span data-ttu-id="538b3-107">Логикалрегистер: [логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="538b3-107">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="538b3-108">Блок кода побитового отражения.</span><span class="sxs-lookup"><span data-stu-id="538b3-108">A code block of the bit-flip code.</span></span>



## <a name="output--qubitqubit"></a><span data-ttu-id="538b3-109">Выходные данные: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[])</span><span class="sxs-lookup"><span data-stu-id="538b3-109">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span></span>

<span data-ttu-id="538b3-110">Кортеж данных, закодированных в логическую регистрацию, и вспомогательный Кубитс, используемый для представления синдром.</span><span class="sxs-lookup"><span data-stu-id="538b3-110">A tuple of the data encoded into the logical register, and the auxiliary qubits used to represent the syndrome.</span></span>

## <a name="see-also"></a><span data-ttu-id="538b3-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="538b3-111">See Also</span></span>

- [<span data-ttu-id="538b3-112">Microsoft. тактов. Ерроркорректион. Логикалрегистер</span><span class="sxs-lookup"><span data-stu-id="538b3-112">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [<span data-ttu-id="538b3-113">Microsoft. тактов. Ерроркорректион. Енкодеинтобитфлипкоде</span><span class="sxs-lookup"><span data-stu-id="538b3-113">Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode</span></span>](xref:Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode)