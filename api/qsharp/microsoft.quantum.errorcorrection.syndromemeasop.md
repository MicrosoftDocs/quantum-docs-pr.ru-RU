---
uid: Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp
title: Определяемый пользователем тип Синдромемеасоп
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SyndromeMeasOp
qsharp.summary: Represents an operation that is used to measure the syndrome of an error-correcting code block.
ms.openlocfilehash: 1314e16d26c7310bab21caa91cb398d4b6f09b29
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712121"
---
# <a name="syndromemeasop-user-defined-type"></a><span data-ttu-id="e5551-102">Определяемый пользователем тип Синдромемеасоп</span><span class="sxs-lookup"><span data-stu-id="e5551-102">SyndromeMeasOp user defined type</span></span>

<span data-ttu-id="e5551-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="e5551-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="e5551-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e5551-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e5551-105">Представляет операцию, используемую для измерения синдром блока кода исправления ошибок.</span><span class="sxs-lookup"><span data-stu-id="e5551-105">Represents an operation that is used to measure the syndrome of an error-correcting code block.</span></span>

```qsharp

newtype SyndromeMeasOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => Microsoft.Quantum.ErrorCorrection.Syndrome));
```



## <a name="remarks"></a><span data-ttu-id="e5551-106">Remarks</span><span class="sxs-lookup"><span data-stu-id="e5551-106">Remarks</span></span>

<span data-ttu-id="e5551-107">Подпись `(LogicalRegister => Syndrome)` представляет операцию, которая взаимодействует с Кубитс в `LogicalRegister` и некоторыми дополнительными Кубитс, за которыми следуют измерения вспомогательного Кубитс для извлечения `Syndrome` значения, представляющего `Result[]` эти измерения.</span><span class="sxs-lookup"><span data-stu-id="e5551-107">The signature `(LogicalRegister => Syndrome)` represents an operation that acts jointly on the qubits in `LogicalRegister` and some auxiliary qubits followed by a measurements of the auxiliary qubits to extract a `Syndrome` value representing the `Result[]` of these measurements.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5551-108">См. также:</span><span class="sxs-lookup"><span data-stu-id="e5551-108">See Also</span></span>

- [<span data-ttu-id="e5551-109">Microsoft. тактов. Ерроркорректион. Логикалрегистер</span><span class="sxs-lookup"><span data-stu-id="e5551-109">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [<span data-ttu-id="e5551-110">Microsoft. тактов. Ерроркорректион. синдром</span><span class="sxs-lookup"><span data-stu-id="e5551-110">Microsoft.Quantum.ErrorCorrection.Syndrome</span></span>](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)