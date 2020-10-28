---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCode
title: Функция Стеанекоде
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCode
qsharp.summary: Returns a CSS value representing the ⟦7, 1, 3⟧ Steane code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: ea36320fff1f0c24426e2fcead976ef051d6699f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712178"
---
# <a name="steanecode-function"></a><span data-ttu-id="e985d-102">Функция Стеанекоде</span><span class="sxs-lookup"><span data-stu-id="e985d-102">SteaneCode function</span></span>

<span data-ttu-id="e985d-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="e985d-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="e985d-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e985d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e985d-105">Возвращает значение CSS, представляющее кодировщик кода ⟦ 7, 1, 3 ⟧ Стеане и декодер с измерением синдром на месте.</span><span class="sxs-lookup"><span data-stu-id="e985d-105">Returns a CSS value representing the ⟦7, 1, 3⟧ Steane code encoder and decoder with in-place syndrome measurement.</span></span>

```qsharp
function SteaneCode () : Microsoft.Quantum.ErrorCorrection.CSS
```


## <a name="output--css"></a><span data-ttu-id="e985d-106">Выходные данные: [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span><span class="sxs-lookup"><span data-stu-id="e985d-106">Output : [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span></span>

<span data-ttu-id="e985d-107">Объект типа CSS, который собирает все релевантные данные для выполнения кодирования и исправления ошибок для ⟦ 7, 1, 3 ⟧ Стеане Code.</span><span class="sxs-lookup"><span data-stu-id="e985d-107">An object of CSS type which collects all relevant data to perform encoding and error correction for the ⟦7, 1, 3⟧ Steane code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e985d-108">Remarks</span><span class="sxs-lookup"><span data-stu-id="e985d-108">Remarks</span></span>

<span data-ttu-id="e985d-109">Этот код был найден в следующем документе:</span><span class="sxs-lookup"><span data-stu-id="e985d-109">This code was found in the following paper:</span></span>

- <span data-ttu-id="e985d-110">А.</span><span class="sxs-lookup"><span data-stu-id="e985d-110">A.</span></span> <span data-ttu-id="e985d-111">Стеане, "множественные помехи частиц и исправление ошибок такта", proc.</span><span class="sxs-lookup"><span data-stu-id="e985d-111">Steane, "Multiple Particle Interference and Quantum Error Correction", Proc.</span></span> <span data-ttu-id="e985d-112">Рой.</span><span class="sxs-lookup"><span data-stu-id="e985d-112">Roy.</span></span> <span data-ttu-id="e985d-113">SoC. Лонд.</span><span class="sxs-lookup"><span data-stu-id="e985d-113">Soc. Lond.</span></span> <span data-ttu-id="e985d-114">A452 (1996) pp. 2551; https://arxiv.org/abs/quant-ph/9601029.</span><span class="sxs-lookup"><span data-stu-id="e985d-114">A452 (1996) pp. 2551; https://arxiv.org/abs/quant-ph/9601029.</span></span>