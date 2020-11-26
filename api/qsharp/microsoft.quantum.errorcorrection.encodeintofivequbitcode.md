---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoFiveQubitCode
title: Операция Енкодеинтофивекубиткоде
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoFiveQubitCode
qsharp.summary: Encodes into the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 70e52b7440dca1fa8761db13d6187cb6bf8c43c4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200991"
---
# <a name="encodeintofivequbitcode-operation"></a><span data-ttu-id="f541b-102">Операция Енкодеинтофивекубиткоде</span><span class="sxs-lookup"><span data-stu-id="f541b-102">EncodeIntoFiveQubitCode operation</span></span>

<span data-ttu-id="f541b-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="f541b-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="f541b-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f541b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f541b-105">Кодирует в код такта ⟦ 5, 1, 3 ⟧.</span><span class="sxs-lookup"><span data-stu-id="f541b-105">Encodes into the ⟦5, 1, 3⟧ quantum code.</span></span>

```qsharp
operation EncodeIntoFiveQubitCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a><span data-ttu-id="f541b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f541b-106">Input</span></span>

### <a name="physregister--qubit"></a><span data-ttu-id="f541b-107">Фисрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f541b-107">physRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f541b-108">Кубит, представляющий незакодированное состояние.</span><span class="sxs-lookup"><span data-stu-id="f541b-108">A qubit representing an unencoded state.</span></span> <span data-ttu-id="f541b-109">Длина этого массива равна `Qubit[]` 1.</span><span class="sxs-lookup"><span data-stu-id="f541b-109">This array `Qubit[]` is of length 1.</span></span>


### <a name="auxqubits--qubit"></a><span data-ttu-id="f541b-110">Аукскубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f541b-110">auxQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f541b-111">Регистр вспомогательных Кубитс, которые будут использоваться для представления закодированного состояния.</span><span class="sxs-lookup"><span data-stu-id="f541b-111">A register of auxiliary qubits that will be used to represent the encoded state.</span></span>



## <a name="output--logicalregister"></a><span data-ttu-id="f541b-112">Выходные данные: [логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="f541b-112">Output : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="f541b-113">Массив физического Кубитс типа `LogicalRegister` , который хранит закодированное состояние.</span><span class="sxs-lookup"><span data-stu-id="f541b-113">An array of physical qubits of type `LogicalRegister` that store the encoded state.</span></span>

## <a name="see-also"></a><span data-ttu-id="f541b-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="f541b-114">See Also</span></span>

- [<span data-ttu-id="f541b-115">Microsoft. тактов. Ерроркорректион. Логикалрегистер</span><span class="sxs-lookup"><span data-stu-id="f541b-115">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)