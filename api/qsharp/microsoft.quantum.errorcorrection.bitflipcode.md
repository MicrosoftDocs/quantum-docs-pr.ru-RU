---
uid: Microsoft.Quantum.ErrorCorrection.BitFlipCode
title: Функция Битфлипкоде
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: BitFlipCode
qsharp.summary: Returns a QECC value representing the ⟦3, 1, 1⟧ bit flip code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: 8d4498647682026e9dec3fa96cfb69ba1e3214b6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712500"
---
# <a name="bitflipcode-function"></a><span data-ttu-id="27aee-102">Функция Битфлипкоде</span><span class="sxs-lookup"><span data-stu-id="27aee-102">BitFlipCode function</span></span>

<span data-ttu-id="27aee-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="27aee-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="27aee-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="27aee-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="27aee-105">Возвращает значение КЕКК, представляющее кодировщик ⟦ 3, 1, 1 ⟧ битного отражения кода и декодер с измерением синдром на месте.</span><span class="sxs-lookup"><span data-stu-id="27aee-105">Returns a QECC value representing the ⟦3, 1, 1⟧ bit flip code encoder and decoder with in-place syndrome measurement.</span></span>

```qsharp
function BitFlipCode () : Microsoft.Quantum.ErrorCorrection.QECC
```


## <a name="output--qecc"></a><span data-ttu-id="27aee-106">Выходные данные: [кекк](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span><span class="sxs-lookup"><span data-stu-id="27aee-106">Output : [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span></span>

<span data-ttu-id="27aee-107">Возвращает реализацию кода исправления ошибки такта путем указания `QECC` типа.</span><span class="sxs-lookup"><span data-stu-id="27aee-107">Returns an implementation of a quantum error correction code by specifying a `QECC` type.</span></span>