---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoSteaneCode
title: Операция Енкодеинтостеанекоде
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoSteaneCode
qsharp.summary: An encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 39b8ab549413d9d5281f6b84a6e970c45242fca8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712388"
---
# <a name="encodeintosteanecode-operation"></a><span data-ttu-id="20e00-102">Операция Енкодеинтостеанекоде</span><span class="sxs-lookup"><span data-stu-id="20e00-102">EncodeIntoSteaneCode operation</span></span>

<span data-ttu-id="20e00-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="20e00-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="20e00-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="20e00-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="20e00-105">Операция кодирования, которая сопоставляет незакодированный регистр такта с закодированным регистром такта в коде такта ⟦ 7, 1, 3 ⟧ Стеане.</span><span class="sxs-lookup"><span data-stu-id="20e00-105">An encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.</span></span>

```qsharp
operation EncodeIntoSteaneCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a><span data-ttu-id="20e00-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="20e00-106">Input</span></span>

### <a name="physregister--qubit"></a><span data-ttu-id="20e00-107">Фисрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="20e00-107">physRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="20e00-108">Регистр кубит, который содержит незакодированное состояние такта</span><span class="sxs-lookup"><span data-stu-id="20e00-108">A qubit register which holds the an unencoded quantum state</span></span>


### <a name="auxqubits--qubit"></a><span data-ttu-id="20e00-109">Аукскубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="20e00-109">auxQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="20e00-110">Регистр кубит, который изначально равен нулю и добавляется в тактовую систему, чтобы можно было выполнить операцию кодирования.</span><span class="sxs-lookup"><span data-stu-id="20e00-110">A qubit register which is initially zero and which gets added to the quantum system so that an encoding operation can be performed</span></span>



## <a name="output--logicalregister"></a><span data-ttu-id="20e00-111">Выходные данные: [логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="20e00-111">Output : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="20e00-112">Регистр такта, удерживающий состояние после применения кодировщика Стеане</span><span class="sxs-lookup"><span data-stu-id="20e00-112">A quantum register holding the state after the Steane encoder has been applied</span></span>

## <a name="see-also"></a><span data-ttu-id="20e00-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="20e00-113">See Also</span></span>

- [<span data-ttu-id="20e00-114">Microsoft. тактов. Ерроркорректион. Логикалрегистер</span><span class="sxs-lookup"><span data-stu-id="20e00-114">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [<span data-ttu-id="20e00-115">Microsoft. тактов. Ерроркорректион. Стеанекодедекодер</span><span class="sxs-lookup"><span data-stu-id="20e00-115">Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder)