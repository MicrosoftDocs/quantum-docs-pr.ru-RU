---
uid: Microsoft.Quantum.ErrorCorrection._ExtractLogicalQubitFromSteaneCode
title: _ExtractLogicalQubitFromSteaneCode операция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: _ExtractLogicalQubitFromSteaneCode
qsharp.summary: >-
  Syndrome measurement and the inverse of embedding.

  $X$- and $Z$-stabilizers are not treated equally, which is due to the particular choice of the encoding circuit. This asymmetry leads to a different syndrome extraction routine. One could measure the syndrome by measuring multi-qubit Pauli operator directly on the code state, but for the distillation purpose the logical qubit is returned into a single qubit, in course of which the syndrome measurements can be done without further ancillas.
ms.openlocfilehash: 71390feb84660cc9bf7bb12b64eac6d3ca512387
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712556"
---
# <a name="_extractlogicalqubitfromsteanecode-operation"></a><span data-ttu-id="7b6c4-102">_ExtractLogicalQubitFromSteaneCode операция</span><span class="sxs-lookup"><span data-stu-id="7b6c4-102">_ExtractLogicalQubitFromSteaneCode operation</span></span>

<span data-ttu-id="7b6c4-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="7b6c4-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="7b6c4-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7b6c4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7b6c4-105">Синдром измерение и обратное внедрение.</span><span class="sxs-lookup"><span data-stu-id="7b6c4-105">Syndrome measurement and the inverse of embedding.</span></span>

<span data-ttu-id="7b6c4-106">$X $-and $Z $-стабилизерс не обрабатываются одинаково, что обусловлено определенным выбором канала кодирования.</span><span class="sxs-lookup"><span data-stu-id="7b6c4-106">$X$- and $Z$-stabilizers are not treated equally, which is due to the particular choice of the encoding circuit.</span></span>
<span data-ttu-id="7b6c4-107">Эта асимметрию приводит к другой подпрограммы извлечения синдром.</span><span class="sxs-lookup"><span data-stu-id="7b6c4-107">This asymmetry leads to a different syndrome extraction routine.</span></span>
<span data-ttu-id="7b6c4-108">Можно измерить синдром, изменив оператор Multi-кубит Паули непосредственно в состоянии кода, но для цели «по-прежнему» логическая кубит возвращается в один кубит, в рамках которого измерения синдром могут быть выполнены без дополнительных анЦиллас.</span><span class="sxs-lookup"><span data-stu-id="7b6c4-108">One could measure the syndrome by measuring multi-qubit Pauli operator directly on the code state, but for the distillation purpose the logical qubit is returned into a single qubit, in course of which the syndrome measurements can be done without further ancillas.</span></span>

```qsharp
operation _ExtractLogicalQubitFromSteaneCode (code : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit, Int, Int)
```


## <a name="input"></a><span data-ttu-id="7b6c4-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7b6c4-109">Input</span></span>

### <a name="code--logicalregister"></a><span data-ttu-id="7b6c4-110">код: [логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="7b6c4-110">code : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>





## <a name="output--qubitintint"></a><span data-ttu-id="7b6c4-111">Выходные данные: ([кубит](xref:microsoft.quantum.lang-ref.qubit),[int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="7b6c4-111">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>

<span data-ttu-id="7b6c4-112">Логические кубит и пара целых чисел для $X $-синдром и $Z $-синдром.</span><span class="sxs-lookup"><span data-stu-id="7b6c4-112">The logical qubit and a pair of integers for $X$-syndrome and $Z$-syndrome.</span></span>
<span data-ttu-id="7b6c4-113">Они представляют индекс кода кубит, в котором одна $X $-или $Z $-Error вызывала измеряемый синдром.</span><span class="sxs-lookup"><span data-stu-id="7b6c4-113">They represent the index of the code qubit on which a single $X$- or $Z$-error would have caused the measured syndrome.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b6c4-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="7b6c4-114">Remarks</span></span>

<span data-ttu-id="7b6c4-115">Обратите внимание, что эта операция не помечена как `internal` , так как модульные тесты непосредственно зависят от этой операции.</span><span class="sxs-lookup"><span data-stu-id="7b6c4-115">Note that this operation is not marked as `internal`, as unit tests directly depend on this operation.</span></span> <span data-ttu-id="7b6c4-116">В качестве будущего улучшения модульные тесты должны быть подвергнуты рефакторингу, чтобы они зависели только от открытых вызываемых.</span><span class="sxs-lookup"><span data-stu-id="7b6c4-116">As a future improvement, unit tests should be refactored to depend only on public callables directly.</span></span>

> [!WARNING]
> <span data-ttu-id="7b6c4-117">Эта подпрограмма адаптирована к определенному каналу кодирования для кода Стеане 7 кубит; Если канал кодирования изменен, результат синдром может быть интерпретирован иначе.</span><span class="sxs-lookup"><span data-stu-id="7b6c4-117">This routine is tailored to a particular encoding circuit for Steane's 7 qubit code; if the encoding circuit is modified then the syndrome outcome might have to be interpreted differently.</span></span>