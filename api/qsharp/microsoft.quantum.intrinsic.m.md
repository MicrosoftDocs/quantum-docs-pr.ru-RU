---
uid: Microsoft.Quantum.Intrinsic.M
title: Операция M
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: M
qsharp.summary: >-
  Performs a measurement of a single qubit in the Pauli $Z$ basis.

  The output result is given by the distribution \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}. \end{align}
ms.openlocfilehash: 0037d7f5ad060857c6ca2c863b1d24aca3e338cf
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818873"
---
# <a name="m-operation"></a><span data-ttu-id="12047-102">Операция M</span><span class="sxs-lookup"><span data-stu-id="12047-102">M operation</span></span>

<span data-ttu-id="12047-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="12047-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="12047-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="12047-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="12047-105">Выполняет измерение отдельного кубита в Паули $Z $.</span><span class="sxs-lookup"><span data-stu-id="12047-105">Performs a measurement of a single qubit in the Pauli $Z$ basis.</span></span>

<span data-ttu-id="12047-106">Результат вывода задается параметром Distribution \бегин{алигн} \Пр (\Тексттт{зеро} | \кет{\пси}) = \бракет{\пси | 0} \braket{0 | \пси}.</span><span class="sxs-lookup"><span data-stu-id="12047-106">The output result is given by the distribution \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}.</span></span>
<span data-ttu-id="12047-107">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="12047-107">\end{align}</span></span>

```qsharp
operation M (qubit : Qubit) : Result
```


## <a name="input"></a><span data-ttu-id="12047-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="12047-108">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="12047-109">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="12047-109">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="12047-110">Кубит.</span><span class="sxs-lookup"><span data-stu-id="12047-110">Qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="12047-111">Выходные данные __: <Result> Недопустимый__</span><span class="sxs-lookup"><span data-stu-id="12047-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="12047-112">`Zero` Если обнаружено значение $ + $1 еиженвалуе, а `One` также значение $-$1 еиженвалуе.</span><span class="sxs-lookup"><span data-stu-id="12047-112">`Zero` if the $+1$ eigenvalue is observed, and `One` if the $-1$ eigenvalue is observed.</span></span>

## <a name="remarks"></a><span data-ttu-id="12047-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="12047-113">Remarks</span></span>

<span data-ttu-id="12047-114">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="12047-114">Equivalent to:</span></span>

```qsharp
Measure([PauliZ], [qubit]);
```