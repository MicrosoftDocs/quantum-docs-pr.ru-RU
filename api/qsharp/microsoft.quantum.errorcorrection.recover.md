---
uid: Microsoft.Quantum.ErrorCorrection.Recover
title: Операция восстановления
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: Recover
qsharp.summary: Performs a single round of error correction by a quantum code described by a `QECC` type.
ms.openlocfilehash: a659399f51794a4edc1d2ff43da84e46797103fb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712206"
---
# <a name="recover-operation"></a><span data-ttu-id="f91af-102">Операция восстановления</span><span class="sxs-lookup"><span data-stu-id="f91af-102">Recover operation</span></span>

<span data-ttu-id="f91af-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="f91af-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="f91af-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f91af-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f91af-105">Выполняет единичное округление исправления ошибки с помощью кода такта, описанного `QECC` типом.</span><span class="sxs-lookup"><span data-stu-id="f91af-105">Performs a single round of error correction by a quantum code described by a `QECC` type.</span></span>

```qsharp
operation Recover (code : Microsoft.Quantum.ErrorCorrection.QECC, fn : Microsoft.Quantum.ErrorCorrection.RecoveryFn, logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : Unit
```


## <a name="input"></a><span data-ttu-id="f91af-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f91af-106">Input</span></span>

### <a name="code--qecc"></a><span data-ttu-id="f91af-107">код: [кекк](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span><span class="sxs-lookup"><span data-stu-id="f91af-107">code : [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span></span>

<span data-ttu-id="f91af-108">Ошибка такта. Исправление кода, упакованного как `QECC` тип, описывает кодирование и декодирование данных тактов, а также способ измерения ошибки синдромес.</span><span class="sxs-lookup"><span data-stu-id="f91af-108">A quantum error-correcting code packaged as a `QECC` type describes the encoding and decoding of quantum data, and how error syndromes are to be measured.</span></span>


### <a name="fn--recoveryfn"></a><span data-ttu-id="f91af-109">FN: [рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="f91af-109">fn : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="f91af-110">Объект `RecoveryFn` , сопоставляющий каждую ошибку, синдром с `Pauli[]` операциями, которые исправлять обнаруженную ошибку.</span><span class="sxs-lookup"><span data-stu-id="f91af-110">A `RecoveryFn` that maps each error syndrome to the `Pauli[]` operations that correct the detected error.</span></span>


### <a name="logicalregister--logicalregister"></a><span data-ttu-id="f91af-111">Логикалрегистер: [логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="f91af-111">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="f91af-112">Массив Кубитс, в котором определен код стабилизер.</span><span class="sxs-lookup"><span data-stu-id="f91af-112">An array of qubits where the stabilizer code is defined.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f91af-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f91af-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="f91af-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="f91af-114">See Also</span></span>

- [<span data-ttu-id="f91af-115">Microsoft. тактов. Ерроркорректион. КЕКК</span><span class="sxs-lookup"><span data-stu-id="f91af-115">Microsoft.Quantum.ErrorCorrection.QECC</span></span>](xref:Microsoft.Quantum.ErrorCorrection.QECC)
- [<span data-ttu-id="f91af-116">Microsoft. тактов. Ерроркорректион. Рековерифн</span><span class="sxs-lookup"><span data-stu-id="f91af-116">Microsoft.Quantum.ErrorCorrection.RecoveryFn</span></span>](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)
- [<span data-ttu-id="f91af-117">Microsoft. тактов. Ерроркорректион. Логикалрегистер</span><span class="sxs-lookup"><span data-stu-id="f91af-117">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)