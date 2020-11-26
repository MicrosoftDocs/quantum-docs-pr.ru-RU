---
uid: Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget
title: Операция Аппликсконтролледонтрустаблевисклеантаржет
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyXControlledOnTruthTableWithCleanTarget
qsharp.summary: Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.
ms.openlocfilehash: 904ff7e2e7e81ee966846af120e9427f4e92301c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203269"
---
# <a name="applyxcontrolledontruthtablewithcleantarget-operation"></a><span data-ttu-id="6c7ed-102">Операция Аппликсконтролледонтрустаблевисклеантаржет</span><span class="sxs-lookup"><span data-stu-id="6c7ed-102">ApplyXControlledOnTruthTableWithCleanTarget operation</span></span>

<span data-ttu-id="6c7ed-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="6c7ed-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="6c7ed-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6c7ed-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6c7ed-105">Применяет @"microsoft.quantum.intrinsic.x" операцию к `target` , если логическая функция `func` возвращает значение true для классического назначения в `controlRegister` .</span><span class="sxs-lookup"><span data-stu-id="6c7ed-105">Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.</span></span>

```qsharp
operation ApplyXControlledOnTruthTableWithCleanTarget (func : BigInt, controlRegister : Qubit[], target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="6c7ed-106">Описание</span><span class="sxs-lookup"><span data-stu-id="6c7ed-106">Description</span></span>

<span data-ttu-id="6c7ed-107">Эта операция реализует особый случай @"microsoft.quantum.synthesis.applyxcontrolledontruthtable" , в котором Целевая кубит находится в состоянии $ \кет {0} $.</span><span class="sxs-lookup"><span data-stu-id="6c7ed-107">This operation implements a special case of @"microsoft.quantum.synthesis.applyxcontrolledontruthtable", in which the target qubit is known to be in the $\ket{0}$ state.</span></span>

<span data-ttu-id="6c7ed-108">В реализации используются @"microsoft.quantum.intrinsic.cnot" @"microsoft.quantum.intrinsic.r1" шлюзы и.</span><span class="sxs-lookup"><span data-stu-id="6c7ed-108">The implementation makes use of @"microsoft.quantum.intrinsic.cnot" and @"microsoft.quantum.intrinsic.r1" gates.</span></span>  <span data-ttu-id="6c7ed-109">Реализация примыкающей операции оптимизирована и использует невычисление на основе измерения.</span><span class="sxs-lookup"><span data-stu-id="6c7ed-109">The implementation of the adjoint operation is optimized and uses measurement-based uncomputation.</span></span>

## <a name="input"></a><span data-ttu-id="6c7ed-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6c7ed-110">Input</span></span>

### <a name="func--bigint"></a><span data-ttu-id="6c7ed-111">Func: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="6c7ed-111">func : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="6c7ed-112">Логическая таблица истинности, представленная как большое целое число</span><span class="sxs-lookup"><span data-stu-id="6c7ed-112">Boolean truth table represented as big integer</span></span>


### <a name="controlregister--qubit"></a><span data-ttu-id="6c7ed-113">Контролрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="6c7ed-113">controlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="6c7ed-114">Регистрация элемента управления Кубитс</span><span class="sxs-lookup"><span data-stu-id="6c7ed-114">Register of control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="6c7ed-115">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="6c7ed-115">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="6c7ed-116">Целевой кубит (должен находиться в $ \кет {0} $ State)</span><span class="sxs-lookup"><span data-stu-id="6c7ed-116">Target qubit (must be in $\ket{0}$ state)</span></span>



## <a name="output--unit"></a><span data-ttu-id="6c7ed-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6c7ed-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="6c7ed-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="6c7ed-118">See Also</span></span>

- [<span data-ttu-id="6c7ed-119">Microsoft. тактов. синтез. Аппликсконтролледонтрустабле</span><span class="sxs-lookup"><span data-stu-id="6c7ed-119">Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTable</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTable)