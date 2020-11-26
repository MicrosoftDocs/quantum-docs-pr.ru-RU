---
uid: Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp
title: Определяемый пользователем тип Синдромемеасоп
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SyndromeMeasOp
qsharp.summary: Represents an operation that is used to measure the syndrome of an error-correcting code block.
ms.openlocfilehash: 65e47d82546b1df0beec2c00f435d3e7a28e6ae6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200260"
---
# <a name="syndromemeasop-user-defined-type"></a><span data-ttu-id="e8090-102">Определяемый пользователем тип Синдромемеасоп</span><span class="sxs-lookup"><span data-stu-id="e8090-102">SyndromeMeasOp user defined type</span></span>

<span data-ttu-id="e8090-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="e8090-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="e8090-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e8090-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e8090-105">Представляет операцию, используемую для измерения синдром блока кода исправления ошибок.</span><span class="sxs-lookup"><span data-stu-id="e8090-105">Represents an operation that is used to measure the syndrome of an error-correcting code block.</span></span>

```qsharp

newtype SyndromeMeasOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => Microsoft.Quantum.ErrorCorrection.Syndrome));
```



## <a name="remarks"></a><span data-ttu-id="e8090-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8090-106">Remarks</span></span>

<span data-ttu-id="e8090-107">Подпись `(LogicalRegister => Syndrome)` представляет операцию, которая взаимодействует с Кубитс в `LogicalRegister` и некоторыми дополнительными Кубитс, за которыми следуют измерения вспомогательного Кубитс для извлечения `Syndrome` значения, представляющего `Result[]` эти измерения.</span><span class="sxs-lookup"><span data-stu-id="e8090-107">The signature `(LogicalRegister => Syndrome)` represents an operation that acts jointly on the qubits in `LogicalRegister` and some auxiliary qubits followed by a measurements of the auxiliary qubits to extract a `Syndrome` value representing the `Result[]` of these measurements.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8090-108">См. также:</span><span class="sxs-lookup"><span data-stu-id="e8090-108">See Also</span></span>

- [<span data-ttu-id="e8090-109">Microsoft. тактов. Ерроркорректион. Логикалрегистер</span><span class="sxs-lookup"><span data-stu-id="e8090-109">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [<span data-ttu-id="e8090-110">Microsoft. тактов. Ерроркорректион. синдром</span><span class="sxs-lookup"><span data-stu-id="e8090-110">Microsoft.Quantum.ErrorCorrection.Syndrome</span></span>](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)