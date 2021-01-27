---
uid: Microsoft.Quantum.Canon.ApplyMultiplyControlledLowDepthAnd
title: Операция Апплимултипликонтролледловдепсанд
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiplyControlledLowDepthAnd
qsharp.summary: Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.  The adjoint operation assumes that the target qubit will be reset to 0.  Requires a Rz depth of 1, while the number of helper qubits are exponential in the number of qubits.
ms.openlocfilehash: 0ad4b6eabcbbb63751489dd92a13a6673c1ae6b1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841675"
---
# <a name="applymultiplycontrolledlowdepthand-operation"></a><span data-ttu-id="a904c-102">Операция Апплимултипликонтролледловдепсанд</span><span class="sxs-lookup"><span data-stu-id="a904c-102">ApplyMultiplyControlledLowDepthAnd operation</span></span>

<span data-ttu-id="a904c-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a904c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a904c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a904c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a904c-105">Реализует многоуправляемый шлюз Тоффоли, предполагая, что целевой кубит инициализирован 0.</span><span class="sxs-lookup"><span data-stu-id="a904c-105">Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.</span></span>  <span data-ttu-id="a904c-106">При выполнении примыкающей операции предполагается, что целевой кубит будет сброшен в 0.</span><span class="sxs-lookup"><span data-stu-id="a904c-106">The adjoint operation assumes that the target qubit will be reset to 0.</span></span>  <span data-ttu-id="a904c-107">Требуется РЗ глубина 1, а число вспомогательных Кубитс — экспоненциальное число Кубитс.</span><span class="sxs-lookup"><span data-stu-id="a904c-107">Requires a Rz depth of 1, while the number of helper qubits are exponential in the number of qubits.</span></span>

```qsharp
operation ApplyMultiplyControlledLowDepthAnd (controls : Qubit[], target : Qubit) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="a904c-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a904c-108">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="a904c-109">элементы управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a904c-109">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a904c-110">Управление Кубитс</span><span class="sxs-lookup"><span data-stu-id="a904c-110">Control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="a904c-111">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a904c-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a904c-112">Целевой кубит</span><span class="sxs-lookup"><span data-stu-id="a904c-112">Target qubit</span></span>



## <a name="output--unit"></a><span data-ttu-id="a904c-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a904c-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

