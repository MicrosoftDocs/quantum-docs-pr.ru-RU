---
uid: Microsoft.Quantum.ErrorCorrection.BitFlipRecoveryFn
title: Функция Битфлипрековерифн
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: BitFlipRecoveryFn
qsharp.summary: Function for recovery Pauli operations for given syndrome measurement by table lookup for the ⟦3, 1, 1⟧ bit flip code.
ms.openlocfilehash: 1cf2bd944b4dcaadeeca96fa0f576250590962e0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827594"
---
# <a name="bitfliprecoveryfn-function"></a><span data-ttu-id="995ec-102">Функция Битфлипрековерифн</span><span class="sxs-lookup"><span data-stu-id="995ec-102">BitFlipRecoveryFn function</span></span>

<span data-ttu-id="995ec-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="995ec-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="995ec-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="995ec-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="995ec-105">Функция для операций восстановления Паули для заданного измерения синдром путем уточняющего запроса таблицы для ⟦ 3, 1, 1 ⟧ разрядного кода отражения.</span><span class="sxs-lookup"><span data-stu-id="995ec-105">Function for recovery Pauli operations for given syndrome measurement by table lookup for the ⟦3, 1, 1⟧ bit flip code.</span></span>

```qsharp
function BitFlipRecoveryFn () : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="output--recoveryfn"></a><span data-ttu-id="995ec-106">Выходные данные: [рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="995ec-106">Output : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="995ec-107">Функция типа `RecoveryFn` , которая принимает синдром измерение `Result[]` и возвращает `Pauli[]` операции, которые исправляет обнаруженную ошибку.</span><span class="sxs-lookup"><span data-stu-id="995ec-107">Function of type `RecoveryFn` that takes a syndrome measurement `Result[]` and returns the `Pauli[]` operations that corrects the detected error.</span></span>

## <a name="see-also"></a><span data-ttu-id="995ec-108">См. также:</span><span class="sxs-lookup"><span data-stu-id="995ec-108">See Also</span></span>

- [<span data-ttu-id="995ec-109">Microsoft. тактов. Ерроркорректион. Рековерифн</span><span class="sxs-lookup"><span data-stu-id="995ec-109">Microsoft.Quantum.ErrorCorrection.RecoveryFn</span></span>](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)