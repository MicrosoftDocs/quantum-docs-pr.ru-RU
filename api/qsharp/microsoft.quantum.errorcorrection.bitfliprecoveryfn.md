---
uid: Microsoft.Quantum.ErrorCorrection.BitFlipRecoveryFn
title: Функция Битфлипрековерифн
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: BitFlipRecoveryFn
qsharp.summary: Function for recovery Pauli operations for given syndrome measurement by table lookup for the ⟦3, 1, 1⟧ bit flip code.
ms.openlocfilehash: dad90475b2506187282825e143b11adc5120f453
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712499"
---
# <a name="bitfliprecoveryfn-function"></a><span data-ttu-id="88da8-102">Функция Битфлипрековерифн</span><span class="sxs-lookup"><span data-stu-id="88da8-102">BitFlipRecoveryFn function</span></span>

<span data-ttu-id="88da8-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="88da8-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="88da8-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="88da8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="88da8-105">Функция для операций восстановления Паули для заданного измерения синдром путем уточняющего запроса таблицы для ⟦ 3, 1, 1 ⟧ разрядного кода отражения.</span><span class="sxs-lookup"><span data-stu-id="88da8-105">Function for recovery Pauli operations for given syndrome measurement by table lookup for the ⟦3, 1, 1⟧ bit flip code.</span></span>

```qsharp
function BitFlipRecoveryFn () : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="output--recoveryfn"></a><span data-ttu-id="88da8-106">Выходные данные: [рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="88da8-106">Output : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="88da8-107">Функция типа `RecoveryFn` , которая принимает синдром измерение `Result[]` и возвращает `Pauli[]` операции, которые исправляет обнаруженную ошибку.</span><span class="sxs-lookup"><span data-stu-id="88da8-107">Function of type `RecoveryFn` that takes a syndrome measurement `Result[]` and returns the `Pauli[]` operations that corrects the detected error.</span></span>

## <a name="see-also"></a><span data-ttu-id="88da8-108">См. также:</span><span class="sxs-lookup"><span data-stu-id="88da8-108">See Also</span></span>

- [<span data-ttu-id="88da8-109">Microsoft. тактов. Ерроркорректион. Рековерифн</span><span class="sxs-lookup"><span data-stu-id="88da8-109">Microsoft.Quantum.ErrorCorrection.RecoveryFn</span></span>](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)