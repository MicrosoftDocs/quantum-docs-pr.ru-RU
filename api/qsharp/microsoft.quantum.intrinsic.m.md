---
uid: Microsoft.Quantum.Intrinsic.M
title: Операция M
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: M
qsharp.summary: >-
  Performs a measurement of a single qubit in the Pauli $Z$ basis.

  The output result is given by the distribution \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}. \end{align}
ms.openlocfilehash: 8d4b120385bfc7086a7cb0e3f77034c760d78d92
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731393"
---
# <a name="m-operation"></a><span data-ttu-id="d03a4-102">Операция M</span><span class="sxs-lookup"><span data-stu-id="d03a4-102">M operation</span></span>

<span data-ttu-id="d03a4-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="d03a4-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="d03a4-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d03a4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d03a4-105">Выполняет измерение отдельного кубита в Паули $Z $.</span><span class="sxs-lookup"><span data-stu-id="d03a4-105">Performs a measurement of a single qubit in the Pauli $Z$ basis.</span></span>

<span data-ttu-id="d03a4-106">Результат вывода задается параметром Distribution \бегин{алигн} \Пр (\Тексттт{зеро} | \кет{\пси}) = \бракет{\пси | 0} \braket{0 | \пси}.</span><span class="sxs-lookup"><span data-stu-id="d03a4-106">The output result is given by the distribution \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}.</span></span>
<span data-ttu-id="d03a4-107">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="d03a4-107">\end{align}</span></span>

```qsharp
operation M (qubit : Qubit) : Result
```


## <a name="input"></a><span data-ttu-id="d03a4-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d03a4-108">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="d03a4-109">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d03a4-109">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="d03a4-110">Кубит.</span><span class="sxs-lookup"><span data-stu-id="d03a4-110">Qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="d03a4-111">Выходные данные __: <Result> Недопустимый__</span><span class="sxs-lookup"><span data-stu-id="d03a4-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="d03a4-112">`Zero` Если обнаружено значение $ + $1 еиженвалуе, а `One` также значение $-$1 еиженвалуе.</span><span class="sxs-lookup"><span data-stu-id="d03a4-112">`Zero` if the $+1$ eigenvalue is observed, and `One` if the $-1$ eigenvalue is observed.</span></span>

## <a name="remarks"></a><span data-ttu-id="d03a4-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="d03a4-113">Remarks</span></span>

<span data-ttu-id="d03a4-114">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="d03a4-114">Equivalent to:</span></span>

```qsharp
Measure([PauliZ], [qubit]);
```