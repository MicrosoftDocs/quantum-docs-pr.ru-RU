---
uid: Microsoft.Quantum.ErrorCorrection.RecoverCSS
title: Операция Рековерксс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: RecoverCSS
qsharp.summary: Performs a single round of error correction by a quantum code described by a `CSS` type.
ms.openlocfilehash: 48d3cd3d5f6aea265fac2f50b913ab855a31accf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712205"
---
# <a name="recovercss-operation"></a><span data-ttu-id="19d96-102">Операция Рековерксс</span><span class="sxs-lookup"><span data-stu-id="19d96-102">RecoverCSS operation</span></span>

<span data-ttu-id="19d96-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="19d96-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="19d96-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="19d96-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="19d96-105">Выполняет единичное округление исправления ошибки с помощью кода такта, описанного `CSS` типом.</span><span class="sxs-lookup"><span data-stu-id="19d96-105">Performs a single round of error correction by a quantum code described by a `CSS` type.</span></span>

```qsharp
operation RecoverCSS (code : Microsoft.Quantum.ErrorCorrection.CSS, fnX : Microsoft.Quantum.ErrorCorrection.RecoveryFn, fnZ : Microsoft.Quantum.ErrorCorrection.RecoveryFn, logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : Unit
```


## <a name="input"></a><span data-ttu-id="19d96-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="19d96-106">Input</span></span>

### <a name="code--css"></a><span data-ttu-id="19d96-107">код: [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span><span class="sxs-lookup"><span data-stu-id="19d96-107">code : [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span></span>

<span data-ttu-id="19d96-108">В такте ошибки CSS, упакованной в виде типа, `CSS` описывается кодирование и декодирование данных тактов, а также способ измерения ошибки синдромес.</span><span class="sxs-lookup"><span data-stu-id="19d96-108">A quantum CSS error-correcting code packaged as a `CSS` type describes the encoding and decoding of quantum data, and how error syndromes are to be measured.</span></span>


### <a name="fnx--recoveryfn"></a><span data-ttu-id="19d96-109">ФНКС: [рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="19d96-109">fnX : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="19d96-110">Объект `RecoveryFn` , сопоставляющий каждый $X $ Error синдром с `Pauli[]` операциями, которые исправлять обнаруженную ошибку.</span><span class="sxs-lookup"><span data-stu-id="19d96-110">A `RecoveryFn` that maps each $X$ error syndrome to the `Pauli[]` operations that correct the detected error.</span></span>


### <a name="fnz--recoveryfn"></a><span data-ttu-id="19d96-111">Фнз: [рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="19d96-111">fnZ : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="19d96-112">Объект `RecoveryFn` , сопоставляющий каждый $Z $ Error синдром с `Pauli[]` операциями, которые исправлять обнаруженную ошибку.</span><span class="sxs-lookup"><span data-stu-id="19d96-112">A `RecoveryFn` that maps each $Z$ error syndrome to the `Pauli[]` operations that correct the detected error.</span></span>


### <a name="logicalregister--logicalregister"></a><span data-ttu-id="19d96-113">Логикалрегистер: [логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="19d96-113">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="19d96-114">Массив Кубитс, в котором определен код стабилизер.</span><span class="sxs-lookup"><span data-stu-id="19d96-114">An array of qubits where the stabilizer code is defined.</span></span>



## <a name="output--unit"></a><span data-ttu-id="19d96-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="19d96-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="19d96-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="19d96-116">See Also</span></span>

- [<span data-ttu-id="19d96-117">Microsoft. тактов. Ерроркорректион. CSS</span><span class="sxs-lookup"><span data-stu-id="19d96-117">Microsoft.Quantum.ErrorCorrection.CSS</span></span>](xref:Microsoft.Quantum.ErrorCorrection.CSS)
- [<span data-ttu-id="19d96-118">Microsoft. тактов. Ерроркорректион. Рековерифн</span><span class="sxs-lookup"><span data-stu-id="19d96-118">Microsoft.Quantum.ErrorCorrection.RecoveryFn</span></span>](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)
- [<span data-ttu-id="19d96-119">Microsoft. тактов. Ерроркорректион. Логикалрегистер</span><span class="sxs-lookup"><span data-stu-id="19d96-119">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)