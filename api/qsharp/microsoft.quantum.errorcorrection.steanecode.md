---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCode
title: Функция Стеанекоде
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCode
qsharp.summary: Returns a CSS value representing the ⟦7, 1, 3⟧ Steane code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: af3f3ef5088b898bd827ebca00fdc7fcb992f2a1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853056"
---
# <a name="steanecode-function"></a><span data-ttu-id="96bc0-102">Функция Стеанекоде</span><span class="sxs-lookup"><span data-stu-id="96bc0-102">SteaneCode function</span></span>

<span data-ttu-id="96bc0-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="96bc0-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="96bc0-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="96bc0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="96bc0-105">Возвращает значение CSS, представляющее кодировщик кода ⟦ 7, 1, 3 ⟧ Стеане и декодер с измерением синдром на месте.</span><span class="sxs-lookup"><span data-stu-id="96bc0-105">Returns a CSS value representing the ⟦7, 1, 3⟧ Steane code encoder and decoder with in-place syndrome measurement.</span></span>

```qsharp
function SteaneCode () : Microsoft.Quantum.ErrorCorrection.CSS
```


## <a name="output--css"></a><span data-ttu-id="96bc0-106">Выходные данные: [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span><span class="sxs-lookup"><span data-stu-id="96bc0-106">Output : [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span></span>

<span data-ttu-id="96bc0-107">Объект типа CSS, который собирает все релевантные данные для выполнения кодирования и исправления ошибок для ⟦ 7, 1, 3 ⟧ Стеане Code.</span><span class="sxs-lookup"><span data-stu-id="96bc0-107">An object of CSS type which collects all relevant data to perform encoding and error correction for the ⟦7, 1, 3⟧ Steane code.</span></span>

## <a name="remarks"></a><span data-ttu-id="96bc0-108">Remarks</span><span class="sxs-lookup"><span data-stu-id="96bc0-108">Remarks</span></span>

<span data-ttu-id="96bc0-109">Этот код был найден в следующем документе:</span><span class="sxs-lookup"><span data-stu-id="96bc0-109">This code was found in the following paper:</span></span>

- <span data-ttu-id="96bc0-110">A.</span><span class="sxs-lookup"><span data-stu-id="96bc0-110">A.</span></span> <span data-ttu-id="96bc0-111">Стеане, "множественные помехи частиц и исправление ошибок такта", proc.</span><span class="sxs-lookup"><span data-stu-id="96bc0-111">Steane, "Multiple Particle Interference and Quantum Error Correction", Proc.</span></span> <span data-ttu-id="96bc0-112">Рой.</span><span class="sxs-lookup"><span data-stu-id="96bc0-112">Roy.</span></span> <span data-ttu-id="96bc0-113">SoC. Лонд.</span><span class="sxs-lookup"><span data-stu-id="96bc0-113">Soc. Lond.</span></span> <span data-ttu-id="96bc0-114">A452 (1996) pp. 2551; https://arxiv.org/abs/quant-ph/9601029.</span><span class="sxs-lookup"><span data-stu-id="96bc0-114">A452 (1996) pp. 2551; https://arxiv.org/abs/quant-ph/9601029.</span></span>