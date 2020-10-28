---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX
title: Функция Стеанекодерековерикс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryX
qsharp.summary: Decoder for the X-part of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 0f6b987ca23bd9ff2076080d60f1ca756b36848e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712135"
---
# <a name="steanecoderecoveryx-function"></a><span data-ttu-id="104d6-102">Функция Стеанекодерековерикс</span><span class="sxs-lookup"><span data-stu-id="104d6-102">SteaneCodeRecoveryX function</span></span>

<span data-ttu-id="104d6-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="104d6-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="104d6-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="104d6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="104d6-105">Декодер для X-части группы стабилизер ⟦ 7, 1, 3 ⟧ Стеане.</span><span class="sxs-lookup"><span data-stu-id="104d6-105">Decoder for the X-part of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.</span></span>

```qsharp
function SteaneCodeRecoveryX (syndrome : Microsoft.Quantum.ErrorCorrection.Syndrome) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="104d6-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="104d6-106">Input</span></span>

### <a name="syndrome--syndrome"></a><span data-ttu-id="104d6-107">синдром: [синдром](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span><span class="sxs-lookup"><span data-stu-id="104d6-107">syndrome : [Syndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span></span>

<span data-ttu-id="104d6-108">Массив синдром, полученный из измерения X-части стабилизер.</span><span class="sxs-lookup"><span data-stu-id="104d6-108">A syndrome array obtained from measuring the X-part of the stabilizer.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="104d6-109">Выходные данные: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="104d6-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="104d6-110">Массив операций Паули, которые при применении к закодированной тактовой системе исправляет ошибку, соответствующую `syndrome` .</span><span class="sxs-lookup"><span data-stu-id="104d6-110">An array of Pauli operations which, when applied to the encoded quantum system corrects the error corresponding to `syndrome`.</span></span>

## <a name="remarks"></a><span data-ttu-id="104d6-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="104d6-111">Remarks</span></span>

<span data-ttu-id="104d6-112">Выбранный декодер использует свойство кода CSS ⟦ 7, 1, 3 ⟧ Стеане Code, т. е. оно корректирует X Errors и Z Errors отдельно.</span><span class="sxs-lookup"><span data-stu-id="104d6-112">The chosen decoder uses the CSS code property of the ⟦7, 1, 3⟧ Steane code, i.e., it corrects X errors and Z errors separately.</span></span> <span data-ttu-id="104d6-113">Свойство кода заключается в том, что положение X, соответственно, с коррекцией Z, которое должно применяться, — это 3-разрядная кодировка X, соответственно, Z синдром, когда считается целым числом.</span><span class="sxs-lookup"><span data-stu-id="104d6-113">A property of the code is that the location of the X, respectively, Z correction to be applied is the 3-bit encoding of the X, respectively, Z syndrome when considered an integer.</span></span>

## <a name="references"></a><span data-ttu-id="104d6-114">Ссылки</span><span class="sxs-lookup"><span data-stu-id="104d6-114">References</span></span>

- <span data-ttu-id="104d6-115">Г.</span><span class="sxs-lookup"><span data-stu-id="104d6-115">D.</span></span> <span data-ttu-id="104d6-116">Готтесман, «Стабилизер коды и исправление ошибок такта», «степень Ph.d. гипотеза», Калтеч, 1997; https://arxiv.org/abs/quant-ph/9705052</span><span class="sxs-lookup"><span data-stu-id="104d6-116">Gottesman, "Stabilizer Codes and Quantum Error Correction," Ph.D. Thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052</span></span>

## <a name="see-also"></a><span data-ttu-id="104d6-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="104d6-117">See Also</span></span>

- [<span data-ttu-id="104d6-118">Microsoft. тактов. Ерроркорректион. Стеанекодерековерикс</span><span class="sxs-lookup"><span data-stu-id="104d6-118">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [<span data-ttu-id="104d6-119">Microsoft. тактов. Ерроркорректион. Стеанекодерековерифнс</span><span class="sxs-lookup"><span data-stu-id="104d6-119">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns)