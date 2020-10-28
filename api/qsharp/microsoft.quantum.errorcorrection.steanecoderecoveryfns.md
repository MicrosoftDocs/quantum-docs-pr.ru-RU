---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns
title: Функция Стеанекодерековерифнс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryFns
qsharp.summary: Decoder for combined X- and Z-parts of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: b1dd1c2e9a71e58bd8a86d1759a8b6af13a49614
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712136"
---
# <a name="steanecoderecoveryfns-function"></a><span data-ttu-id="c37f4-102">Функция Стеанекодерековерифнс</span><span class="sxs-lookup"><span data-stu-id="c37f4-102">SteaneCodeRecoveryFns function</span></span>

<span data-ttu-id="c37f4-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="c37f4-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="c37f4-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c37f4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c37f4-105">Декодер для Объединенных X-и Z-частей стабилизер группы ⟦ 7, 1, 3 ⟧ Стеане.</span><span class="sxs-lookup"><span data-stu-id="c37f4-105">Decoder for combined X- and Z-parts of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.</span></span>

```qsharp
function SteaneCodeRecoveryFns () : (Microsoft.Quantum.ErrorCorrection.RecoveryFn, Microsoft.Quantum.ErrorCorrection.RecoveryFn)
```


## <a name="output--recoveryfnrecoveryfn"></a><span data-ttu-id="c37f4-106">Выходные данные: ([рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn),[рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn))</span><span class="sxs-lookup"><span data-stu-id="c37f4-106">Output : ([RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn),[RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn))</span></span>

<span data-ttu-id="c37f4-107">Кортеж функций типа `RecoveryFn` , принимающий измерение синдром `Result[]` и возвращающий `Pauli[]` операции, которые исправляет обнаруженную ошибку.</span><span class="sxs-lookup"><span data-stu-id="c37f4-107">Tuple of functions of type `RecoveryFn` that takes a syndrome measurement `Result[]` and returns the `Pauli[]` operations that corrects the detected error.</span></span>

## <a name="see-also"></a><span data-ttu-id="c37f4-108">См. также:</span><span class="sxs-lookup"><span data-stu-id="c37f4-108">See Also</span></span>

- [<span data-ttu-id="c37f4-109">Microsoft. тактов. Ерроркорректион. Стеанекодерековерикс</span><span class="sxs-lookup"><span data-stu-id="c37f4-109">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [<span data-ttu-id="c37f4-110">Microsoft. тактов. Ерроркорректион. Стеанекодерековериз</span><span class="sxs-lookup"><span data-stu-id="c37f4-110">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryZ</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryZ)