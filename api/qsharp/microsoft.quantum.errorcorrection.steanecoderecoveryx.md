---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX
title: Функция Стеанекодерековерикс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryX
qsharp.summary: Decoder for the X-part of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: c90eac291ebe718d10377399184ad705bb51673e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98824704"
---
# <a name="steanecoderecoveryx-function"></a><span data-ttu-id="083d8-102">Функция Стеанекодерековерикс</span><span class="sxs-lookup"><span data-stu-id="083d8-102">SteaneCodeRecoveryX function</span></span>

<span data-ttu-id="083d8-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="083d8-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="083d8-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="083d8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="083d8-105">Декодер для X-части группы стабилизер ⟦ 7, 1, 3 ⟧ Стеане.</span><span class="sxs-lookup"><span data-stu-id="083d8-105">Decoder for the X-part of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.</span></span>

```qsharp
function SteaneCodeRecoveryX (syndrome : Microsoft.Quantum.ErrorCorrection.Syndrome) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="083d8-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="083d8-106">Input</span></span>

### <a name="syndrome--syndrome"></a><span data-ttu-id="083d8-107">синдром: [синдром](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span><span class="sxs-lookup"><span data-stu-id="083d8-107">syndrome : [Syndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span></span>

<span data-ttu-id="083d8-108">Массив синдром, полученный из измерения X-части стабилизер.</span><span class="sxs-lookup"><span data-stu-id="083d8-108">A syndrome array obtained from measuring the X-part of the stabilizer.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="083d8-109">Выходные данные: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="083d8-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="083d8-110">Массив операций Паули, которые при применении к закодированной тактовой системе исправляет ошибку, соответствующую `syndrome` .</span><span class="sxs-lookup"><span data-stu-id="083d8-110">An array of Pauli operations which, when applied to the encoded quantum system corrects the error corresponding to `syndrome`.</span></span>

## <a name="remarks"></a><span data-ttu-id="083d8-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="083d8-111">Remarks</span></span>

<span data-ttu-id="083d8-112">Выбранный декодер использует свойство кода CSS ⟦ 7, 1, 3 ⟧ Стеане Code, т. е. оно корректирует X Errors и Z Errors отдельно.</span><span class="sxs-lookup"><span data-stu-id="083d8-112">The chosen decoder uses the CSS code property of the ⟦7, 1, 3⟧ Steane code, i.e., it corrects X errors and Z errors separately.</span></span> <span data-ttu-id="083d8-113">Свойство кода заключается в том, что положение X, соответственно, с коррекцией Z, которое должно применяться, — это 3-разрядная кодировка X, соответственно, Z синдром, когда считается целым числом.</span><span class="sxs-lookup"><span data-stu-id="083d8-113">A property of the code is that the location of the X, respectively, Z correction to be applied is the 3-bit encoding of the X, respectively, Z syndrome when considered an integer.</span></span>

## <a name="references"></a><span data-ttu-id="083d8-114">Ссылки</span><span class="sxs-lookup"><span data-stu-id="083d8-114">References</span></span>

- <span data-ttu-id="083d8-115">Г.</span><span class="sxs-lookup"><span data-stu-id="083d8-115">D.</span></span> <span data-ttu-id="083d8-116">Готтесман, «Стабилизер коды и исправление ошибок такта», «степень Ph.d. гипотеза», Калтеч, 1997; https://arxiv.org/abs/quant-ph/9705052</span><span class="sxs-lookup"><span data-stu-id="083d8-116">Gottesman, "Stabilizer Codes and Quantum Error Correction," Ph.D. Thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052</span></span>

## <a name="see-also"></a><span data-ttu-id="083d8-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="083d8-117">See Also</span></span>

- [<span data-ttu-id="083d8-118">Microsoft. тактов. Ерроркорректион. Стеанекодерековерикс</span><span class="sxs-lookup"><span data-stu-id="083d8-118">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [<span data-ttu-id="083d8-119">Microsoft. тактов. Ерроркорректион. Стеанекодерековерифнс</span><span class="sxs-lookup"><span data-stu-id="083d8-119">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns)