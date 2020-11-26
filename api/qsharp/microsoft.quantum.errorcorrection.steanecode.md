---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCode
title: Функция Стеанекоде
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCode
qsharp.summary: Returns a CSS value representing the ⟦7, 1, 3⟧ Steane code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: b981c82acfa82cd58d82666703d4bb95ac5df280
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200481"
---
# <a name="steanecode-function"></a><span data-ttu-id="d24da-102">Функция Стеанекоде</span><span class="sxs-lookup"><span data-stu-id="d24da-102">SteaneCode function</span></span>

<span data-ttu-id="d24da-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="d24da-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="d24da-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d24da-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d24da-105">Возвращает значение CSS, представляющее кодировщик кода ⟦ 7, 1, 3 ⟧ Стеане и декодер с измерением синдром на месте.</span><span class="sxs-lookup"><span data-stu-id="d24da-105">Returns a CSS value representing the ⟦7, 1, 3⟧ Steane code encoder and decoder with in-place syndrome measurement.</span></span>

```qsharp
function SteaneCode () : Microsoft.Quantum.ErrorCorrection.CSS
```


## <a name="output--css"></a><span data-ttu-id="d24da-106">Выходные данные: [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span><span class="sxs-lookup"><span data-stu-id="d24da-106">Output : [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span></span>

<span data-ttu-id="d24da-107">Объект типа CSS, который собирает все релевантные данные для выполнения кодирования и исправления ошибок для ⟦ 7, 1, 3 ⟧ Стеане Code.</span><span class="sxs-lookup"><span data-stu-id="d24da-107">An object of CSS type which collects all relevant data to perform encoding and error correction for the ⟦7, 1, 3⟧ Steane code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d24da-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d24da-108">Remarks</span></span>

<span data-ttu-id="d24da-109">Этот код был найден в следующем документе:</span><span class="sxs-lookup"><span data-stu-id="d24da-109">This code was found in the following paper:</span></span>

- <span data-ttu-id="d24da-110">A.</span><span class="sxs-lookup"><span data-stu-id="d24da-110">A.</span></span> <span data-ttu-id="d24da-111">Стеане, "множественные помехи частиц и исправление ошибок такта", proc.</span><span class="sxs-lookup"><span data-stu-id="d24da-111">Steane, "Multiple Particle Interference and Quantum Error Correction", Proc.</span></span> <span data-ttu-id="d24da-112">Рой.</span><span class="sxs-lookup"><span data-stu-id="d24da-112">Roy.</span></span> <span data-ttu-id="d24da-113">SoC. Лонд.</span><span class="sxs-lookup"><span data-stu-id="d24da-113">Soc. Lond.</span></span> <span data-ttu-id="d24da-114">A452 (1996) pp. 2551; https://arxiv.org/abs/quant-ph/9601029.</span><span class="sxs-lookup"><span data-stu-id="d24da-114">A452 (1996) pp. 2551; https://arxiv.org/abs/quant-ph/9601029.</span></span>