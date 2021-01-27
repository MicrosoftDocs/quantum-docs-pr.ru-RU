---
uid: Microsoft.Quantum.Synthesis.ApplyUnitary
title: Операция Апплюнитари
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyUnitary
qsharp.summary: >-
  Applies gate defined by 2^n x 2^n unitary matrix.

  Fails if matrix is not unitary, or has wrong size.
ms.openlocfilehash: 58215d3b05b8c6974e979d21a13869f27b436310
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98859262"
---
# <a name="applyunitary-operation"></a><span data-ttu-id="b4f91-102">Операция Апплюнитари</span><span class="sxs-lookup"><span data-stu-id="b4f91-102">ApplyUnitary operation</span></span>

<span data-ttu-id="b4f91-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="b4f91-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="b4f91-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b4f91-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b4f91-105">Применяет шлюз, определенный 2 ^ n x 2 ^ n, единой матрицей.</span><span class="sxs-lookup"><span data-stu-id="b4f91-105">Applies gate defined by 2^n x 2^n unitary matrix.</span></span>

<span data-ttu-id="b4f91-106">Завершается ошибкой, если матрица не является единой или имеет неправильный размер.</span><span class="sxs-lookup"><span data-stu-id="b4f91-106">Fails if matrix is not unitary, or has wrong size.</span></span>

```qsharp
operation ApplyUnitary (unitary : Microsoft.Quantum.Math.Complex[][], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="b4f91-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b4f91-107">Input</span></span>

### <a name="unitary--complex"></a><span data-ttu-id="b4f91-108">Единая: [сложная](xref:Microsoft.Quantum.Math.Complex)[] []</span><span class="sxs-lookup"><span data-stu-id="b4f91-108">unitary : [Complex](xref:Microsoft.Quantum.Math.Complex)[][]</span></span>

<span data-ttu-id="b4f91-109">2 ^ n x 2 ^ n единая матрица, описывающая операцию.</span><span class="sxs-lookup"><span data-stu-id="b4f91-109">2^n x 2^n unitary matrix describing the operation.</span></span>
<span data-ttu-id="b4f91-110">Если матрица не является единой или не является подходящим размером, создает исключение.</span><span class="sxs-lookup"><span data-stu-id="b4f91-110">If matrix is not unitary or not of suitable size, throws an exception.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="b4f91-111">Кубитс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="b4f91-111">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="b4f91-112">Кубитс, к которому применяется регистр операций с длиной n.</span><span class="sxs-lookup"><span data-stu-id="b4f91-112">Qubits to which apply the operation - register of length n.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b4f91-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b4f91-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

