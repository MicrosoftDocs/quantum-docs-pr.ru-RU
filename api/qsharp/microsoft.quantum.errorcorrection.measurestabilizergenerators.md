---
uid: Microsoft.Quantum.ErrorCorrection.MeasureStabilizerGenerators
title: Операция Меасурестабилизерженераторс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: MeasureStabilizerGenerators
qsharp.summary: Measures the given set of generators of a stabilizer group.
ms.openlocfilehash: 6c048c17df21d1026dc671f30d72a13ed8d8b7f5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200634"
---
# <a name="measurestabilizergenerators-operation"></a><span data-ttu-id="26cc8-102">Операция Меасурестабилизерженераторс</span><span class="sxs-lookup"><span data-stu-id="26cc8-102">MeasureStabilizerGenerators operation</span></span>

<span data-ttu-id="26cc8-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="26cc8-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="26cc8-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="26cc8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="26cc8-105">Измеряет заданный набор генераторов группы стабилизер.</span><span class="sxs-lookup"><span data-stu-id="26cc8-105">Measures the given set of generators of a stabilizer group.</span></span>

```qsharp
operation MeasureStabilizerGenerators (stabilizerGroup : Pauli[][], logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister, gadget : ((Pauli[], Qubit[]) => Result)) : Microsoft.Quantum.ErrorCorrection.Syndrome
```


## <a name="input"></a><span data-ttu-id="26cc8-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="26cc8-106">Input</span></span>

### <a name="stabilizergroup--pauli"></a><span data-ttu-id="26cc8-107">Стабилизерграуп: [Паули](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="26cc8-107">stabilizerGroup : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="26cc8-108">Массив операторов Паули мултикубит.</span><span class="sxs-lookup"><span data-stu-id="26cc8-108">An array of multiqubit Pauli operators.</span></span>
<span data-ttu-id="26cc8-109">Например, `stabilizerGroup[0]` представляет собой список однокубитных матриц Паули, продукт тензорные, который является генератором стабилизер.</span><span class="sxs-lookup"><span data-stu-id="26cc8-109">For example, `stabilizerGroup[0]` is a list of single-qubit Pauli matrices, the tensor product of which is a stabilizer generator.</span></span>


### <a name="logicalregister--logicalregister"></a><span data-ttu-id="26cc8-110">Логикалрегистер: [логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="26cc8-110">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="26cc8-111">Массив Кубитс, в котором определен код стабилизер.</span><span class="sxs-lookup"><span data-stu-id="26cc8-111">An array of qubits where the stabilizer code is defined.</span></span>


### <a name="gadget--pauliqubit--__invalidresult__"></a><span data-ttu-id="26cc8-112">Мини-приложение: ([Паули](xref:microsoft.quantum.lang-ref.pauli)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) __= <Result> Недопустимый__></span><span class="sxs-lookup"><span data-stu-id="26cc8-112">gadget : ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __invalid<Result>__</span></span> 

<span data-ttu-id="26cc8-113">Операция, указывающая, как измерять оператор мултикубит Паули.</span><span class="sxs-lookup"><span data-stu-id="26cc8-113">An operation that specifies how to measure a multiqubit Pauli operator.</span></span>



## <a name="output--syndrome"></a><span data-ttu-id="26cc8-114">Выходные данные: [синдром](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span><span class="sxs-lookup"><span data-stu-id="26cc8-114">Output : [Syndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span></span>

<span data-ttu-id="26cc8-115">Результат измерений.</span><span class="sxs-lookup"><span data-stu-id="26cc8-115">The result of measurements.</span></span>

## <a name="remarks"></a><span data-ttu-id="26cc8-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26cc8-116">Remarks</span></span>

<span data-ttu-id="26cc8-117">Это не проверяет, работает ли данный набор генераторов.</span><span class="sxs-lookup"><span data-stu-id="26cc8-117">This does not check if the given set of generators are commuting.</span></span>
<span data-ttu-id="26cc8-118">В противном случае результат измерения может быть произвольным.</span><span class="sxs-lookup"><span data-stu-id="26cc8-118">If they are not commuting, the result of measurements may be arbitrary.</span></span>