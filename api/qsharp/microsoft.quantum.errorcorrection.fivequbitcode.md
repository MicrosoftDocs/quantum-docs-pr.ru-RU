---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCode
title: Функция Фивекубиткоде
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCode
qsharp.summary: Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: 3b45af29897735905f7fe52340e2a8e425bd8cbe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200889"
---
# <a name="fivequbitcode-function"></a><span data-ttu-id="a3f6c-102">Функция Фивекубиткоде</span><span class="sxs-lookup"><span data-stu-id="a3f6c-102">FiveQubitCode function</span></span>

<span data-ttu-id="a3f6c-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="a3f6c-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="a3f6c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a3f6c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a3f6c-105">Возвращает значение КЕКК, представляющее ⟦ 5, 1, 3 ⟧ кодировщика кода и декодер с измерением синдром "на месте".</span><span class="sxs-lookup"><span data-stu-id="a3f6c-105">Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.</span></span>

```qsharp
function FiveQubitCode () : Microsoft.Quantum.ErrorCorrection.QECC
```


## <a name="output--qecc"></a><span data-ttu-id="a3f6c-106">Выходные данные: [кекк](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span><span class="sxs-lookup"><span data-stu-id="a3f6c-106">Output : [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span></span>

<span data-ttu-id="a3f6c-107">Возвращает реализацию кода исправления ошибки такта путем указания `QECC` типа.</span><span class="sxs-lookup"><span data-stu-id="a3f6c-107">Returns an implementation of a quantum error correction code by specifying a `QECC` type.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3f6c-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3f6c-108">Remarks</span></span>

<span data-ttu-id="a3f6c-109">Этот код был найден независимо в следующих двух документах:</span><span class="sxs-lookup"><span data-stu-id="a3f6c-109">This code was found independently in the following two papers:</span></span>

- <span data-ttu-id="a3f6c-110">В.</span><span class="sxs-lookup"><span data-stu-id="a3f6c-110">C.</span></span> <span data-ttu-id="a3f6c-111">З.</span><span class="sxs-lookup"><span data-stu-id="a3f6c-111">H.</span></span> <span data-ttu-id="a3f6c-112">Беннет, D. Дивинцензо, J. A.</span><span class="sxs-lookup"><span data-stu-id="a3f6c-112">Bennett, D. DiVincenzo, J. A.</span></span> <span data-ttu-id="a3f6c-113">Смолин и W. K.</span><span class="sxs-lookup"><span data-stu-id="a3f6c-113">Smolin and W. K.</span></span> <span data-ttu-id="a3f6c-114">Вуттерс, "смешанное состояние замкнутые и исправление ошибок такта", "инвентаризационная. Rev. A, 54 (1996) pp. 3824-3851; https://arxiv.org/abs/quant-ph/9604024 и</span><span class="sxs-lookup"><span data-stu-id="a3f6c-114">Wootters, "Mixed state entanglement and quantum error correction," Phys. Rev. A, 54 (1996) pp. 3824-3851; https://arxiv.org/abs/quant-ph/9604024 and</span></span>
- <span data-ttu-id="a3f6c-115">Ф.</span><span class="sxs-lookup"><span data-stu-id="a3f6c-115">R.</span></span> <span data-ttu-id="a3f6c-116">ЛаФламме, C. Микуел, J. P.</span><span class="sxs-lookup"><span data-stu-id="a3f6c-116">Laflamme, C. Miquel, J. P.</span></span> <span data-ttu-id="a3f6c-117">Пас и W. H.</span><span class="sxs-lookup"><span data-stu-id="a3f6c-117">Paz and W. H.</span></span> <span data-ttu-id="a3f6c-118">Зурек, «отличный код исправления тактовой ошибки», «инвентаризационная. Rev. Летт.</span><span class="sxs-lookup"><span data-stu-id="a3f6c-118">Zurek, "Perfect quantum error correction code," Phys. Rev. Lett.</span></span> <span data-ttu-id="a3f6c-119">77 (1996) pp. 198-201; https://arxiv.org/abs/quant-ph/9602019</span><span class="sxs-lookup"><span data-stu-id="a3f6c-119">77 (1996) pp. 198-201; https://arxiv.org/abs/quant-ph/9602019</span></span>