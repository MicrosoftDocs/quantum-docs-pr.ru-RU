---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromSteaneCode
title: Операция Декодефромстеанекоде
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromSteaneCode
qsharp.summary: An inverse encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: e6831a8630c0a80c2abe7c4a720263f0de03edc4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712416"
---
# <a name="decodefromsteanecode-operation"></a><span data-ttu-id="24502-102">Операция Декодефромстеанекоде</span><span class="sxs-lookup"><span data-stu-id="24502-102">DecodeFromSteaneCode operation</span></span>

<span data-ttu-id="24502-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="24502-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="24502-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="24502-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="24502-105">Операция обратной кодировки, которая сопоставляет незакодированный регистр такта с закодированным регистром такта в коде такта ⟦ 7, 1, 3 ⟧ Стеане.</span><span class="sxs-lookup"><span data-stu-id="24502-105">An inverse encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.</span></span>

```qsharp
operation DecodeFromSteaneCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a><span data-ttu-id="24502-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="24502-106">Input</span></span>

### <a name="logicalregister--logicalregister"></a><span data-ttu-id="24502-107">Логикалрегистер: [логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="24502-107">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="24502-108">Массив Кубитс, представляющий закодированное 5-кубит логическое состояние кода.</span><span class="sxs-lookup"><span data-stu-id="24502-108">An array of qubits representing the encoded 5-qubit code logical state.</span></span>



## <a name="output--qubitqubit"></a><span data-ttu-id="24502-109">Выходные данные: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[])</span><span class="sxs-lookup"><span data-stu-id="24502-109">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span></span>

<span data-ttu-id="24502-110">Массив кубит с длиной 1, представляющий незакодированное состояние в первом параметре вместе с вспомогательным Кубитс во втором параметре.</span><span class="sxs-lookup"><span data-stu-id="24502-110">A qubit array of length 1 representing the unencoded state in the first parameter, together with auxiliary qubits in the second parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="24502-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="24502-111">Remarks</span></span>

<span data-ttu-id="24502-112">Выбранный декодер использует свойство кода CSS ⟦ 7, 1, 3 ⟧ Стеане Code, т. е. оно корректирует X Errors и Z Errors отдельно.</span><span class="sxs-lookup"><span data-stu-id="24502-112">The chosen decoder uses the CSS code property of the ⟦7, 1, 3⟧ Steane code, i.e., it corrects X errors and Z errors separately.</span></span> <span data-ttu-id="24502-113">Свойство кода заключается в том, что положение X, соответственно, с коррекцией Z, которое должно применяться, — это 3-разрядная кодировка X, соответственно, Z синдром, когда считается целым числом.</span><span class="sxs-lookup"><span data-stu-id="24502-113">A property of the code is that the location of the X, respectively, Z correction to be applied is the 3-bit encoding of the X, respectively, Z syndrome when considered an integer.</span></span>

## <a name="references"></a><span data-ttu-id="24502-114">Ссылки</span><span class="sxs-lookup"><span data-stu-id="24502-114">References</span></span>

- <span data-ttu-id="24502-115">Г.</span><span class="sxs-lookup"><span data-stu-id="24502-115">D.</span></span> <span data-ttu-id="24502-116">Готтесман, «Стабилизер коды и исправление ошибок такта», «степень Ph.d. гипотеза», Калтеч, 1997; https://arxiv.org/abs/quant-ph/9705052</span><span class="sxs-lookup"><span data-stu-id="24502-116">Gottesman, "Stabilizer Codes and Quantum Error Correction," Ph.D. Thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052</span></span>

## <a name="see-also"></a><span data-ttu-id="24502-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="24502-117">See Also</span></span>

- [<span data-ttu-id="24502-118">Microsoft. тактов. Ерроркорректион. Стеанекодинкодер</span><span class="sxs-lookup"><span data-stu-id="24502-118">Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoder</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoder)
- [<span data-ttu-id="24502-119">Microsoft. тактов. Ерроркорректион. Стеанекодедекодер</span><span class="sxs-lookup"><span data-stu-id="24502-119">Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder)
- [<span data-ttu-id="24502-120">Microsoft. тактов. Ерроркорректион. Логикалрегистер</span><span class="sxs-lookup"><span data-stu-id="24502-120">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)