---
uid: Microsoft.Quantum.ErrorCorrection.MeasureStabilizerGenerators
title: Операция Меасурестабилизерженераторс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: MeasureStabilizerGenerators
qsharp.summary: Measures the given set of generators of a stabilizer group.
ms.openlocfilehash: a3f48ff24a39d13a57f7a144e21d4e41bb8a8b49
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712262"
---
# <a name="measurestabilizergenerators-operation"></a><span data-ttu-id="bacfc-102">Операция Меасурестабилизерженераторс</span><span class="sxs-lookup"><span data-stu-id="bacfc-102">MeasureStabilizerGenerators operation</span></span>

<span data-ttu-id="bacfc-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="bacfc-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="bacfc-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bacfc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bacfc-105">Измеряет заданный набор генераторов группы стабилизер.</span><span class="sxs-lookup"><span data-stu-id="bacfc-105">Measures the given set of generators of a stabilizer group.</span></span>

```qsharp
operation MeasureStabilizerGenerators (stabilizerGroup : Pauli[][], logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister, gadget : ((Pauli[], Qubit[]) => Result)) : Microsoft.Quantum.ErrorCorrection.Syndrome
```


## <a name="input"></a><span data-ttu-id="bacfc-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bacfc-106">Input</span></span>

### <a name="stabilizergroup--pauli"></a><span data-ttu-id="bacfc-107">Стабилизерграуп: [Паули](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="bacfc-107">stabilizerGroup : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="bacfc-108">Массив операторов Паули мултикубит.</span><span class="sxs-lookup"><span data-stu-id="bacfc-108">An array of multiqubit Pauli operators.</span></span>
<span data-ttu-id="bacfc-109">Например, `stabilizerGroup[0]` представляет собой список однокубитных матриц Паули, продукт тензорные, который является генератором стабилизер.</span><span class="sxs-lookup"><span data-stu-id="bacfc-109">For example, `stabilizerGroup[0]` is a list of single-qubit Pauli matrices, the tensor product of which is a stabilizer generator.</span></span>


### <a name="logicalregister--logicalregister"></a><span data-ttu-id="bacfc-110">Логикалрегистер: [логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="bacfc-110">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="bacfc-111">Массив Кубитс, в котором определен код стабилизер.</span><span class="sxs-lookup"><span data-stu-id="bacfc-111">An array of qubits where the stabilizer code is defined.</span></span>


### <a name="gadget--pauliqubit--__invalidresult__"></a><span data-ttu-id="bacfc-112">Мини-приложение: ( [Паули](xref:microsoft.quantum.lang-ref.pauli)[], [кубит](xref:microsoft.quantum.lang-ref.qubit)[]) __= <Result> Недопустимый__ ></span><span class="sxs-lookup"><span data-stu-id="bacfc-112">gadget : ( [Pauli](xref:microsoft.quantum.lang-ref.pauli)[], [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __invalid<Result>__</span></span> 

<span data-ttu-id="bacfc-113">Операция, указывающая, как измерять оператор мултикубит Паули.</span><span class="sxs-lookup"><span data-stu-id="bacfc-113">An operation that specifies how to measure a multiqubit Pauli operator.</span></span>



## <a name="output--syndrome"></a><span data-ttu-id="bacfc-114">Выходные данные: [синдром](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span><span class="sxs-lookup"><span data-stu-id="bacfc-114">Output : [Syndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span></span>

<span data-ttu-id="bacfc-115">Результат измерений.</span><span class="sxs-lookup"><span data-stu-id="bacfc-115">The result of measurements.</span></span>

## <a name="remarks"></a><span data-ttu-id="bacfc-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="bacfc-116">Remarks</span></span>

<span data-ttu-id="bacfc-117">Это не проверяет, работает ли данный набор генераторов.</span><span class="sxs-lookup"><span data-stu-id="bacfc-117">This does not check if the given set of generators are commuting.</span></span>
<span data-ttu-id="bacfc-118">В противном случае результат измерения может быть произвольным.</span><span class="sxs-lookup"><span data-stu-id="bacfc-118">If they are not commuting, the result of measurements may be arbitrary.</span></span>