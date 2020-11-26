---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns
title: Функция Стеанекодерековерифнс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryFns
qsharp.summary: Decoder for combined X- and Z-parts of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 7395996e75c5a1c0c5d13f76d9ec76acae5683c7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200413"
---
# <a name="steanecoderecoveryfns-function"></a><span data-ttu-id="baabd-102">Функция Стеанекодерековерифнс</span><span class="sxs-lookup"><span data-stu-id="baabd-102">SteaneCodeRecoveryFns function</span></span>

<span data-ttu-id="baabd-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="baabd-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="baabd-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="baabd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="baabd-105">Декодер для Объединенных X-и Z-частей стабилизер группы ⟦ 7, 1, 3 ⟧ Стеане.</span><span class="sxs-lookup"><span data-stu-id="baabd-105">Decoder for combined X- and Z-parts of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.</span></span>

```qsharp
function SteaneCodeRecoveryFns () : (Microsoft.Quantum.ErrorCorrection.RecoveryFn, Microsoft.Quantum.ErrorCorrection.RecoveryFn)
```


## <a name="output--recoveryfnrecoveryfn"></a><span data-ttu-id="baabd-106">Выходные данные: ([рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn),[рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn))</span><span class="sxs-lookup"><span data-stu-id="baabd-106">Output : ([RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn),[RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn))</span></span>

<span data-ttu-id="baabd-107">Кортеж функций типа `RecoveryFn` , принимающий измерение синдром `Result[]` и возвращающий `Pauli[]` операции, которые исправляет обнаруженную ошибку.</span><span class="sxs-lookup"><span data-stu-id="baabd-107">Tuple of functions of type `RecoveryFn` that takes a syndrome measurement `Result[]` and returns the `Pauli[]` operations that corrects the detected error.</span></span>

## <a name="see-also"></a><span data-ttu-id="baabd-108">См. также:</span><span class="sxs-lookup"><span data-stu-id="baabd-108">See Also</span></span>

- [<span data-ttu-id="baabd-109">Microsoft. тактов. Ерроркорректион. Стеанекодерековерикс</span><span class="sxs-lookup"><span data-stu-id="baabd-109">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [<span data-ttu-id="baabd-110">Microsoft. тактов. Ерроркорректион. Стеанекодерековериз</span><span class="sxs-lookup"><span data-stu-id="baabd-110">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryZ</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryZ)