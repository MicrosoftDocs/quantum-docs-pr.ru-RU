---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCodeRecoveryFn
title: Функция Фивекубиткодерековерифн
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCodeRecoveryFn
qsharp.summary: Returns function that maps error syndrome measurements to the appropriate error-correcting Pauli operators by table lookup for the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 5b8afe222d197eb7d342ac45f027f2de9130b61a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712331"
---
# <a name="fivequbitcoderecoveryfn-function"></a><span data-ttu-id="df4fc-102">Функция Фивекубиткодерековерифн</span><span class="sxs-lookup"><span data-stu-id="df4fc-102">FiveQubitCodeRecoveryFn function</span></span>

<span data-ttu-id="df4fc-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="df4fc-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="df4fc-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="df4fc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="df4fc-105">Функция возвращает функцию, которая сопоставляет измерения Error синдром с соответствующими операторами Паули с ошибками по таблице уточняющих запросов для ⟦ 5, 1, 3 ⟧ тактового кода.</span><span class="sxs-lookup"><span data-stu-id="df4fc-105">Returns function that maps error syndrome measurements to the appropriate error-correcting Pauli operators by table lookup for the ⟦5, 1, 3⟧ quantum code.</span></span>

```qsharp
function FiveQubitCodeRecoveryFn () : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="output--recoveryfn"></a><span data-ttu-id="df4fc-106">Выходные данные: [рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="df4fc-106">Output : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="df4fc-107">Функция типа `RecoveryFn` , которая принимает синдром измерение `Result[]` и возвращает `Pauli[]` операторы, которые исправляет обнаруженную ошибку.</span><span class="sxs-lookup"><span data-stu-id="df4fc-107">Function of type `RecoveryFn` that takes a syndrome measurement `Result[]` and returns the `Pauli[]` operators that corrects the detected error.</span></span>

## <a name="remarks"></a><span data-ttu-id="df4fc-108">Remarks</span><span class="sxs-lookup"><span data-stu-id="df4fc-108">Remarks</span></span>

<span data-ttu-id="df4fc-109">Просматривая все ошибки веса $1 $, мы получаем общую сумму в $3 – раз 5 = 15 $ возможные нетривиальные синдромес.</span><span class="sxs-lookup"><span data-stu-id="df4fc-109">By iterating over all errors of weight $1$, we obtain a total of $3\times 5=15$ possible non-trivial syndromes.</span></span>
<span data-ttu-id="df4fc-110">Вместе с удостоверением создается таблица ошибок и соответствующих синдром.</span><span class="sxs-lookup"><span data-stu-id="df4fc-110">Together with the identity, a table of error and corresponding syndrome is built up.</span></span> <span data-ttu-id="df4fc-111">Для 5-кубит кода, который получает эта таблица: $X \_ 1: (0, 0, 0, 1); X \_ 2: (1, 0, 0, 0); X \_ 3: (1, 1, 0, 0); X \_ 4: (0, 1, 1, 0); X \_ 5: (0, 0, 1, 1) $, $Z \_ 1: (1, 0, 1, 0); Z \_ 2: (0, 1, 0, 1); Z \_ 3: (0, 0, 1, 0); Z \_ 4: (1, 0, 0, 1); Z \_ 5: (0, 1, 0, 0) $ с $Y _i $ получено путем добавления $X _i $ и $Z _i $ синдромес.</span><span class="sxs-lookup"><span data-stu-id="df4fc-111">For the 5 qubit code this table is given by: $X\_1: (0,0,0,1); X\_2: (1,0,0,0); X\_3: (1,1,0,0); X\_4: (0,1,1,0); X\_5: (0,0,1,1)$, $Z\_1: (1,0,1,0); Z\_2: (0,1,0,1); Z\_3: (0,0,1,0); Z\_4: (1,0,0,1); Z\_5: (0,1,0,0)$ with $Y_i$ obtained by adding the $X_i$ and $Z_i$ syndromes.</span></span> <span data-ttu-id="df4fc-112">Обратите внимание, что порядок в восстановлении таблицы подстановки задается путем преобразования битвекторс в целые числа (с прямым порядком байтов).</span><span class="sxs-lookup"><span data-stu-id="df4fc-112">Note that the ordering in the table lookup recovery is given by converting the bitvectors to integers (using little endian).</span></span>

## <a name="see-also"></a><span data-ttu-id="df4fc-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="df4fc-113">See Also</span></span>

- [<span data-ttu-id="df4fc-114">Microsoft. тактов. Ерроркорректион. Рековерифн</span><span class="sxs-lookup"><span data-stu-id="df4fc-114">Microsoft.Quantum.ErrorCorrection.RecoveryFn</span></span>](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)