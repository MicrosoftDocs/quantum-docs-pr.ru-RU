---
uid: Microsoft.Quantum.ErrorCorrection.RecoverCSS
title: Операция Рековерксс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: RecoverCSS
qsharp.summary: Performs a single round of error correction by a quantum code described by a `CSS` type.
ms.openlocfilehash: c192abbdfd02b26fbdba7b11f51ed08bb1a2030f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853037"
---
# <a name="recovercss-operation"></a><span data-ttu-id="0cf3e-102">Операция Рековерксс</span><span class="sxs-lookup"><span data-stu-id="0cf3e-102">RecoverCSS operation</span></span>

<span data-ttu-id="0cf3e-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="0cf3e-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="0cf3e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0cf3e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0cf3e-105">Выполняет единичное округление исправления ошибки с помощью кода такта, описанного `CSS` типом.</span><span class="sxs-lookup"><span data-stu-id="0cf3e-105">Performs a single round of error correction by a quantum code described by a `CSS` type.</span></span>

```qsharp
operation RecoverCSS (code : Microsoft.Quantum.ErrorCorrection.CSS, fnX : Microsoft.Quantum.ErrorCorrection.RecoveryFn, fnZ : Microsoft.Quantum.ErrorCorrection.RecoveryFn, logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : Unit
```


## <a name="input"></a><span data-ttu-id="0cf3e-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0cf3e-106">Input</span></span>

### <a name="code--css"></a><span data-ttu-id="0cf3e-107">код: [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span><span class="sxs-lookup"><span data-stu-id="0cf3e-107">code : [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span></span>

<span data-ttu-id="0cf3e-108">В такте ошибки CSS, упакованной в виде типа, `CSS` описывается кодирование и декодирование данных тактов, а также способ измерения ошибки синдромес.</span><span class="sxs-lookup"><span data-stu-id="0cf3e-108">A quantum CSS error-correcting code packaged as a `CSS` type describes the encoding and decoding of quantum data, and how error syndromes are to be measured.</span></span>


### <a name="fnx--recoveryfn"></a><span data-ttu-id="0cf3e-109">ФНКС: [рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="0cf3e-109">fnX : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="0cf3e-110">Объект `RecoveryFn` , сопоставляющий каждый $X $ Error синдром с `Pauli[]` операциями, которые исправлять обнаруженную ошибку.</span><span class="sxs-lookup"><span data-stu-id="0cf3e-110">A `RecoveryFn` that maps each $X$ error syndrome to the `Pauli[]` operations that correct the detected error.</span></span>


### <a name="fnz--recoveryfn"></a><span data-ttu-id="0cf3e-111">Фнз: [рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="0cf3e-111">fnZ : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="0cf3e-112">Объект `RecoveryFn` , сопоставляющий каждый $Z $ Error синдром с `Pauli[]` операциями, которые исправлять обнаруженную ошибку.</span><span class="sxs-lookup"><span data-stu-id="0cf3e-112">A `RecoveryFn` that maps each $Z$ error syndrome to the `Pauli[]` operations that correct the detected error.</span></span>


### <a name="logicalregister--logicalregister"></a><span data-ttu-id="0cf3e-113">Логикалрегистер: [логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="0cf3e-113">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="0cf3e-114">Массив Кубитс, в котором определен код стабилизер.</span><span class="sxs-lookup"><span data-stu-id="0cf3e-114">An array of qubits where the stabilizer code is defined.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0cf3e-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0cf3e-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="0cf3e-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="0cf3e-116">See Also</span></span>

- [<span data-ttu-id="0cf3e-117">Microsoft. тактов. Ерроркорректион. CSS</span><span class="sxs-lookup"><span data-stu-id="0cf3e-117">Microsoft.Quantum.ErrorCorrection.CSS</span></span>](xref:Microsoft.Quantum.ErrorCorrection.CSS)
- [<span data-ttu-id="0cf3e-118">Microsoft. тактов. Ерроркорректион. Рековерифн</span><span class="sxs-lookup"><span data-stu-id="0cf3e-118">Microsoft.Quantum.ErrorCorrection.RecoveryFn</span></span>](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)
- [<span data-ttu-id="0cf3e-119">Microsoft. тактов. Ерроркорректион. Логикалрегистер</span><span class="sxs-lookup"><span data-stu-id="0cf3e-119">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)