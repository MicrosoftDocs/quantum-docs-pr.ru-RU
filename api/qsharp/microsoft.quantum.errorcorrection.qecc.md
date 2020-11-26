---
uid: Microsoft.Quantum.ErrorCorrection.QECC
title: Определяемый пользователем тип КЕКК
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: QECC
qsharp.summary: Represents an error-correcting code as defined by its encoder, decoder, and syndrome measurement procedure.
ms.openlocfilehash: c0c20fa82988aad661579c6498fec47e77f0726a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200617"
---
# <a name="qecc-user-defined-type"></a><span data-ttu-id="89e8b-102">Определяемый пользователем тип КЕКК</span><span class="sxs-lookup"><span data-stu-id="89e8b-102">QECC user defined type</span></span>

<span data-ttu-id="89e8b-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="89e8b-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="89e8b-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="89e8b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="89e8b-105">Представляет код исправления ошибок в соответствии с определением процедуры измерения кодировщика, декодера и синдром.</span><span class="sxs-lookup"><span data-stu-id="89e8b-105">Represents an error-correcting code as defined by its encoder, decoder, and syndrome measurement procedure.</span></span>

```qsharp

newtype QECC = (Microsoft.Quantum.ErrorCorrection.EncodeOp, Microsoft.Quantum.ErrorCorrection.DecodeOp, Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp);
```

