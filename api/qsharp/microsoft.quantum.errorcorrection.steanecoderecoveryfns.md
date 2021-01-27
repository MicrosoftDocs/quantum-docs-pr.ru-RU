---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns
title: Функция Стеанекодерековерифнс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryFns
qsharp.summary: Decoder for combined X- and Z-parts of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 8dc715042f98b90b8cea7e2d6ecb5d02a78d297f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853027"
---
# <a name="steanecoderecoveryfns-function"></a><span data-ttu-id="8916d-102">Функция Стеанекодерековерифнс</span><span class="sxs-lookup"><span data-stu-id="8916d-102">SteaneCodeRecoveryFns function</span></span>

<span data-ttu-id="8916d-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="8916d-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="8916d-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8916d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8916d-105">Декодер для Объединенных X-и Z-частей стабилизер группы ⟦ 7, 1, 3 ⟧ Стеане.</span><span class="sxs-lookup"><span data-stu-id="8916d-105">Decoder for combined X- and Z-parts of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.</span></span>

```qsharp
function SteaneCodeRecoveryFns () : (Microsoft.Quantum.ErrorCorrection.RecoveryFn, Microsoft.Quantum.ErrorCorrection.RecoveryFn)
```


## <a name="output--recoveryfnrecoveryfn"></a><span data-ttu-id="8916d-106">Выходные данные: ([рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn),[рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn))</span><span class="sxs-lookup"><span data-stu-id="8916d-106">Output : ([RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn),[RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn))</span></span>

<span data-ttu-id="8916d-107">Кортеж функций типа `RecoveryFn` , принимающий измерение синдром `Result[]` и возвращающий `Pauli[]` операции, которые исправляет обнаруженную ошибку.</span><span class="sxs-lookup"><span data-stu-id="8916d-107">Tuple of functions of type `RecoveryFn` that takes a syndrome measurement `Result[]` and returns the `Pauli[]` operations that corrects the detected error.</span></span>

## <a name="see-also"></a><span data-ttu-id="8916d-108">См. также:</span><span class="sxs-lookup"><span data-stu-id="8916d-108">See Also</span></span>

- [<span data-ttu-id="8916d-109">Microsoft. тактов. Ерроркорректион. Стеанекодерековерикс</span><span class="sxs-lookup"><span data-stu-id="8916d-109">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [<span data-ttu-id="8916d-110">Microsoft. тактов. Ерроркорректион. Стеанекодерековериз</span><span class="sxs-lookup"><span data-stu-id="8916d-110">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryZ</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryZ)