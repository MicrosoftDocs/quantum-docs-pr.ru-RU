---
uid: Microsoft.Quantum.ErrorCorrection.BitFlipCode
title: Функция Битфлипкоде
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: BitFlipCode
qsharp.summary: Returns a QECC value representing the ⟦3, 1, 1⟧ bit flip code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: 0a5a028f85b80575b754b93a797a1460d21bb552
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853190"
---
# <a name="bitflipcode-function"></a><span data-ttu-id="7241a-102">Функция Битфлипкоде</span><span class="sxs-lookup"><span data-stu-id="7241a-102">BitFlipCode function</span></span>

<span data-ttu-id="7241a-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="7241a-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="7241a-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7241a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7241a-105">Возвращает значение КЕКК, представляющее кодировщик ⟦ 3, 1, 1 ⟧ битного отражения кода и декодер с измерением синдром на месте.</span><span class="sxs-lookup"><span data-stu-id="7241a-105">Returns a QECC value representing the ⟦3, 1, 1⟧ bit flip code encoder and decoder with in-place syndrome measurement.</span></span>

```qsharp
function BitFlipCode () : Microsoft.Quantum.ErrorCorrection.QECC
```


## <a name="output--qecc"></a><span data-ttu-id="7241a-106">Выходные данные: [кекк](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span><span class="sxs-lookup"><span data-stu-id="7241a-106">Output : [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span></span>

<span data-ttu-id="7241a-107">Возвращает реализацию кода исправления ошибки такта путем указания `QECC` типа.</span><span class="sxs-lookup"><span data-stu-id="7241a-107">Returns an implementation of a quantum error correction code by specifying a `QECC` type.</span></span>