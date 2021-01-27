---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCode
title: Функция Фивекубиткоде
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCode
qsharp.summary: Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: 540dcf1eafa7449f386676a9a3c9562a4d4bf29c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853136"
---
# <a name="fivequbitcode-function"></a><span data-ttu-id="9ecf9-102">Функция Фивекубиткоде</span><span class="sxs-lookup"><span data-stu-id="9ecf9-102">FiveQubitCode function</span></span>

<span data-ttu-id="9ecf9-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="9ecf9-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="9ecf9-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9ecf9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9ecf9-105">Возвращает значение КЕКК, представляющее ⟦ 5, 1, 3 ⟧ кодировщика кода и декодер с измерением синдром "на месте".</span><span class="sxs-lookup"><span data-stu-id="9ecf9-105">Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.</span></span>

```qsharp
function FiveQubitCode () : Microsoft.Quantum.ErrorCorrection.QECC
```


## <a name="output--qecc"></a><span data-ttu-id="9ecf9-106">Выходные данные: [кекк](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span><span class="sxs-lookup"><span data-stu-id="9ecf9-106">Output : [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span></span>

<span data-ttu-id="9ecf9-107">Возвращает реализацию кода исправления ошибки такта путем указания `QECC` типа.</span><span class="sxs-lookup"><span data-stu-id="9ecf9-107">Returns an implementation of a quantum error correction code by specifying a `QECC` type.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ecf9-108">Remarks</span><span class="sxs-lookup"><span data-stu-id="9ecf9-108">Remarks</span></span>

<span data-ttu-id="9ecf9-109">Этот код был найден независимо в следующих двух документах:</span><span class="sxs-lookup"><span data-stu-id="9ecf9-109">This code was found independently in the following two papers:</span></span>

- <span data-ttu-id="9ecf9-110">В.</span><span class="sxs-lookup"><span data-stu-id="9ecf9-110">C.</span></span> <span data-ttu-id="9ecf9-111">З.</span><span class="sxs-lookup"><span data-stu-id="9ecf9-111">H.</span></span> <span data-ttu-id="9ecf9-112">Беннет, D. Дивинцензо, J. A.</span><span class="sxs-lookup"><span data-stu-id="9ecf9-112">Bennett, D. DiVincenzo, J. A.</span></span> <span data-ttu-id="9ecf9-113">Смолин и W. K.</span><span class="sxs-lookup"><span data-stu-id="9ecf9-113">Smolin and W. K.</span></span> <span data-ttu-id="9ecf9-114">Вуттерс, "смешанное состояние замкнутые и исправление ошибок такта", "инвентаризационная. Rev. A, 54 (1996) pp. 3824-3851; https://arxiv.org/abs/quant-ph/9604024 и</span><span class="sxs-lookup"><span data-stu-id="9ecf9-114">Wootters, "Mixed state entanglement and quantum error correction," Phys. Rev. A, 54 (1996) pp. 3824-3851; https://arxiv.org/abs/quant-ph/9604024 and</span></span>
- <span data-ttu-id="9ecf9-115">Ф.</span><span class="sxs-lookup"><span data-stu-id="9ecf9-115">R.</span></span> <span data-ttu-id="9ecf9-116">ЛаФламме, C. Микуел, J. P.</span><span class="sxs-lookup"><span data-stu-id="9ecf9-116">Laflamme, C. Miquel, J. P.</span></span> <span data-ttu-id="9ecf9-117">Пас и W. H.</span><span class="sxs-lookup"><span data-stu-id="9ecf9-117">Paz and W. H.</span></span> <span data-ttu-id="9ecf9-118">Зурек, «отличный код исправления тактовой ошибки», «инвентаризационная. Rev. Летт.</span><span class="sxs-lookup"><span data-stu-id="9ecf9-118">Zurek, "Perfect quantum error correction code," Phys. Rev. Lett.</span></span> <span data-ttu-id="9ecf9-119">77 (1996) pp. 198-201; https://arxiv.org/abs/quant-ph/9602019</span><span class="sxs-lookup"><span data-stu-id="9ecf9-119">77 (1996) pp. 198-201; https://arxiv.org/abs/quant-ph/9602019</span></span>