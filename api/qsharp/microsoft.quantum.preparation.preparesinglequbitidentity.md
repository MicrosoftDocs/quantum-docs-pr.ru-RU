---
uid: Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity
title: Операция Препаресинглекубитидентити
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareSingleQubitIdentity
qsharp.summary: >-
  Prepares a qubit in the maximally mixed state.

  It prepares the given qubit in the $\boldone / 2$ state by applying the depolarizing channel $$ \begin{align} \Omega(\rho) \mathrel{:=} \frac{1}{4} \sum_{\mu \in \{0, 1, 2, 3\}} \sigma\_{\mu} \rho \sigma\_{\mu}^{\dagger}, \end{align} $$ where $\sigma\_i$ is the $i$th Pauli operator, and where $\rho$ is a density operator representing a mixed state.
ms.openlocfilehash: c6c9b5724354d6ee034dd8b6733901ebdd8072d6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856872"
---
# <a name="preparesinglequbitidentity-operation"></a><span data-ttu-id="cbf50-102">Операция Препаресинглекубитидентити</span><span class="sxs-lookup"><span data-stu-id="cbf50-102">PrepareSingleQubitIdentity operation</span></span>

<span data-ttu-id="cbf50-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="cbf50-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="cbf50-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cbf50-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cbf50-105">Подготавливает кубит в максимально смешанном состоянии.</span><span class="sxs-lookup"><span data-stu-id="cbf50-105">Prepares a qubit in the maximally mixed state.</span></span>

<span data-ttu-id="cbf50-106">Он подготавливает заданный кубит в состоянии $ \болдоне/$2, применяя канал деполаризинг $ $ \бегин{алигн} \Омега (\рхо) \масрел{: =} \фрак {1} {4} \ sum_ {\му \ин \{ 0, 1, 2, 3 \} } \сигма \_ {\му} \rho \sigma \_ {\mu} ^ {\dagger}, \end{align} $ $, где $ \sigma \_ i $ — $i $ TH Pauli, где $ \rho $ — оператор плотности, представляющий смешанное состояние.</span><span class="sxs-lookup"><span data-stu-id="cbf50-106">It prepares the given qubit in the $\boldone / 2$ state by applying the depolarizing channel $$ \begin{align} \Omega(\rho) \mathrel{:=} \frac{1}{4} \sum_{\mu \in \{0, 1, 2, 3\}} \sigma\_{\mu} \rho \sigma\_{\mu}^{\dagger}, \end{align} $$ where $\sigma\_i$ is the $i$th Pauli operator, and where $\rho$ is a density operator representing a mixed state.</span></span>

```qsharp
operation PrepareSingleQubitIdentity (qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="cbf50-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="cbf50-107">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="cbf50-108">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="cbf50-108">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="cbf50-109">Объект кубит, состояние которого необходимо деполяровать, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="cbf50-109">A qubit whose state is to be depolarized in the manner described above.</span></span>



## <a name="output--unit"></a><span data-ttu-id="cbf50-110">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cbf50-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="cbf50-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="cbf50-111">Remarks</span></span>

<span data-ttu-id="cbf50-112">Смешанное состояние $ \болдоне/$2, описывающее результат применения этой операции к состоянию, неявно описывает значение ожидания для случайных вариантов, сделанных в этой операции.</span><span class="sxs-lookup"><span data-stu-id="cbf50-112">The mixed state $\boldone / 2$ describing the result of applying this operation to a state implicitly describes an expectation value over random choices made in this operation.</span></span>
<span data-ttu-id="cbf50-113">Таким образом, для любого отдельного приложения эта операция сопоставляет чистые состояния с чистыми состояниями, но действует, как описано в разделе ожидание.</span><span class="sxs-lookup"><span data-stu-id="cbf50-113">Thus, for any single application, this operation maps pure states to pure states, but it acts as described in expectation.</span></span>
<span data-ttu-id="cbf50-114">В частности, эта операция может использоваться в процессе томографи для измерения *небазовых* компонентов канала.</span><span class="sxs-lookup"><span data-stu-id="cbf50-114">In particular, this operation can be used in process tomography to measure the *non-unital* components of a channel.</span></span>