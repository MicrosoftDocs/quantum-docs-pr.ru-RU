---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromFiveQubitCode
title: Операция Декодефромфивекубиткоде
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromFiveQubitCode
qsharp.summary: Decodes the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 421da6296b604f30aefed58730091f64f19c3a61
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712471"
---
# <a name="decodefromfivequbitcode-operation"></a><span data-ttu-id="51de7-102">Операция Декодефромфивекубиткоде</span><span class="sxs-lookup"><span data-stu-id="51de7-102">DecodeFromFiveQubitCode operation</span></span>

<span data-ttu-id="51de7-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="51de7-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="51de7-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="51de7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="51de7-105">Декодирует код такта ⟦ 5, 1, 3 ⟧.</span><span class="sxs-lookup"><span data-stu-id="51de7-105">Decodes the ⟦5, 1, 3⟧ quantum code.</span></span>

```qsharp
operation DecodeFromFiveQubitCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a><span data-ttu-id="51de7-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="51de7-106">Input</span></span>

### <a name="logicalregister--logicalregister"></a><span data-ttu-id="51de7-107">Логикалрегистер: [логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="51de7-107">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="51de7-108">Массив Кубитс, представляющий закодированное 5-кубит логическое состояние кода.</span><span class="sxs-lookup"><span data-stu-id="51de7-108">An array of qubits representing the encoded 5-qubit code logical state.</span></span>



## <a name="output--qubitqubit"></a><span data-ttu-id="51de7-109">Выходные данные: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[])</span><span class="sxs-lookup"><span data-stu-id="51de7-109">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span></span>

<span data-ttu-id="51de7-110">Массив кубит с длиной 1, представляющий незакодированное состояние в первом параметре вместе с вспомогательным Кубитс во втором параметре.</span><span class="sxs-lookup"><span data-stu-id="51de7-110">A qubit array of length 1 representing the unencoded state in the first parameter, together with auxiliary qubits in the second parameter.</span></span>

## <a name="see-also"></a><span data-ttu-id="51de7-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="51de7-111">See Also</span></span>

- [<span data-ttu-id="51de7-112">Microsoft. тактов. Ерроркорректион. Фивекубиткодинкодер</span><span class="sxs-lookup"><span data-stu-id="51de7-112">Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoder</span></span>](xref:Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoder)
- [<span data-ttu-id="51de7-113">Microsoft. тактов. Ерроркорректион. Логикалрегистер</span><span class="sxs-lookup"><span data-stu-id="51de7-113">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)